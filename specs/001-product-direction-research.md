# Auto-Ads Product Direction Research

## 0. Working Title

**Auto-Ads: AI Market Source Finder + Campaign Pack Generator**

Alternative names:

- FishPool AI
- AudienceMap AI
- MarketRadar
- AdSource AI
- GrowthMap AI
- PromoPilot
- AutoTraffic

**Best internal name for now:** Auto-Ads

**Best product description:**

> Auto-Ads helps founders, small businesses, creators, and small agencies find where their customers gather online, discover what topics they care about, and generate TikTok/Instagram-ready promotion assets from that strategy.

---

## 1. Context

Charles’s core point:

> Every product needs promotion. If we keep building products but nobody knows about them, there is no revenue. If there is no revenue, the business dies.

This is the real business problem.

The problem is not only:

> Can AI write ad copy?

The deeper problem is:

> How do we know who to target, where to reach them, what they care about, and what content/ad angle has the highest chance of working?

Charles is essentially describing a **distribution intelligence product**.

---

## 2. Important Alignment Correction

**MVP = Minimum Viable Product**

Meaning:

> The smallest usable product that can validate whether customers actually want the solution.

This matters because the team should not build a large AI marketing platform first. The first goal is to validate one painful workflow.

The MVP should not be:

> AI automatically does all marketing.

The MVP should be:

> Given a business, find the best customer source and produce a focused promotion plan.

---

## 3. Requirement Digest from Charles

### 3.1 Charles’s Main Requirements

| Charles’s statement | Product interpretation |
|---|---|
| Any product needs advertising | Distribution is part of product success |
| Building 100 products with no users means bankruptcy | Product development without acquisition is not a business |
| Need a promotion/traffic product | Build a tool that helps users get attention and leads |
| First step: find specific market hot topics | The product must start with market research |
| Imagine who the customers are | The product must define ICP/customer segments |
| Find what sites/channels/content they consume | The product must map customer gathering places |
| Add prompts, assumptions, constraints | The AI workflow must be structured, not freeform |
| Add “Murder Board” | The AI must challenge weak assumptions before output |
| Precision targeting is like fishing: first find the fish | The product’s core value is audience-source discovery |

### 3.2 Charles’s Real Product Thesis

Charles is not describing a simple AI copywriting app.

He is describing:

> An AI system that helps a business find the right customer group, the right online gathering places, the right topics, and then generate a marketing plan.

This is stronger than a normal **AI ad generator**.

---

## 4. Market Evidence

The market is large enough to justify exploration. IAB reported that US digital advertising revenue reached **$294.6B in 2025**, with social advertising at **$117.7B** and digital video at **$78B**. IAB also says growth is shifting toward performance, video, creator-led content, commerce integration, and AI-supported workflows.

Creator-led advertising is also now a major channel. IAB projected US creator ad spend at **$37B in 2025**, up **26% year over year**, and nearly **4x faster than the broader media industry**. IAB also says nearly half of creator ad buyers consider creators a **must buy**.

Small businesses already feel marketing uncertainty. Constant Contact’s 2025 small business marketing report found that only **18% of SMBs feel very confident in their marketing**, down from **27% in 2024**. It also found that **23%** say their top frustration is not knowing what drives results, and **41%** struggle to get people to open or click.

AI adoption is no longer too early. The US Chamber reported that **58% of small businesses use generative AI**, up from **40% in 2024** and **23% in 2023**. Salesforce also reports that **78% of SMB leaders** say investing in AI will be a game-changer, and **90%** believe AI will make operations more efficient.

TikTok itself recommends platform-native creative, hooks within the first seconds, multiple creatives, continuous testing, and maintaining a creative library to handle fatigue. TikTok recommends **3–5 creatives per ad group** and **3–5 diversified ad groups per campaign** as a starting structure.

**Conclusion:**

> There is a real market, but the winning product should not be “AI writes ads.” The better product is “AI finds the customer source and turns it into campaign assets.”

---

## 5. Core User Pain

### 5.1 Yang’s Pain

Yang’s pain is explicit in the chat:

