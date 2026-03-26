# L&L SEO Playbook
**Lawn & Land Marketing — Internal SEO Documentation & Tooling**
*Last updated: March 26, 2026*

---

## 🔗 Live Pages

| Page | URL | Status |
|------|-----|--------|
| SEO Playbook | https://lawnlab.dev/seo-playbook | ✅ Live |
| Client Audit Results | https://lawnlab.dev/seo-audit | ✅ Live |
| SEO Deliverables Checklist (SOP Tracker) | https://lawnlab.dev/seo-checklist | ✅ Live — Interactive |

---

## 📁 Repository Contents

| File/Folder | Description |
|-------------|-------------|
| `README.md` | This file — full project context |
| `SEO-CHECKLIST.md` | 38-item checklist with current state, target state, automation scores |
| `seo-playbook.html` | Source HTML for the SEO Playbook page (deployed to lawnlab.dev/seo-playbook) |
| `audits/SUMMARY.md` | Portfolio-wide audit summary — corrected March 26, 2026 |
| `audits/*.md` | Individual client audit files (27 clients) |

---

## 📖 What Each Page Is

### `/seo-playbook` — The Process Doc
Our standardized SEO process — what we do for every client, organized by category:
- Google Business Profile (build, posts, review replies)
- Website (service pages, service area pages, internal linking)
- Technical SEO (Rank Math, schema, GSC, sitemaps)
- Content (blog, alt text)
- Link Building & Citations (Whitespark, press releases, backlinks)
- Roadmap (known gaps + improvement priorities)
- Tools Stack

Built March 25, 2026 from a brain dump with Matt. This is the source of truth for "what does L&L do for SEO clients."

---

### `/seo-audit` — Client Audit Results
Technical audit of all 27 active SEO clients. Corrected March 26, 2026.

**Key findings:**
- ✅ 27/27 clients have active blogs (previous audit falsely reported 18 missing — was a static HTML crawl bug)
- ✅ 27/27 HTTPS, sitemaps, meta descriptions, mobile viewport
- ✅ 26/27 H1 detected (Groundsmith Landscaping flagged for manual browser verification)
- ⚠️ 3 clients missing GBP link on homepage: Goodin Lawn Care, GreenTech Gardeners, Hill Landscaping NJ
- ⚠️ 14/27 clients using `Organization` schema instead of `LocalBusiness` — schema upgrade opportunity
- ⚠️ Vash Landscaping — 4 H1 tags on homepage (needs consolidation)
- ⚠️ BE Landscapes — meta description too short (86 chars)
- ⚠️ Full Service Property — no social links on site

**Audit method:** Direct HTTP checks + raw HTML inspection. Blog confirmed via `GET /blog/` HTTP status. Previous static HTML crawl missed JS-rendered content (Avada/Elementor sites).

---

### `/seo-checklist` — Live SOP Tracker ⭐
The main resource. 38-item interactive checklist across 5 categories with:

**Categories:**
1. On-Page SEO (9 items) — keyword research, service pages, SAPs, blog, internal linking, alt text, title/meta, H1, competitor analysis
2. Off-Page SEO (10 items) — citations, press releases, backlinks (directories, social, vendor testimonials, chamber, sponsorships, press pitches, HARO)
3. Technical SEO (9 items) — Rank Math, schema, GSC, sitemap, robots.txt, redirects, page speed, mobile, canonicals
4. Google Business Profile SEO (8 items) — profile build, categories, posts, review replies, photos, Q&A, GBP link, attributes
5. Reporting (2 items) — internal scorecard, client monthly report

**Features:**
- Per-item status: Not Started → In Progress → Complete → Automated ⚡
- "Assigned to" field per item
- Progress notes per item (in modal)
- Live segmented progress bar
- Filter by status
- "View Details →" modal per item with: current state, target state, human involvement, automation potential
- Automation score 0–10 per item (0 = fully human, 10 = fully automated)
- Name prompt on first visit — saves to localStorage, used on all updates
- Supabase backend — whole team sees same state in real time

**Supabase:** Project SEO (`ztzqnpajurlxuorrfiwd.supabase.co`) — dedicated project, not shared with Task Garden.

---

## 📊 Current Portfolio State (as of March 26, 2026)

| Metric | Value |
|--------|-------|
| Active SEO clients | 27 |
| Average audit score | 9.7/10 |
| Clients with blogs | 27/27 (100%) |
| Clients with LocalBusiness schema | 13/27 (48%) |
| Clients with GBP link on site | 24/27 (89%) |

---

## 🗺️ What We're Working Toward (Long-Term Vision)

The SEO checklist SOP tracker is the foundation. Here's the roadmap of what gets built on top of it:

