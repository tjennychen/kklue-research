# KKlue

**D2C Competitive Intelligence Pipeline**

Reverse-engineers any D2C brand's competitive landscape from API data, automated verification, and adversarial stress-testing. Built for the jewelry/accessories vertical but adaptable to any D2C category.

## What it does

KKlue maps brand positioning, pricing, influencer strategies, and growth engines across 13+ competitor brands. It collects structured data from Instagram, Meta Ads Library, and Reddit, then runs multi-agent adversarial debate to stress-test strategic recommendations before execution.

The pipeline was built to inform a real US market entry for a Hong Kong fine jewelry brand. Every analysis, scraper, and debate framework was created to answer specific go-to-market questions with data, not guesswork.

## Data sources

| Source | What it captures |
|---|---|
| **Instagram** (via Modash API + CDP scraping) | Influencer collaborations, post engagement, partnership types, creator demographics, repeated collaborator patterns |
| **Reddit** | Consumer sentiment, brand perception, purchase decision drivers, tarnish/quality complaints, community recommendations |
| **Meta Ads Library** | Competitor ad creative, spend patterns, targeting signals |

## Pipeline stages

### 1. Discovery
Identify competitor brands, map their positioning, pricing, hero products, and estimated revenue. 13 brands analyzed across demi-fine, accessible fine, and true fine jewelry tiers.

### 2. Data collection
- **Modash data pull**: Top 100 collaborators + mid-tier (100-1000 likes) posts per brand. 12,000+ posts across 13 competitor programs collected as structured JSON.
- **CDP verification scrapers**: Raw Chrome DevTools Protocol scripts (Python + JS) connect to a running Chrome instance, navigate Instagram posts, intercept API responses for captions, detect brand mentions, capture screenshots of carousel slides. Used to verify whether "collaborators" actually mention the brand or are false positives.
- **Profile scraping**: Automated bio + header screenshot capture for top influencer candidates.
- **Reddit/community research**: Indexed consumer threads on purchase behavior, brand trust, material education, and competitive perception.

### 3. Analysis
Per-competitor Modash analysis reports that decompose each brand's influencer program:
- Partnership type breakdown (paid vs gifted vs affiliate vs ambassador)
- Hidden engine identification (the single creator cluster driving disproportionate engagement)
- AAPI creator representation audit (zero of 13 competitors had a systematic AAPI program)
- Repeated collaborator detection and verification
- Cross-competitor synthesis with creator archetype mapping

### 4. Adversarial stress-testing
A 7-persona debate framework that pressure-tests strategic recommendations from every angle. Personas include target customers (Asian-American tastemaker, practical mom, brand insider), a competing brand CMO, a Reddit skeptic, an operations lead, and a VC investor. Each persona holds genuine stakes and genuine skepticism.

The debate surfaces real tensions (brand translation risk, price sensitivity, cultural authenticity) before they surface in the market.

## Key scripts

| File | Purpose |
|---|---|
| `scrape-mejuri-repeated.js` | Playwright-based collaborator verification: intercepts Instagram API for captions, screenshots posts/carousels, outputs CSV |
| `scrape-top10.py` | Raw CDP scraper for top 10 repeated collaborators with carousel slide navigation |
| `scrape-profiles.py` | CDP profile scraper: bio extraction + header screenshots for influencer candidates |
| `export-pdf.cjs` | Exports HTML slide deck to PDF via Playwright + Ghostscript merge |
| `test-cdp.py` / `test-single-post.js` | CDP and Playwright test harnesses for single-post scraping |

## Repo structure

```
modash-data/           Structured JSON: collaborators, top posts, mid-tier posts for 13 brands
Cometitor research/    Per-brand Modash analysis reports + cross-competitor synthesis
mejuri-verified/       Verification screenshots + CSV for repeated collaborator audit
kk-images/             Brand campaign and product images
research_*.md          Deep research: competitors, Reddit insights, influencer strategy, GTM
debate_framework_*.md  Multi-persona adversarial debate structure
kklue-gtm-deck-*.html  GTM presentation deck (EN + ZH)
```

## Seeding Ninja (spinoff)

KOC (Key Opinion Consumer) seeding pattern detection. Identifies which competitor influencer programs are running undisclosed gifting at scale by analyzing the gap between "unspecified" partnership posts and actual engagement patterns. Gorjana's "unspecified" posts generate more total likes (103K) than paid (30K), gifted (29K), and affiliate (24K) combined. That pattern is a seeding program.

## Built with

- Playwright (browser automation + CDP connection)
- Raw Chrome DevTools Protocol (websockets + JSON-RPC for Instagram scraping)
- Modash API (influencer discovery and collaboration data)
- Node.js + Python

---

Built by [Jenny Chen](https://linkedin.com/in/tjennychen)