> I have development experience, but I do not have product/marketing experience. I do not know which pain points are real, which are fake, and which users will actually pay.

This is likely the same pain felt by many technical founders and small business owners.

They can build, but they cannot reliably answer:

- Who exactly is my customer?
- Where do these customers gather online?
- What topics do they already care about?
- Which channels are worth testing?
- What ad angle should I use?
- What content should I make first?
- What should I avoid wasting time on?

This is the real opportunity.

### 5.2 Charles’s Pain

Charles’s pain is more business-oriented:

> We cannot keep building things without traffic and revenue.

His mental model is:

```txt
Product → Customer source → Attention → Promotion → Conversion → Revenue
```

He wants the AI to help find the **source of customers**, not just produce pretty ad text.

### 5.3 Small Business Pain

Small businesses often do marketing activity without confidence. Constant Contact’s report says marketing effort and investment are up, but confidence is falling; many businesses lack clear insight into what is working.

This supports Charles’s point: the issue is not lack of tools. The issue is **lack of direction**.

---

## 6. Product Reframe

Previous idea:

> AI ad copy/image assistant for TikTok and Instagram.

Better idea after digesting Charles:

> AI customer-source discovery and promotion-planning assistant, with TikTok/Instagram creative generation as one output.

Important distinction:

> The product should not assume TikTok and Instagram are always correct.

For example, Charles said:

> If you sell eggs, YouTube ads may be weak.

Product implication:

> Auto-Ads should first decide whether TikTok/Instagram are suitable for the business. If they are not, the product should say so.

This is a better product because it earns user trust.

---

## 7. Recommended MVP

### 7.1 MVP One-Liner

> Enter your business. Auto-Ads finds your best customer groups, where they gather online, what topics they care about, and generates a focused TikTok/Instagram promotion pack if those channels fit.

### 7.2 MVP Promise

> Stop guessing where to promote. Find your customer fish pool first.

### 7.3 MVP Output

The MVP should generate one **Market Source Report** and one **Campaign Pack**.

#### Market Source Report

Includes:

1. Best customer segments
2. Customer pain/desire map
3. Where they gather online
4. Websites, communities, channels, hashtags, creators, and content formats
5. Top 50 topics/trends/questions for that market
6. Competitor promotion examples
7. Channel-fit score
8. TikTok/Instagram suitability score
9. Recommended first campaign direction
10. Murder Board critique

#### Campaign Pack

Includes:

1. 10 campaign angles
2. 30 hooks
3. 10 captions
4. 10 CTA options
5. 5 image prompt directions
6. 5 TikTok/Reels short script outlines
7. 3 Instagram carousel outlines
8. 1 manual testing plan
9. Export as Markdown/CSV/ZIP

---

## 8. The MVP Should Be Strategy-First, Not Creative-First

Most AI ad tools start here:

```txt
User enters product → AI generates ad copy/images
```

Auto-Ads should start here:

```txt
User enters business → AI finds customer source → AI identifies topics → AI critiques assumptions → AI generates campaign assets
```

This is a better wedge because generic AI copy is already commoditized. The value is in the structured workflow.

---

## 9. First-Step Product Flow

### Step 1: Business Intake

Ask the user:

- What do you sell?
- Who do you think buys it?
- Where do you sell it?
- Is it local, national, or online?
- What is the price?
- What is the main customer pain?
- What is the main benefit?
- What type of customer has urgency?
- Are you B2B, B2C, creator, local service, e-commerce, or agency?
- What channels have you tried?
- What result do you want: leads, sales, traffic, awareness, followers?

### Step 2: AI Builds Customer Hypotheses

Example output:

| Segment | Pain | Buying intent | Reachability | Notes |
|---|---|---:|---:|---|
| Shopify sellers | Need more product sales | High | High | Good for TikTok/Instagram ads |
| Local restaurants | Need foot traffic | Medium | Medium | Needs local targeting |
| Server hosting buyers | Need reliable infrastructure | High | Medium | TikTok may be weak; search/forums may be stronger |
| Small agencies | Need fast client deliverables | High | High | Strong SaaS willingness to pay |

### Step 3: Find Gathering Places

The product should search for:

