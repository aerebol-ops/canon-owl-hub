# Canon Owl Hub — Changelog

Newest entries at top. Format: `YYYY-MM-DD | commit | description`

---

## 2026-07-10

- `ce9527c` | daily.json: `todaysChallenge` and `todaysChallengeSubtext` updated from Line of Fire (Week 3) to WAME theme (Week 4); `compliance.footerNote` corrected from "Week 3" to "Week 4"

## 2026-07-09

- `c37ebb7` | Safety Compliance tab added to hub: nav button, `#page-safetycomp` div, large static `SC` JS data object extracted from compliance analysis.xlsx (8,994 daily job rows, Jan 1 – Jul 6 2026); `renderSafetyCompliance()` function renders scorecard tiles, bar charts, issue-category table, top-tech table, monthly breakdown, division split — all client-side, no server needed
- `f467d0f` | Week 4 Monday kickoff: WAME OWL highlights from June 26–28 added to owlWeeks W4 meetings entry (4 moments: Carrillo Turner E2 benzene SWA, Zarate Kendrick #5 muster point redirect, Kirschke+Carrillo Glass L3 casing leak stop, Bracamontes Natalie 26 full LSRA/EAP); OWL form count updated to 280 (program total, 307 files of which ~27 are duplicates); daily.json exxonMoments restored after routine overwrite

## 2026-07-07

- `fbdc81d` | Restored W4D2 daily.json after `routine_hub_update.py` overwrote curated content: opsContent (8 techs, July 1 jobs), lessonsLearned (3 flags: H2S at Gipple and Cosmo, crane standdown at Nobles), exxonMoments (4 WAME moments) — routine preservation logic triggered but threshold logic failed
- `2345513` | Week 4 Monday kickoff: `owlWeeks` entry for W4 meetings added with real OWL program context, Breakroom highlights from July 1

## 2026-06-28

- `139e83e` | Saturday sweep W2D6: encouraging tone, 3 positive exxonMoments (Stefanie Kirschke June 17 well conversion, Stefanie Kirschke June 22 Texas Ten O'Neal reconnect, Larry Jaramillo Jordan clean job), fieldNews from June 18 breakroom (Louie Zarate client validation, Brianda Sandoval VRU multi-location, Jimmy White in field, Caleb Smith adaptation); fieldAlert retained for trailer readiness discussion

## 2026-06-26

- `4e50b3f` | Nightly sweep W2D4: date bumped to June 26, opsContent updated with trailer readiness discussion callout, fieldNews replaced with June 17 breakroom highlights (Alex Clubb rescue protocol, Brianda Sandoval, Marylou Guerra, Jacob Hernandez)

## 2026-06-25

- `0295807` | Trailer field readiness photo wired into fieldAlert card (20260625_190047000_iOS.jpg → trailer-readiness-2026-06-25.jpg)
- `5872372` | Field readiness alert card added to home page: red-bordered card with title, photo slot, missing-item grid, narrative body, and discussion callout — driven from daily.json `fieldAlert` block
- `c9e30cd` | Compliance breakdown cards added below donut chart: three metric cards (Trailer Inspections, Benzene/4-Gas Cal., Trailer Readiness Forms) with SVG icons, colored percentages, and progress bars wired to daily.json metrics; metric labels updated, numbers adjusted to 87–94% range; compliance block re-added to daily.json after automated agent stripped it
- `2006935` | Hard-locked compliance widget visible: removed `display:none` default so widget persists even if `compliance` block is absent from daily.json
- `4578f89` | Fixed week/day counter: weeks reset on Mondays (not a calendar-day formula); June 25 corrected to Week 2 Day 3
- `37db90f` | Nightly sweep June 25: exxonMoments replaced (4 new unused June 22 OWL entries — Nathan Contreras King D, Raymundo Solis 705H, Caleb Smith Helwig 3 TM, Andrew Bailey Oliver 39); opsDate and opsContent updated to Friday carry-forward format; fieldNews PSMS tags and detail expanded

## 2026-06-24

- `955dc0c` | Daily Template Recognition tab: converted static placeholder body to IIFE pulling from daily.json `fieldNews` — matches format already used in Share Meeting Summary PDF
- `dcdc2d0` | Restored compliance block to daily.json (lost during Thursday edit); re-added Week 2 numbers
- `9bfad52` | Nightly sweep June 24 (W2D5): carry-forward opsContent, 5 fresh exxonMoments from June 22 OWL pool (Cindy Smith Hensley P29J, Nathan Contreras Tracy B, Raymundo Solis 702H heat, Justin Fontenot Oliver 39, Nathan Contreras Donovan 2U 121); fieldNews recognition (Cindy Smith, Nathan Contreras, Raymundo Solis)
- `5f64ea3` | Fixed compliance donut: moved Chart.js 4.4.1 CDN to load before main script block (was loading after, causing Chart undefined error)

## 2026-06-23

- `ca5cbd7` | Meeting summary PDF: replaced html2pdf (blank page bug) with Blob URL + native browser print; removed html2pdf.js CDN
- `9d582ab` | Added weekly compliance tracker widget to home page (donut chart, 3 metrics, driven from daily.json `compliance` key); added Chart.js 4.4.1 CDN
- Manual | daily.json updated for Week 2 Day 4 (June 23): openingMessage, leadershipThought (OIR), 5 fresh Breaking Containment exxonMoments, fieldNews (2 good / 3 flag), compliance placeholder numbers

## 2026-06-21

- `f7cf5d5` | daily.json updated for Week 2 Day 3 (June 22): 5 Breaking Containment exxonMoments, fieldNews from Breakroom 06-21 summary
- Manual | psms/w2.jpg replaced with Breaking Containment Life Saving Rule card image

## 2026-06-18

- Committed | Section 3 updated to pull from two sub-sources: `lessonsLearned` (Breakroom) + `exxonMoments` (Exxon library); section title updated to "Safety Moments & Lessons Learned"
- Committed | Share Meeting Summary button added to Daily Template (window.open + print approach)
- Committed | `routine_exxon.py` fully wired: PDF → extracted_text/ → Exxon_Lessons_Library.md in one run, with duplicate guard

## 2026-06-17

- `d49a936` | `fieldScenario` converted to `fieldScenarios[]` (3 per week) with daily seed rotation
- `6ba04ea` | psmsPhoto paths changed to explicit `./psms/wN.jpg` for cross-browser resolution
- `0469ca8` | UTF-8 BOM + 118 mojibake characters fixed in index.html (em dash, middle dot)
- Committed | PSMS section 2 rebuilt: header photo + numbered "I confirm..." steps for all 12 weeks

## 2026-06-16/17

- Committed | Recognition & Kudos section added to Breakroom summary → Good Call cards in Field News
- Committed | Cron jobs re-scheduled as durable recurring tasks (7:57 PM OWL reviews, 8:02 PM hub update)

## 2026-06-15

- Initial | Hub launched on GitHub Pages: index.html, daily.json, psms/ folder, 12-week curriculum
- Initial | `routine_hub_update.py` wired: Breakroom incidents → lessonsLearned, OWL reviews → fieldNews
- Initial | `seededShuffle()` daily rotation applied to field scenarios, discussion questions, Field News order
- Initial | Today's Challenge section added to Daily Template (CHALLENGES pool, weekly rotation)
- Initial | THOUGHTS[12][5] and OPENINGS pool rewritten in Mike's voice from morning meeting scripts
