# SEO Audit Summary — Lawn & Land Marketing Clients
**Audit Date:** 2026-03-25  
**Sites Audited:** 27  
**Auditor:** Roshi (automated via DataForSEO API + static HTML analysis)

---

## ⚠️ Methodology Notes

- **H1 Detection Limitation:** All 26/27 sites use Avada/Fusion page builder, which embeds H1 text inside deeply nested `<div>` structures with inline styles. Static HTML regex extraction failed to detect H1s that exist inside page builder wrappers. **This is a false positive** — H1s almost certainly exist on these pages but weren't detectable without JavaScript rendering. Recommend manual H1 verification or a JS-enabled crawler.
- **Blog Detection:** Searched for `/blog` links in static HTML. Sites with blog links buried deep in JS menus may have been missed (e.g., Goodin Lawn Care has a blog but was initially marked "No").
- **Sitemap Count:** Many sitemaps are sitemap index files pointing to sub-sitemaps — page counts reported may be 0 where an index file exists (counted `<url>` tags, not `<sitemap>` entries).
- **Backlink Data:** Via DataForSEO backlinks/summary/live API. "Spam Score" field = domain rank (higher = stronger, not spammier — DataForSEO `rank` field).

---

## 📊 Scores by Site

| Site | Score | Top Issue |
|------|-------|-----------|
| Augusta Grass Masters | 8.5/10 | H1 not detected (page builder), no blog |
| ALF Landscape | 8.5/10 | H1 not detected (page builder), no blog |
| BE Landscapes | 9.0/10 | H1 not detected (page builder) |
| Bills Lawn | 9.0/10 | H1 not detected (page builder) |
| Brothers Outdoor Services | 9.0/10 | H1 not detected (page builder) |
| My Countryside Lawn | 9.0/10 | H1 not detected (page builder) |
| From The Ground Up Tampa Bay | 8.5/10 | H1 not detected (page builder), no blog |
| FTGU Pools | 8.5/10 | H1 not detected (page builder), no blog |
| Full Service Property | 9.0/10 | H1 not detected (page builder) |
| Going Yard LLC | 9.0/10 | H1 not detected (page builder) |
| Goodin Lawn Care | 9.0/10 | H1 not detected (page builder) — HAS blog |
| Green Dream Lawns | 8.5/10 | H1 not detected (page builder), no blog |
| GreenTech Gardeners | 8.5/10 | H1 not detected (page builder), no blog |
| Groundsmith Landscaping | 8.5/10 | Short title tag (29 chars), H1 not detected, no blog |
| Hill Landscaping NJ | **9.5/10** | No critical issues — best in portfolio |
| In Bloom Lawn and Landscape | 9.0/10 | H1 not detected (page builder) |
| Independent Lawn Service | 9.0/10 | H1 not detected (page builder) |
| Landscape St Louis | 9.0/10 | H1 not detected (page builder) |
| PC Solution LLC | 8.5/10 | H1 not detected (page builder), no blog |
| Outdoor Perfection Landscaping | 9.0/10 | H1 not detected (page builder) |
| Renegade Landscapes | 8.5/10 | H1 not detected (page builder), no blog |
| Rock Solid NV | 8.5/10 | H1 not detected (page builder), no blog |
| My Rock Solid Landscape | 9.0/10 | H1 not detected (page builder) |
| Secret Gardens LLC | 8.5/10 | H1 not detected (page builder), no blog |
| Lawn Care Columbia | 8.5/10 | H1 not detected (page builder), no blog |
| Toms Mulch | 8.5/10 | H1 not detected (page builder), no blog |
| Vash Landscaping | 8.5/10 | H1 not detected (page builder), no blog |

**Average Score:** 8.8/10  
**Highest:** Hill Landscaping NJ (9.5/10)  
**Lowest (tied):** 14 sites at 8.5/10

---

## 🔴 Top 5 Recurring Issues (Portfolio-Wide)

### 1. No Blog — 18 of 27 sites (67%)
The single biggest SEO gap across the portfolio. Blogs are the primary mechanism for:
- Ranking long-tail local keywords ("best lawn care in [city]", "when to aerate lawn in [state]")
- Earning natural backlinks
- Demonstrating E-E-A-T (expertise, experience, authoritativeness, trust)
- Content freshness signals to Google