- TikTok trends
- Instagram creators/pages
- Reddit communities
- YouTube channels
- Google search topics
- Google Trends
- Meta Ad Library competitors
- TikTok Creative Center competitors
- Blogs/forums/newsletters
- Discord/Slack communities, where discoverable
- Marketplaces and review sites
- Comment sections and FAQs

TikTok Creative Center is useful because it exposes top ads, trends, and creative triggers. TikTok’s Creative Center explicitly positions Top Ads as a way to analyze successful campaigns and understand creative triggers. Google Trends is useful for search interest and “what the world is searching for right now.” Meta Ad Library is useful because it lets users search ads currently running across Meta technologies by keyword or advertiser.

### Step 4: Generate Top 50 Topics

The topics should be ranked by:

- Relevance
- Urgency
- Buyer intent
- Content potential
- Trend momentum
- Competition level
- Channel fit
- Ease of creating content
- Risk level
- Confidence score

### Step 5: Murder Board

The Murder Board should attack the AI’s own plan.

A murder board is a critical review process used to scrutinize proposals and identify weaknesses before moving forward.

For Auto-Ads, the Murder Board should ask:

- Are these customers real buyers or just viewers?
- Is this channel actually where they make purchase decisions?
- Are we confusing popularity with buyer intent?
- Are TikTok/Instagram suitable for this business?
- Is the user likely to afford paid ads?
- Is the topic too broad?
- Is the audience too vague?
- Are there legal or platform-policy risks?
- Are we recommending what is trendy or what converts?
- What data is missing?
- What assumption could kill this campaign?

This feature is important because Charles specifically warned that without constraints and review, AI output becomes too broad and useless.

### Step 6: Generate Campaign Pack

Only after the strategy passes the Murder Board should Auto-Ads generate:

- TikTok hooks
- Instagram captions
- Reels scripts
- Image prompts
- Carousel outlines
- CTA variants
- Testing plan

---

## 10. MVP Scope

### Build in MVP

| Feature | Priority | Reason |
|---|---:|---|
| Business intake form | P0 | Needed for structured output |
| Customer segment generator | P0 | Core value |
| Gathering-place finder | P0 | Charles’s main requirement |
| Topic finder | P0 | Turns research into action |
| Channel-fit scoring | P0 | Prevents wrong-channel recommendations |
| Murder Board critique | P0 | Prevents hallucinated strategy |
| TikTok/Instagram campaign pack | P1 | Turns strategy into assets |
| Export to Markdown/CSV | P1 | Lightweight, useful |
| Saved projects | P1 | Users need to revisit research |
| Basic image prompt generation | P2 | Useful but not core |
| AI image generation | P2 | Nice, but cost/risk higher |

### Do Not Build in MVP

Do not build these first:

- Direct TikTok/Instagram posting
- Direct Meta/TikTok Ads API campaign launch
- Budget optimization
- Full analytics dashboard
- Social scheduler
- Influencer marketplace
- Full video editor
- Auto media buyer
- Full brand management suite

Reason:

> Charles’s requirement is first about finding customer sources. Do not waste engineering effort on platform integrations before validating that users want the strategy workflow.

---

## 11. Is Connecting to TikTok/Instagram Hard?

### Short Answer

Yes, but not impossible.

It is technically possible, but it is not the right MVP priority.

TikTok’s API for Business supports Marketing API functions such as campaign management, creative material management, reporting, audience uploads, and automated optimization. TikTok also has a Content Posting API that supports direct posting or uploading drafts from an app to TikTok, but direct posting requires scopes, approval, authorization, and audit conditions.

Meta’s Marketing API can manage ads, but the `ads_management` permission and app review/access requirements create friction.

### MVP Recommendation

Do not connect first.

Start with:

- Export to Markdown
- Export to CSV
- Copy-to-clipboard
- Download image/copy pack
- Manual upload to TikTok/Instagram/Ads Manager

Add integrations later only after users repeatedly export and use campaign packs.

---

## 12. Individual User Group Assessment

### 12.1 Technical Founders / Indie Hackers

#### Pain

They can build products but struggle with positioning, audience discovery, and distribution.

