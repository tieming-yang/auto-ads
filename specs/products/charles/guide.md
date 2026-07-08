# DEEPWATER — SIM-1 Dashboard Operator Guide

A step-by-step, click-by-click guide to running the AI lead-generation engine from the dashboard.
You are the **Captain**: the engine does the fishing, you make the judgment calls at each station.

---

## 0. Start & open the dashboard

**Start the server** (on the box, ARM-FISHER — leave it running):

```bash
SIM1_ADMIN_TOKEN=live DATABASE_URL=postgresql:///fishing \
  .venv/bin/python -m engine.admin_server --host 0.0.0.0 --port 8770
```

**Open it** from your laptop's browser:

```
http://192.168.0.108:8770/admin?key=live
```

- Click the **⚔ PLAYER / 📊 OPERATOR** toggle (top-right) into **PLAYER** mode.
- You'll see five station tabs across the top — the fishing expedition, left to right:

> **⚓ CHART → 🪝 SCOUT&RIG → 🔧 BENCH → 👁 WATCH → 📜 LEDGER**

> **Shortcut:** clicking **Seed Starter Session** (top-right) auto-fills a ready product + persona + 2 crews so you can skip Station 1's manual setup. The steps below are the manual path so you learn each field.

Do the stations in order.

---

## ⚓ STATION 1 — CHART  *(click the CHART tab)*

### Set the product — the "CAST" panel at the top
- **1-1** — In **Product / Service** (placeholder *"set product/service to begin"*), type your product name. *Example:* `PulseCheck`
- **1-2** — In **Value Prop** (*"what the lure promises"*), type the promise. *Example:* `Know if your offer lands before you scale — a browser-native reaction test.`
- **1-3** — *(Optional)* **Notes** — an operator note, e.g. `first live test`.
- **1-4** — *(Optional — Brand Kit, skip for a first run)* Tagline / Slogan / Logo Description / Brand Colors / Prop Preferences / Logo Upload. Fill these later when you want your logo appearing *inside* the content as an in-scene prop.
- **1-5** — Click **Save Cast**. (The "set product/service to begin" warning disappears.)