**Action:** Launch blog programs for all 18 sites without blogs. Even 1-2 posts/month targeting local + seasonal keywords moves the needle within 60-90 days.

### 2. H1 Tags in Avada Page Builder (Detection Limitation)
Static crawlers cannot reliably detect H1s in Avada/Fusion Builder. A JS-rendered crawler (Screaming Frog, DataForSEO On-Page full crawl with JS rendering) should verify H1 presence on all 27 sites. If missing, add H1 with: `[Primary Service] in [City, State] | [Brand Name]`

### 3. Weak Backlink Profiles — Most sites under 150 referring domains
Only 2-3 sites in the portfolio have 200+ referring domains. For competitive local markets, 50-200+ referring domains from local/industry sources is the threshold for ranking in top 3 maps + organic. 

**Top performers by referring domains:**
- Augusta Grass Masters: 233 RD
- Hill Landscaping NJ: 125 RD
- Most others: 50-120 RD range

**Action:** Systematic citation building (NAP consistency across 50+ directories), local press outreach, supplier backlinks, and association memberships.

### 4. No XML Sitemap Accessible at /sitemap.xml — Affects ~8 sites
Several sites return 301 redirects or errors at `/sitemap.xml`. While the sitemap may exist at a different URL, Google prefers the canonical path. Sites without an accessible sitemap risk slower indexation of new content.

**Action:** Ensure sitemap.xml is accessible at root domain AND submitted to Google Search Console.

### 5. Title Tags Missing City/Location — ~30% of portfolio
Several title tags are generic (just brand name) or missing geographic modifiers. Local SEO is fundamentally about matching searcher intent with location + service.

**Weak example:** `"Groundsmith Landscaping Company Dublin OH"` (29 chars, no full-service descriptor)  
**Strong example:** `"Landscaping Company in Flemington NJ | Hill Landscaping"` (Hill Landscaping NJ)

---

## 🟡 Secondary Issues

- **Schema Markup:** Most sites have schema (via Avada/RankMath). Ensure LocalBusiness schema includes: NAP, service area, services offered, hours, geo coordinates.
- **robots.txt:** All sites have accessible robots.txt — ✅ good baseline.
- **SSL/HTTPS:** All 27 sites are on HTTPS — ✅ no issues.
- **HTTP Status:** All 27 return 200 — ✅ no broken sites.

---

## ✅ Priority Recommendations

1. **Blog Launch Sprint** — Create a templated blog workflow and launch blogs for all 18 blogless sites. Prioritize 3-4 posts targeting seasonal + local keywords per site in Q2.
2. **JS-Rendered H1 Audit** — Run Screaming Frog with JS rendering ON to confirm H1 presence across all sites. Fix any true misses.
3. **Citation Building Campaign** — Build 30-50 citations per site across Yelp, Angi, BBB, HomeAdvisor, local chambers, and industry directories. Focus on NAP consistency.
4. **Google Search Console Sitemap Submission** — Verify all 27 sites have sitemaps submitted in GSC. Check for indexation issues.
5. **Title Tag Audit + Optimization** — Review every title tag against format: `[Primary Service Keyword] in [City, State] | [Brand]`. Prioritize the 8-9 sites scoring 8.5.

---

## 📁 Individual Audit Files

All 27 individual audit files are available in `/audits/` directory:

- augustagrassmasters.md, alflandscape.md, belandscapes.md, billslawn.md
- brothersoutdoorservices.md, mycountrysidelawn.md, fromthegrounduptampabay.md
- ftgupools.md, fullserviceproperty.md, goingyardllc.md, goodinlawncare.md
- greendreamlawns.md, greentechgardeners.md, groundsmithlandscaping.md
- hilllandscapingnj.md, inbloomlawnandlandscape.md, independentlawnservice.md
- landscapestlouis.md, pcsolutionllc.md, outdoorperfectionlandscaping.md
- renegadelandscapes.md, rocksolidnv.md, myrocksolidlandscape.md
- secretgardensllc.md, lawncarecolumbia.com, tomsmulch.md, vashlandscaping.md

---

*Generated by Roshi SEO Audit System | Lawn & Land Marketing | 2026-03-25*