#### Fit

Very high.

Yang is in this category, so the team can dogfood the product.

#### What They Need

- Who is my customer?
- Where do they hang out?
- What content should I make?
- Is TikTok/Instagram even worth using?
- What are the first 10 promotion experiments?

#### MVP Angle

> Find your first 100 users before building more features.

#### Verdict

Strong internal test group. Good for early validation.

---

### 12.2 Small E-Commerce Sellers

#### Pain

They need constant product promotion and creative testing.

#### Fit

Very high.

They have structured input: product URL, product photos, reviews, competitors, price, offer.

#### What They Need

- Product URL → audience map
- Competitor ad examples
- TikTok/Instagram angle ideas
- Product hooks
- Visual prompts
- Testing plan

#### Verdict

Best commercial wedge.

---

### 12.3 Local Small Businesses

#### Pain

They need local customers but often do not know where attention comes from.

#### Fit

Medium.

They have real pain, but may need more education and have lower SaaS willingness to pay.

#### What They Need

- Local customer source map
- Local event/topic finder
- Weekly promotion ideas
- Instagram Story/Reels pack
- Local ad copy

#### Verdict

Good later vertical. Not first unless choosing one niche, such as salons, gyms, clinics, or restaurants.

---

### 12.4 KOLs / Influencers

#### Pain

They need to monetize audience without sounding fake.

#### Fit

Medium.

They may not buy ads directly, but they need sponsor content and affiliate promotion.

#### What They Need

- Sponsor content angles
- Audience-brand fit
- Affiliate campaign ideas
- Personal brand voice
- FTC-safe disclosure reminders

#### Verdict

Useful later. Not the best first MVP unless targeting monetized creators.

---

### 12.5 YouTubers

#### Pain

They need to repurpose long-form content into short-form promotional content.

#### Fit

Medium.

If the MVP only does copy/images, YouTubers may feel the product is incomplete because they expect video clipping.

#### What They Need

- Video transcript → TikTok/Reels hooks
- Thumbnail/title testing
- Sponsor script
- Course/merch promotion
- Instagram carousel from video

#### Verdict

Good later if video repurposing is added.

---

### 12.6 Small Agencies / Freelancers

#### Pain

They need to research markets and produce campaign ideas repeatedly for clients.

#### Fit

Very high.

They have higher willingness to pay and repeated usage.

#### What They Need

- Client workspace
- Business research report
- Customer source map
- Campaign strategy
- Creative pack
- Client-ready export

#### Verdict

Best paid user group after e-commerce sellers.

---

## 13. Recommended Beachhead

The best initial wedge:

> Technical founders, small e-commerce sellers, and small agencies who need to quickly find customer sources and generate TikTok/Instagram promotion packs.

Why not “everyone”?

> Because “everyone who needs ads” is too broad.

Best MVP validation segment:

> Founders/small businesses who already have a product but do not know where to promote it.

This directly matches Charles’s problem.

---

## 14. Product Positioning

Bad positioning:

> AI ad generator.

Better positioning:

> AI market-source finder for founders and small businesses.

Best positioning:

> Find where your customers gather, then generate the ads to reach them.

Possible landing page headline:

> Stop guessing where to promote your product.

Subheadline:

> Auto-Ads finds your best customer groups, the online places they gather, the topics they care about, and turns the strategy into TikTok/Instagram campaign assets.

CTA:

> Generate My Market Source Report

---

## 15. Core Differentiation

Competitors can generate copy and images.

Auto-Ads should differentiate through:

1. Customer-source discovery
2. Channel-fit scoring
3. Topic ranking
4. Murder Board critique
5. Strategy-to-creative workflow
6. Exportable campaign packs
7. Validation-first MVP mindset

The core product is not the generated ad.

The core product is:

> Reducing the user’s uncertainty before they spend time or money on marketing.

---

## 16. MVP User Stories

### Founder

> As a founder, I want to enter my product idea and get the top customer segments, so I can stop guessing who to target.

### Small Business Owner

> As a small business owner, I want to know where my customers spend time online, so I can promote in the right place.

### E-Commerce Seller

