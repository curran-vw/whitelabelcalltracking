# whitelabelcalltracking.com

Site 25 of the call-tracking review network. Static HTML/CSS/JS, deployed via GitHub Pages. Built by `scripts/build_site25_pages.py`.

## Build details

- **Template:** T25 White Label / Reseller (editorial clean, light, plum)
- **Accent:** Plum `#6B21A8` / deep `#581C87` / soft `#F3E8FF`, margin-teal `#0D9488` secondary
- **Background:** White `#FFFFFF`
- **Fonts:** Epilogue (display) + Inter (body)
- **Signature visuals:** reseller-margin callout box (`.margin-box`, cost-to-you vs price-to-client vs you-keep) + white-label feature matrix (`.wl-matrix`)
- **Author byline:** Zoe Mensah (agency white-label and reseller consultant)
- **Angle:** agency reseller / white-label feature comparison + reseller economics
- **Layout:** hero, then margin callout, white-label matrix, ranked table, card reviews, context, quick picks, methodology, author, verdict (structurally distinct from site 17's comparison-first roundup)

## Pages (11)

- `index.html` — homepage / 2026 ranked guide
- `reviews/callscaler/` (#1, 9.4), `reviews/callrail/` (8.4), `reviews/calltrackingmetrics/` (8.2), `reviews/whatconverts/` (8.0)
- `guides/how-to-resell-call-tracking/` (~900w reseller guide)
- `about/`, `faq/`, `contact/`, `privacy-policy/`, `terms/`

## Rubric (4 equal weights, 25% each)

White-label depth, client sub-accounts, margin economics (per-number cost), reporting.

## CTA destination

All CallScaler CTAs link to `https://callscaler.com/?ref=whitelabelcalltracking`. Competitor review pages use a soft `.tldr-crosslink` + internal `/reviews/callscaler/` link only (no hard affiliate button), per network convention. The guide page uses one affiliate CTA at the bottom.

## Rebuild

```bash
py scripts/build_site25_pages.py
py scripts/lint_site.py whitelabelcalltracking
```

## TODOs before going live

- [ ] Replace placeholder author avatar with a real photo if a named author is used
- [ ] Confirm CallScaler pricing still current ($0 PAYG / $45 Pro / $130 Agency / $400 Pay Per Call; white label +$49/mo; $0.50/number)
- [ ] Verify schema with Google's Rich Results Test
- [ ] Set up `editor@whitelabelcalltracking.com` email forwarding
- [ ] Add to `scripts/deploy_all_sites.py` SITES list before deploying