### Phase 1 — Standardize (Now)
- [ ] Work through all 38 checklist items with the SEO team
- [ ] Fix the 3 missing GBP links (Goodin, GreenTech, Hill NJ) — quick wins
- [ ] Upgrade 14 clients from `Organization` → `LocalBusiness` schema
- [ ] Standardize Rank Math config across all 27 client sites
- [ ] Audit and fix H1 issues on page builder sites

### Phase 2 — Automate (Next 60–90 days)
High-automation-score items to build first (score 7–9):
- **Blog pipeline** (score 9) — GSC API → topic selection → AI brief → AI draft → internal links → review → publish. Fully automated except human review gate.
- **Alt text** (score 9) — one-time retroactive AI audit across all 27 sites via WP REST API
- **Internal linking** (score 8) — auto-check sitemap on every publish, suggest link insertions
- **Competitor analysis** (score 8) — monthly DataForSEO automated rank comparison
- **Page speed monitoring** (score 8) — monthly PageSpeed Insights API scan, alert when client drops below 50 mobile
- **GSC monthly pull** (score 8) — automated data pull feeding blog topics + SAP priorities
- **Internal monthly scorecard** (score 9) — GSC + SE Ranking + DataForSEO → auto-generated per-client report

### Phase 3 — Scale (90+ days)
- Keyword research API pipeline (DataForSEO volume + competition scoring at onboarding)
- Service area page expansion system (GSC city impressions → trigger new SAP)
- Client monthly report (AI-drafted from data, human personalizes + sends)
- Press release quality tracking (which PRs get indexed)
- Backlink acquisition system (vendor testimonials, HARO monitoring, press pitch templates)

### Phase 4 — Dashboard
Per-client SEO dashboard showing live rankings, traffic trends, content published, backlinks added, GBP activity. The data infrastructure gets built in Phase 2–3; the dashboard is Phase 4.

---

## 🛠️ Tools Stack

| Tool | Use |
|------|-----|
| WordPress + Rank Math | CMS + on-page SEO for all client sites |
| Google Search Console | Rankings, indexing, performance (API access needed for automation) |
| SE Ranking | Rank tracking + site audit + keyword research |
| DataForSEO | Backlink analysis, competitor research, volume data |
| Whitespark | Citation building + NAP monitoring |
| Signal Genesis / Search Atlas | Press release distribution (2/month per client) |
| Zapier + Claude AI | Automated review replies on GBP |
| n8n | Workflow automation (blog pipeline target) |
| Supabase | Backend for SEO checklist SOP tracker |

---

## 🔧 Technical Notes

### lawnlab.dev Deployment
- DNS: Vercel (CNAME)
- Repo: `LawnAndLandMarketing/lawnlab-dev`
- Deploy method: Vercel CLI (GitHub auto-deploy broken — token mismatch)
- **Correct deploy command:**
```bash
source ~/.secrets.env
cd /tmp/lawnlab-dev-deploy/src  # or fresh clone
npx vercel link --yes --token $VERCEL_TOKEN --scope lawn-and-land-marketing --project lawnlab-dev
npx vercel deploy --prod --token $VERCEL_TOKEN --scope lawn-and-land-marketing
```

### SEO Checklist Supabase
- Project: `Project SEO` (dedicated — not Task Garden)
- URL: `https://ztzqnpajurlxuorrfiwd.supabase.co`
- Table: `seo_checklist_items`
- RLS: disabled (internal tool)
- Credentials in `~/.secrets.env` on Roshi's machine

### Audit Scripts
- All 27 client audits: `/audits/*.md` in this repo
- Corrected audit method: direct HTTP `GET /blog/` check (not static HTML crawl)
- Original audit was wrong — static crawl missed JS-rendered nav links on Avada sites

---

## 👤 Human Actions Still Needed

These require a human to execute (can't be automated):

1. **Fix 3 GBP links** — add GBP link to footer/contact on Goodin Lawn Care, GreenTech Gardeners, Hill Landscaping NJ
2. **Fix Vash Landscaping** — consolidate 4 H1 tags to 1 in Avada builder
3. **Schema upgrades** — update 14 clients from Organization → LocalBusiness in Rank Math
4. **Rank Math standardization** — apply standard config to all 27 client sites (~30 min/site)
5. **Groundsmith Landscaping** — verify H1 in Chrome DevTools (page builder site, static crawl inconclusive)
6. **Chamber of Commerce** — coordinate with each client to join their local chamber (their cost)

---

*Built by Roshi 🐢 in collaboration with Matt Foreman — Lawn & Land Marketing*
*Session: March 25–26, 2026 — SEO standardization sprint*