> As a seller, I want to turn my product page into customer segments, topics, and campaign angles, so I can create ads faster.

### Agency

> As an agency, I want to generate a client-ready market source report, so I can save research time and produce better strategy.

### Yang

> As a developer with limited marketing experience, I want AI to guide my product promotion strategy, challenge bad assumptions, and generate first campaign assets.

---

## 17. MVP Data Inputs

### Minimum Inputs

- Business name
- Business description
- Product/service URL
- Country/market
- Local or online
- Price range
- Target user guess
- Main problem solved
- Current channels tried
- Competitors
- Desired outcome

### Optional Inputs

- Product images
- Customer reviews
- Existing landing page
- Existing social profiles
- Existing ads
- Founder notes
- Sales objections
- Brand tone

---

## 18. MVP Data Sources

Start simple. Do not overbuild.

Useful sources:

- General web search
- Google Trends
- TikTok Creative Center
- Meta Ad Library
- Reddit search
- YouTube search
- Competitor websites
- Product reviews
- Public social profiles
- User-provided URLs

Avoid scraping risky private data. Use public sources, official APIs where possible, and manual user-provided data.

---

## 19. MVP Output Template

Each generated report should have this structure:

```md
# Market Source Report

## 1. Business Summary

## 2. Best Customer Segments

## 3. Customer Pain / Desire Map

## 4. Where Customers Gather

## 5. Top 50 Topics

## 6. Competitor / Reference Signals

## 7. TikTok Fit Score

## 8. Instagram Fit Score

## 9. Recommended First Campaign

## 10. Murder Board Critique

## 11. Final Recommended Action Plan

## 12. TikTok / Instagram Campaign Pack
```

---

## 20. Scoring Model

Use simple scoring first.

### Customer Segment Score

Score each segment from **1–5**:

- Pain urgency
- Willingness to pay
- Reachability
- Channel concentration
- Content availability
- Competition intensity
- Conversion path clarity

### Channel Fit Score

Score each channel from **1–5**:

- Does the audience gather here?
- Are they open to this product category here?
- Can the product be explained visually?
- Are competitors already active?
- Is there buying intent?
- Can we produce content cheaply?
- Is the channel suitable for the user’s budget?

### Topic Score

Score each topic from **1–5**:

- Relevance
- Search/social momentum
- Buyer intent
- Emotional pull
- Content format fit
- Competition
- Risk

The MVP does not need a perfect algorithm. It needs a consistent framework.

---

## 21. Example: Charles’s Server Hosting Case

Input:

> We provide server hosting.

The product should not immediately generate Instagram captions.

It should first ask:

- What type of hosting?
- Physical server colocation?
- VPS?
- GPU server?
- Game server?
- Enterprise hosting?
- Local data center?
- Managed hosting?
- US only?
- Price range?
- Who is the buyer?

Then it should output possible customer groups:

| Segment | Possible need | Likely channels |
|---|---|---|
| Indie hackers | Need affordable deployment | Reddit, Hacker News, X, YouTube, search |
| Game server owners | Need low-latency hosting | Discord, Reddit, YouTube, TikTok possible |
| Agencies | Need reliable client hosting | Google search, LinkedIn, referrals |
| AI builders | Need GPU/compute | X, Reddit, Discord, technical forums |
| Local businesses | Need managed web hosting | Google search, local SEO, referrals |

Then the Murder Board should challenge:

- Is TikTok actually a buyer channel for server hosting?
- Is search intent stronger than social attention?
- Are customers technical or non-technical?
- Is location important?
- Is pricing competitive?
- Is trust/security more important than viral reach?

This is exactly what Charles means by **find the fish first**.

---

## 22. Engineering Direction

### Recommended Stack

Given Yang’s skill set:

- Next.js
- TypeScript
- TailwindCSS
- Supabase or Neon Postgres
- Supabase Storage / Cloudflare R2
- Background jobs with Inngest or Trigger.dev
- Stripe for payments
- LLM provider abstraction
- Image generation provider abstraction
- Export to Markdown/CSV/ZIP

### Core Tables

