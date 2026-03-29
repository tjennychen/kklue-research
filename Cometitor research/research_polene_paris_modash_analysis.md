# Polene Paris Influencer Strategy: Modash Data Analysis
**Date:** 2026-03-29
**Source:** polene_paris-top100.json (100 raw entries), polene_paris-midtier-100-1000likes.json (565 entries)
**After deduplication:** 653 unique posts from 495 unique creators
**Framework:** research_influencer_dtc_best_practices.md

---

## Program Scale

- 1,471 unique creators across 2,000 posts in collaborators.json (API cap hit)
- Date range: Aug 2025 to Mar 2026 (roughly 8 months)
- That's about 1.36 posts per creator. Mostly one-and-done relationships.
- A handful of repeat posters signal active affiliates (see section below)
- Note: the 2,000 post cap means total program size is likely larger. Actual creator count is probably 2,000+.

---

## Partnership Type Breakdown

| Type | Posts | % | Median Likes | Avg Likes | Total Likes | % of Likes |
|---|---|---|---|---|---|---|
| Paid | 82 | 12.6% | 487 | 21,290 | 1,745,802 | 42.1% |
| Unspecified | 250 | 38.3% | 406 | 5,902 | 1,475,620 | 35.6% |
| Gifted | 178 | 27.3% | 365 | 3,100 | 551,775 | 13.3% |
| Affiliate | 131 | 20.1% | 308 | 2,339 | 306,440 | 7.4% |
| Ambassador | 12 | 1.8% | 313 | 5,886 | 70,634 | 1.7% |

**Key read:** Paid posts are 12.6% of all posts but 42.1% of all likes. That's deceptive. Three Korean macro influencers (@page.soobin, @min.nicha, @fallingin__fall) alone account for 1.44M likes (34.7% of total). Strip those three out and Paid median drops to 481 likes. Not special.

**Unspecified is the bulk of the program.** 250 posts, 35.6% of total likes. Median 406 likes. These are undisclosed organic-looking mentions running at scale.

**Affiliate is the largest disclosed segment by count (131 posts) but the worst performer per post.** Median 308 likes. It's a volume play, not a quality play.

---

## Disclosure Compliance

- **Properly disclosed: 104 posts (15.9%)**
- **Likely hidden sponsorship: 501 posts (76.7%)**
- **Unclear/other: 48 posts (7.4%)**

77% of this program is undisclosed. That includes most of the gifted, all of the "unspecified," and a good chunk of the affiliates. Polene is a French luxury brand running an almost entirely non-compliant influencer program by US/EU FTC standards. The small properly-disclosed slice is mostly their macro paid partnerships (German "Werbung," Korean "#광고," French "publicité").

---

## Post Performance Distribution

| Likes Range | Posts | % |
|---|---|---|
| Under 500 | 408 | 34.0% |
| 500-1K | 159 | 13.2% |
| 1K-5K | 454 | 37.8% |
| 5K-15K | 119 | 9.9% |
| 15K+ | 61 | 5.1% |

Distribution note: this uses only the 1,201 posts from collaborators.json that had non-zero likes (799 posts had 0 likes reported, likely reels where likes are hidden or data missing).