### Add the fish — the "Personas" panel
- **1-6** — Under **Personas**, click the **+** button. A new persona card appears.
- **1-7** — In **Hypothesis**, type who you're fishing for. *Example:* `Solo founders who launch offers but can't tell early which ones will convert.`
- **1-8** — In **Pains JSON**, type a JSON list. *Example:* `["guessing which offer works", "wasting spend scaling duds"]`
- **1-9** — Set **Pain Acuteness** and **Deal Fit** (0–1). *Example:* `0.8` and `0.7`.
- **1-10** — Click **Save Persona**.

### Commission the influencer — still on the persona card
- **1-11** — Click **Research Influencer**. Wait ~1–2 min: the engine researches who this fish would love, writes an identity + voice, and **draws a 2D character**.
- **1-12** — Scroll to the **spokesman character** card — the drawn portrait + model sheet. Your options:
  - **APPROVE** (lock the influencer in) · **REVISE** (edit the JSON, then **Save Spokesman**) · **REJECT** · **Regenerate reference** (redraw the face).
- **1-13** — Click **APPROVE**. You now have a live, openly-disclosed AI influencer with a face.

---

## 🪝 STATION 2 — SCOUT&RIG  *(click the SCOUT&RIG tab)*

### Read the water
- **2-1** — Under **Hatch Briefs**, find your persona's brief (shows a **STALE** badge on first use). Click **Re-scout**. Wait ~30–60 sec: the engine researches what content actually wins in this pond (cited exemplars, native format, truthful claims). *This is the reference the crews produce against.*

### Set your crews
- **2-2** — Under **Crews** you already have `codex-direct` + `claude-direct` from the seed. To add one: click **Add crew**, set **Name** and **Config JSON** (e.g. `{"roles":[{"role":"brain","brain":"claude"}]}`), click **Save Crew**. Keep **at least 2** crews — one becomes *treatment*, one *control*.

### Produce
- **2-3** — Click **⚔ LAUNCH SORTIE**. Wait ~1–3 min: each crew generates real placement content against the brief. Watch the batch status update.

---

## 🔧 STATION 3 — BENCH  *(click the BENCH tab)*

- **3-1** — Each lure shows its **prompt cards**: a **picture prompt** + **per-shot video prompt** (when the crew has a Generator role). Copy a prompt.
- **3-2** — Render it in your MAX app (the **Veo / Imagen** links are on the card), download the result.
- **3-3** — Click **attach** on that lure and give it the file/note. *(For a brain-only text placement, attach a thumbnail note to satisfy the gate.)*
- **3-4** — Click **approve** on the lure.
- **3-5** — Once every lure has media + approval, click **Cast Ready**. Your content is cast into the pond as **treatment vs control**.

> ⚠️ **The gate is deliberate: no media + approval = no cast.** This is the D19 human quality checkpoint — the Captain ties the lure.

---

## 👁 STATION 4 — WATCH  *(click the WATCH tab)*

- **4-1** — Click **⏱ Day at Sea** to advance the market. Repeat a few times.
- **4-2** — Watch each pond's ladder climb: **QUIET → ① PINGS (they're there) → ② WAKES (interested — off-ICP shows red, a *negative*) → ③ STRIKES (biting)**.
- **4-3** — When a **CATCH ON DECK** appears, read its dossier and click **Qualify** (keep it → goes to your CRM) or **Throw Back**.

> 🔴 **Honest heads-up:** on a *real* round today the sonar stays **QUIET** — there is no live audience yet (that's go-live). **To actually see reactions and the needle move, use ⚓ TRAINING GROUNDS** (a button on SCOUT&RIG) instead of a real cast — a MockOracle plays the market. Run it a few rounds.

---

## 📜 STATION 5 — LEDGER  *(click the LEDGER tab)*

- **5-1** — Read **THE DRIFT boss bar**: your **treatment** crews vs. your blind **control** (the version of you that ignores feedback), with a **confidence band**. It only shows a win when the evidence is real — it will **not** move on a couple of noisy reactions.
- **5-2** — Click **AFTER-ACTION REPORT** to ingest reactions + evolve (amplify winners, prune losers).
- **5-3** — When a crew earns promotion, a **Commander's Seal** prompt appears — *you* approve it (the evidence is shown). Nothing self-approves.
- **5-4** — Watch the **two clocks**: *"the fast eye (days)"* vs *"CRM truth (season)"*. A bet only becomes **PROVEN** on a real closed-won.

---

## The shortest loop to feel it work right now

1. CHART: steps **1-1 → 1-13** (or just click **Seed Starter Session**).
2. SCOUT&RIG: click **⚓ TRAINING GROUNDS — practice round** a few times.
3. LEDGER: watch the boss bar / needle respond.

---

## Good to know

- **PLAYER vs OPERATOR** — same data, two skins. PLAYER = the game view; **OPERATOR** = the dense numbers table (every game element is one hover from the raw DB row).
- **TRAINING vs real** — anything labeled **TRAINING** is practice against a simulated market; it never touches your real evidence or the needle. Real rounds use real content + real reactions (and today have no live market, so the WATCH is quiet — see the WATCH heads-up).
- **The needle never lies** — it uses a Bayesian confidence gate and refuses to call a win on thin/noisy data. To watch it climb you need repeated rounds with a genuine signal.
- **New Session** = a deliberate clean slate (fresh workspace). Otherwise your work **persists across server restarts** (boot reuses your most-recently-active workspace).
- **The influencer is openly AI** — the gold **"AI"** disclosure sigil is permanent and is never replaced by the character. This is by design (disclosed, human-gated AI).
- **Where the engine is today** — the whole production pipeline (research → drawn influencer → placement brief → crew content → media gate → cast) is real. The *market* half is still simulated (SIM). Real platforms + human-rendered video is the next staging step (SIM-2 → go-live).

---

## Troubleshooting

- **Page won't load / 401** — the server must be running (see §0); the URL must include `?key=<your token>`. With `SIM1_ADMIN_TOKEN=live` the key is `live`; otherwise read the key the server prints at startup.
- **"set product/service first" on Emit** — you haven't saved a product yet (step 1-5) or added a persona/crew.
- **Emit did nothing / 0 casts** — you need a saved product + at least one persona + crews; or a lure is still pending on the BENCH (needs media + approval + **Cast Ready**).
- **Port 8770 in use** — another server is running; free it (`fuser -k 8770/tcp`) or start on another port with `--port`.