```txt
users
workspaces
projects
business_profiles
customer_segments
customer_sources
topics
competitors
channel_scores
murder_board_reviews
campaigns
creative_variants
exports
usage_credits
```

### Core Services

```txt
business-intake-service
market-research-service
source-discovery-service
topic-ranking-service
channel-fit-service
murder-board-service
campaign-generator-service
export-service
usage-billing-service
```

### System Design

The AI pipeline:

1. Normalize user input
2. Generate customer hypotheses
3. Search public sources
4. Extract sources/topics
5. Rank customer segments
6. Rank channels
7. Run Murder Board critique
8. Generate final report
9. Generate campaign pack
10. Export assets

---

## 23. MVP Pricing

Use subscription + usage credits.

### Suggested Pricing

| Plan | Price | Target |
|---|---:|---|
| Free | $0 | 1 limited report |
| Starter | $19–29/mo | Solo founder / creator |
| Growth | $49–79/mo | E-commerce / small business |
| Agency | $149–299/mo | Freelancers / small agencies |
| Extra credits | Usage-based | More reports/images |

Charge around the report, not just generations.

Better value unit:

> Market Source Report + Campaign Pack

Not:

> 1 AI generation

---

## 24. Validation Plan

### Week 1: Concierge MVP

Do not build full SaaS first.

Create a manual workflow:

1. User submits business info through form.
2. Yang runs the research manually with AI assistance.
3. Deliver a Market Source Report.
4. Ask whether they would pay.
5. Track which parts they actually use.

### Week 2: Semi-Automated Prototype

Build:

- Intake form
- AI-generated report
- Manual review
- Export to Markdown/PDF
- Stripe payment or waitlist

### Week 3–4: Real MVP

Build:

- User login
- Project dashboard
- Report generation
- Campaign pack generation
- Export
- Usage credits

### Validation Questions

Ask users:

- Did this reveal a customer group you had not considered?
- Did this reveal a channel you did not know about?
- Did this save research time?
- Would you use this before launching a product?
- Would you pay $29/month?
- Which output was useless?
- Which output would you actually act on this week?

---

## 25. Success Metrics

### Activation

- User creates first business profile
- User generates first Market Source Report
- User exports report

### Value

- User saves report
- User uses recommended topics
- User exports campaign pack
- User returns for another business/project

### Business

- Free-to-paid conversion
- Reports generated per user
- Cost per report
- Monthly recurring revenue
- Churn
- Agency plan conversion

Most important MVP metric:

> Number of reports exported and acted on.

Not:

> Number of AI generations.

---

## 26. Major Risks

### Risk 1: Output Is Too Generic

Mitigation:

- Force structured intake
- Use real public sources
- Require channel-fit scoring
- Use Murder Board critique

### Risk 2: Users Want Automation, Not Reports

Mitigation:

- Report must end with concrete campaign assets
- Do not stop at analysis

### Risk 3: TikTok/Instagram Are Wrong Channels for Some Businesses

Mitigation:

- Product should say “not recommended” when channel fit is weak

### Risk 4: Research Data Is Weak or Hallucinated

Mitigation:

- Cite sources internally
- Mark confidence levels
- Separate fact from assumption
- Add Murder Board review

### Risk 5: Competitors Copy Ad Generation

Mitigation:

- Compete on strategy workflow, not copy generation

---

## 27. Final Recommendation

Build this MVP:

```txt
Business input → Customer source map → Top topics → Murder Board → TikTok/Instagram campaign pack
```

Do not start with:

> AI image/copy generator.

Do not start with:

> Connect to TikTok/Instagram Ads API.

Start with the painful first step Charles described:

> Find the fish pool.

Then generate ads only after the system knows:

- Who the fish are
- Where they gather
- What bait they respond to
- Which channel is worth testing
- Which assumptions might be wrong

This is the strongest product direction because it combines:

- Charles’s business instinct
- Yang’s engineering ability
- Real SMB marketing uncertainty
- AI’s strength in research/synthesis/generation
- A lightweight MVP scope

The product should be positioned as:

> An AI distribution research assistant for small teams that turns business context into customer-source maps and campaign-ready assets.