Polene skews much higher than gorjana. The median like count among posts with data is 1,101. That reflects Polene's bigger audience and global macro creator spend. But it's distorted by outliers. Remove the top 5 posts (page.soobin's 1.08M alone) and the picture flattens fast.

The 5K-15K and 15K+ buckets (15% combined) reflect real macro influencer reach, mostly paid international partnerships.

---

## Engagement Quality: Comment-to-Like Ratio

High CLR signals audiences that talk back. Good sign for micro/community creators.

| Creator | CLR | Likes | Comments | Type |
|---|---|---|---|---|
| @glowbyghazal.de | 618.2% | 363 | 2,244 | Unspecified |
| @jenniferrsweet | 189.3% | 872 | 1,651 | Affiliate |
| @therealhousewifeofnorwood | 193.2% | 296 | 572 | Affiliate |
| @emmarosethatcher | 145.9% | 462 | 674 | Affiliate |
| @gabrieladegraaf | 99.6% | 527 | 525 | Affiliate |

**@glowbyghazal.de's 618% CLR is suspicious.** Label says "Echo: Caption + Usertags" with 2,244 comments on 363 likes. Likely a giveaway, tag-to-enter, or comment-to-get-link mechanic. Not organic engagement.

**@therealhousewifeofnorwood and @gabrieladegraaf** both use comment-gating ("Comment OUTFIT if you want details," "Comment for links"). Artificially inflated. Discount these.

**@jenniferrsweet and @emmarosethatcher** are more interesting. Affiliate accounts with genuinely high comment ratios on LTK-linked posts. Both in the 100-1K mid-tier range. Worth a closer look if KKlue builds an LTK/ShopMy layer.

---

## Special Programs: Asian Macro Creator Push

Polene runs a deliberate macro paid push into Asian markets. It's the single biggest driver of likes in this dataset.

| Metric | Value |
|---|---|
| Asian macro paid posts | 6 (0.9% of all posts) |
| Total likes from these posts | 1,553,160 |
| % of all likes | 37.4% |

Identified creators: @page.soobin (Korean, 1.08M likes, Paid), @min.nicha (Thai, 181K, Paid), @fallingin__fall (Korean, 180K, Paid), @zhuzhuclubheaven (Chinese brand ambassador, 53K), @dorisakurada (Japanese, 58K, Unspecified), @jeon_somsom (Korean, Paid).

The three Korean macro paid posts during Nov-Dec 2025 generated 1.44M likes. That's Polene's equivalent of gorjana's athlete program: a concentrated high-spend macro layer that inflates overall program metrics.

German-speaking and French-speaking creators are the next largest disclosed segments (35 and 12 posts respectively), confirming a strong EU/European footprint. Turkish creators show up too (8 posts with reklam tags).

**This brand is not American.** The creator set is explicitly European and Asian. US creators exist in the affiliate long-tail but aren't the core.

---

## Seasonal Posting Pattern

Data from collaborators.json (2,000 posts):

| Month | Posts |
|---|---|
| 2025-08 | 202 |
| 2025-09 | 326 |
| 2025-10 | 300 |
| 2025-11 | 369 |
| 2025-12 | 306 |
| 2026-01 | 285 |
| 2026-02 | 159 |
| 2026-03 | 53 |

**More evergreen than gorjana.** Monthly post volume stays consistently above 200 from Aug through Jan before dropping off in Feb-Mar. No single month spike. Nov-Dec is the peak (675 combined), but it's a gradual ramp, not a holiday explosion.

March is low but that's likely because the data was pulled mid-month (Mar 29).

---

## Repeat Posters (Ongoing Relationships)

From collaborators.json full dataset:

| Creator | Posts | Primary Type | Total Likes |
|---|---|---|---|
| @sunblockstyle | 28 | Affiliate | 5,468 |
| @elinorcharlotte | 10 | Gifted | 0 (likes hidden) |
| @therealhousewifeofnorwood | 10 | Affiliate | 2,586 |
| @sofy.bdx | 9 | Unspecified | 2,710 |
| @louisescotlandstyles | 9 | Affiliate | 0 (likes hidden) |
| @lv_blackwell | 8 | Affiliate | 0 (likes hidden) |
| @tasmin.devi | 8 | Paid | 17,647 |
| @carrieanne_ | 8 | Gifted | 59,727 |
| @krissiklr | 8 | Paid | 0 (likes hidden) |
| @fernanda_reads | 8 | Unspecified | 6,538 |

**@sunblockstyle is their most activated affiliate creator at 28 posts.** That's a dedicated product promoter running Polene content consistently. Not huge engagement (5.4K total likes across 28 posts) but a real affiliate relationship.

**@carrieanne_ stands out.** 8 gifted posts with 59.7K total likes. Much stronger output per post than the affiliate heavy-hitters. Worth noting.

Most of the "0 likes" creators are likely posting reels where likes are hidden in the data.

---

## Whitespace for KKlue

**The Asian creator lane is occupied at the macro end but wide open at the micro level.** Polene spends big on Korean/Thai/Japanese macro influencers (100K+ followers). But Asian-American micro-influencers (10K-100K, US-based, lifestyle/fashion) don't appear in this data at all. That's KKlue's lane. Korean-American creators who live the exact life KKlue's customer lives.

**US-specific affiliate creators are thin.** Polene's affiliate program exists (131 posts, 20% of total) but it's low-engagement filler. Median 308 likes. If KKlue builds a clean ShopMy or LTK affiliate program targeting US-based micro creators, they can own that conversion layer in markets Polene isn't optimizing for.

**No sports/athlete lane.** Polene doesn't use athletes at all. Not their brand aesthetic. But this also means gorjana owns athletes and Polene owns European/Asian aesthetics. KKlue should carve a distinct third niche: Korean-American cultural identity, travel, fine dining, professional women. None of these three brands are there.

**Disclosure is an opportunity.** 77% of Polene's program is undisclosed. If KKlue runs a clean, properly tagged program from launch, it signals legitimacy to both press and potential retail buyers (Nordstrom, boutiques). Polene and gorjana both have significant FTC exposure. KKlue doesn't have to.

**Evergreen structure is actually achievable here.** Polene posts 200+ per month consistently. That suggests their gifting program is running on autopilot. A smaller KKlue program of 20-30 well-managed creator relationships posting monthly would produce comparable category presence at lower cost than Polene's macro spend.

---

## Skeptic's Core Point

Polene's program looks massive because of three Korean macro paid posts. Take out @page.soobin, @min.nicha, and @fallingin__fall and the median post in this program gets 376 likes. The affiliate layer (131 posts) has a median of 308 likes and generates only 7.4% of total likes despite being 20% of posts. The real program underneath the macro spend is a gifting-and-affiliate long-tail running mostly undisclosed with modest per-post engagement. Polene's brand equity does the work, not the influencer strategy.
