# 🎣 Project Fishing

> An AI lead-generation engine that **generates its target market out of nothing** — it autonomously
> discovers the customer persona and the online **"ponds"** where they gather, attracts them with a
> disclosed AI **spokesman + lure**, senses interest through a **browser-native watch-eye**, then hands
> qualified, researched leads to an external **CRM**. Everything is framed as **placement marketing**
> (utility inside context, not advertising). Built first for the **colo agents** business;
> multi-tenant-ready (`workspace = business`).

**Source of truth:** [`docs/superpowers/specs/2026-06-29-project-fishing-design.md`](docs/superpowers/specs/2026-06-29-project-fishing-design.md)
(with decisions **D1–D22**). This README is a summary; **the spec governs where they differ.**

**Operating the dashboard:** see [`DASHBOARD-README.md`](DASHBOARD-README.md) for the click-by-click guide.

---

## The core insight

colo sells *"full AI autonomy in a data center"* — a **net-new category**. There is no existing market,
no comparable, and no customer list. So the engine can't filter a database; it must **search the live web
and generate the best-guess persona + the ponds where they congregate**, then go fish them and let **real
conversion** correct its hypotheses. This is **blue-water category creation**, not competition — the buyer is
*discovered*, not assumed.

The make-or-break stage is the **generative identification of fish + pond** (Stage 1); get it wrong and
every downstream stage is wasted. The hard problem is turning an AI hypothesis into a *trusted* target
before spending on it — solved by (a) **web-citation evidence** for every claim, (b) a cheap **watch-eye**
that validates in days, and (c) a **verified owned-page conversion** as the ground-truth judge.

---

## The one idea that matters

**The spine is the Versioned Parameter Store + Evidence Ledger.** Every operational decision — which
persona, which pond, which lure, which spokesman, which AI **crew**, even how AI work is delegated — is a
**versioned parameter** carrying a verdict (`AMPLIFY` / `AVOID` / `testing`). Every campaign (`Cast`)
declares which version it ran; every change is backed by **evidence**. `AVOID` is sticky, so the loop never
re-proposes dead bets.

**Iron law (two-tier — D8):** only **verified owned-page conversions / closed-won** may **promote** a bet
or drive a high-blast-radius change. The watch-eye may **fine-tune the lure** via a fit-gated,
*causally-validated surrogate index* — but **raw vanity (views/likes/impressions) and off-ICP engagement
never optimize anything.** The owned-property capture click — the *bite* — is the conversion event, and it
is cryptographically attributable per placement.

---

## The 5 stages (the fishing loop)

| # | Stage | Module | What it does |
|---|-------|--------|--------------|
| 1 | **Identify fish + pond** ★ load-bearing | `persona_pond_engine` | web-generate an evidence-cited *portfolio* of personas + the concrete ponds they gather in (scored as **placement surfaces**, D21) |
| 2 | **Design the catch** | `spokesman_engine` · `hatch_scout` · `studio` | research + **draw a 2D cartoon influencer** (D22), scout a **placement brief** (what wins in this pond), then a **crew of AI agents** (the `team_config`, D19) produces content *against the brief* |
| 3 | **Watch-eye** | `watch_eye` · `expedition` | browser-native sensing — ① is the fish there? ② interested? ③ biting? — over "days at sea" |
| 4 | **Execute** | `caster` | deploy the placement, capture biters at the owned counting page (keyed per `placement_id`), qualify, build the AI dossier, hand to CRM |
| 5 | **Evolve** | `evolve_engine` · `needle` | fuse fast watch-eye + slow CRM truth; promote/kill personas, ponds, content **and crews** on a Bayesian needle vs. a blind control; maintain `do-more` + sticky `not-to-do` |

---

## Key decisions (locked)

- **Motion (D1–D2):** high-ACV, sales-led, account-based — *few right fish*. Boundary: **generate → attract → capture → qualify → research → hand off to CRM**. No closing; **no per-contact cold email**.
- **Browser-native, NO platform API (D4):** the engine senses/acts through a real browser like a human.
- **Human-of-record (D5) + disclosure (D12):** a real human owns each account; every spokesman is openly a **human-gated AI** — the gold "AI" sigil is permanent.
- **Delivery (D11):** baseline (spokesman posts as itself) → relationship (genuine replies, no pitch) → **pull-based** owned-page conversion. Paid/editorial placements exist only as **explicitly-disclosed, human-approved casts**.
- **Autonomy (D13):** ramps on evidence; *"proven" = first closed-won + no incident.*
- **Governance (D8):** watch-eye fine-tunes the lure via a causally-validated surrogate index; **only verified conversion promotes.** Vanity never optimizes anything.
- **Memory (D16):** on-box **pgvector + BGE-M3** (ARM CPU), **hybrid retrieval** (dense + BM25 + RRF + MMR).
- **Stage-1 recall (D18):** an **agy platform-swarm → codex synthesis** (recall problem, not a vote).
- **AI-influencer studio (D19):** the spokesman is an **AI influencer** produced by a **crew of role-specialized agents**; the `team_config` is a versioned, evidence-evolved parameter; media is **human-aided** (the team emits prompts, a human renders in the MAX web apps — the one on-box automation is `agy` image generation).
- **Owned counter is ground truth (D20):** a signed-token owned landing page is the verifiable conversion, replacing CRM-as-truth for the fast loop.
- **Placement Doctrine (D21):** *everything focuses on placement marketing* — venue-selection over targeting, utility-inside-context, keyed floor + causal lift, a **Brand Kit** feeding in-scene props.
- **2D cartoon spokesman (D22):** the influencer avatar is a **drawn 2D character** (disclosure-native, consistency-solvable, and itself a placement asset).

---

## Multi-AI delegation & governance (D17 + the merge gate)

The engine **dogfoods the same local 3-AI loop that designed it** — **`claude`, `codex`, `agy`** run on the
box, dispatched local-first and strength-routed via the **`cli_fanout`** engine (the `triad` skill):

- **Routing:** `agy` = web recon / long-context / **image generation**; `claude` (Opus 4.8) = review / synthesis / risk; `codex` = autonomous execution + token-efficient codegen.
- **The build pipeline is mechanically enforced:** **agy plans → codex builds → claude reviews (Opus 4.8) via a simplify-inclusive `check`**, cross-vendor at every step. A `PreToolUse` **merge gate** blocks any `git merge` unless agy + codex + claude all participated on the branch — routing is a wire, not a discipline.
- **Guardrails:** per-instance state isolation for concurrent CLIs; verify against ground truth, never blind-merge; shared `AGENTS.md`.

---

## Status — built and running

The project has moved from design to a **live, operable engine**. Phases 0–4 shipped; the full loop runs
against a simulated market on the box, gated at every merge. **~290 tests.**

**What's real, end to end:**
- **Stage 1** — persona/pond portfolio with live-web citations (agy swarm + codex synthesis).
- **Stage 2** — `spokesman_engine` researches + **draws a disclosed 2D influencer** (you approve it); `hatch_scout` produces a versioned, cited **placement brief**; the crew studio produces content *against the brief* (claims filtered to the cited corpus; per-shot video prompts).
- **Tackle Bench** — the D19 human-aided render gate: **no media + approval = no cast**.
- **Stage 3/4** — `expedition` runs "day at sea" ticks over the watch-eye pipeline; the ①②③ sonar ladder; owned-page capture keyed per `placement_id`; qualify → lead.
- **Stage 5** — a **deterministic Bayesian needle**: treatment (engine-steered crews) vs. a blind **control** ("the Drift"); `moved` requires a real credible-interval win, so it **cannot be juiced by noise** (mutation-proven: evolve-ON 0.50 → 0.75 beats control).
- **The SIM-1 Admin dashboard** — a "sonar control room" playing the whole flow as a five-station voyage (**CHART → SCOUT&RIG → BENCH → WATCH → LEDGER**), with a PLAYER game skin over a first-class OPERATOR data view. **Live:** `http://192.168.0.108:8770/admin?key=<key>` (see `DASHBOARD-README.md`).

**The honest boundary:** the whole *production* half is real (research → drawn influencer → placement brief
→ crew content → media gate → cast). The *market* half is still **simulated** — reactions come from a
MockOracle ("Training Grounds"), not a live audience. Real platforms + human-rendered video is the next
staging step.

**Next:** **SIM-2** (semi-real-world) → **go-live** (real platforms, human-of-record, MAX-app media).

---

## Running it

```bash
# tests (Postgres 16)
DATABASE_URL_TEST=postgresql:///fishing_test .venv/bin/pytest -q

# migrations
DATABASE_URL=postgresql:///fishing .venv/bin/python -m engine.migrate

# the dashboard (then open http://192.168.0.108:8770/admin?key=live)
SIM1_ADMIN_TOKEN=live DATABASE_URL=postgresql:///fishing \
  .venv/bin/python -m engine.admin_server --host 0.0.0.0 --port 8770

# headless SIM-1 smoke run
DATABASE_URL=postgresql:///fishing .venv/bin/python -m engine.run_sim1
```

**DAL contract:** functions take a `conn` and **do not commit** — the caller owns the transaction.

---

## Repo layout

```
fish/
├── README.md                      ← you are here
├── DASHBOARD-README.md            ← operator guide (click-by-click)
├── AGENTS.md                      ← single source of truth for AI agents (CLAUDE.md/GEMINI.md import it)
├── engine/                        ← the Python engine
│   ├── persona_pond_engine.py     Stage 1
│   ├── spokesman_engine.py        Stage 2 — research + draw the influencer (D22)
│   ├── hatch_scout.py             Stage 2 — the placement brief
│   ├── studio.py / studio_roles.py  Stage 2 — the crew production studio (D19)
│   ├── watch_eye.py / expedition.py Stage 3 — sensing over ticks
│   ├── caster.py                  Stage 4 — deploy + capture
│   ├── evolve_engine.py / needle.py Stage 5 — evolve + the honest needle
│   ├── admin_server.py / admin_page.py  the dashboard
│   ├── cli_dispatch.py            triad runtime door (incl. agy_image)
│   └── migrations/                plain-SQL migrations (000 → 020)
├── tests/                         pytest suite
└── docs/superpowers/specs/        the governing spec + design docs
```

---

## Explicit non-goals

- Not a CRM (we hand off; we don't rebuild pipeline/closing).
- Not a generic market-intelligence tool — research exists *only* to update fishing parameters.
- Not a vanity-metrics dashboard, not a spam/scrape cannon, not fully autonomous (human-supervised; autonomy grows).
- Not the commercial SaaS surface yet (multi-tenant-*ready*, single-tenant operated on colo first). Not B2C.

---

## The colo angle: dogfood is the pitch

Running this engine *with* colo's own AI agents is simultaneously the **revenue engine** and the **live
product proof** — every improvement to the fishing engine improves the product colo sells. The two
flywheels are one flywheel.