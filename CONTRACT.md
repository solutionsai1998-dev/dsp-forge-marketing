# DSP Forge Marketing Site - Project Contract

**Last Updated:** April 15, 2026  
**Status:** LIVE  
**URL:** https://dsp-forge-marketing.vercel.app

---

## URL Reference (clear as of 2026-04-15)

| Purpose | URL | Notes |
|---------|-----|-------|
| Marketing site (live) | https://dsp-forge-marketing.vercel.app | Main URL, aliased from preview deploys |
| Marketing repo | https://github.com/solutionsai1998-dev/dsp-forge-marketing | Static HTML/CSS/JS, Vercel-deployable |
| DSP Hours Manager (demo) | https://dsp-app-production.up.railway.app | Seeded demo data, prospects can click around |
| DSP Hours Manager (live app) | https://dsp-hours-deploy-production.up.railway.app | Customer production deployment |
| DSP Hours Manager repo | https://github.com/solutionsai1998-dev/dsp-app | Next.js + Prisma + PostgreSQL on Railway |
| Demo login | https://dsp-app-production.up.railway.app/login | owner/demo123 |

**Important:** These are two separate projects with separate repos and separate deployments. Do not confuse them.

---

## Project Overview

DSP Forge is a marketing website for the DSP Hours Manager product. It is a static HTML/CSS/JS site hosted on Vercel.

Purpose:
- Attract DSP operators with pricing, features, and social proof
- Provide a contact path for custom development inquiries
- Support outbound sales with clean, honest marketing copy

---

## Site Structure

- `index.html` — Home page (pricing, screenshots, CTA)
- `features.html` — Feature list with click-to-expand screenshots
- `pricing.html` — Full pricing page
- `about.html` — Founder story, click-to-expand dashboard screenshot
- `contact.html` — Contact form (mailto link) and outbound sales path
- `lightbox.js` — Click-to-expand image modal (must be inside `<body>`)
- `styles.css` — Shared styles, CSS variables, responsive design

---

## Key Decisions

### Pricing (set 2026-04-15)
- Core platform: $4/driver/month
- $500/month cap — never pay more regardless of driver count
- Custom development: $100–150/hour or $2,500–5,000 fixed project
- Enterprise: contact for pricing

### Positioning
- "Custom tools built by a dispatcher" — operational grounding, not generic SaaS
- Emphasis on real screens, practical workflows, honest pricing
- No free tier advertised; pilot offered after commitment

### Screenshot Lightbox (fixed 2026-04-15)
- Lightbox modal `<div>` must be INSIDE `<body>`, not between `</head>` and `<body>`
- `lightbox.js` must be present and loaded via `<script src="lightbox.js" defer></script>` in `<head>`
- Click-to-expand uses `onclick="openLightbox(...)"` on `<article>` elements
- The `.click-hint` span shows "Click to expand" in accent color

---

## Today'S Work Log (2026-04-14 → 2026-04-15)

### Morning/Afternoon
- Researched DSP software pricing with subagents (Grok + GLM-5)
- Confirmed $4/driver with $500 cap is well below market (competitors at $10–12)
- Dylan decided to keep pricing visible on marketing site, not contact-us only

### Lightbox Fixes
- Features page: lightbox modal was outside `<body>` tag — fixed
- About page: same issue — fixed
- `lightbox.js` was missing entirely — created and deployed
- Screenshot click-to-expand now works on all pages

### Pricing Updates
- Home page: updated from "$3 to $4" to "$4/driver/month" with $500 cap mention
- Home page bullet list updated to include "$500/month cap — unlimited drivers after that"
- Pricing page already had correct pricing from earlier changes

### Files Changed (commit `01e1e33`)
- `features.html` — fixed body/lightbox placement
- `about.html` — fixed body/lightbox placement
- `lightbox.js` — created
- `index.html` — updated pricing section

---

## Workflow Notes

1. Marketing site is pure static HTML — no build step needed locally
2. Push to GitHub → Vercel auto-deploys
3. Vercel preview URL changes on each deploy; main alias stays stable at `dsp-forge-marketing.vercel.app`
4. If lightbox breaks again, check: (a) `<div id="lightbox">` is inside `<body>`, (b) `lightbox.js` is committed

---

## To Do / Future Work

- [ ] Add actual founder photo (currently placeholder)
- [ ] Add more screenshots from live app
- [ ] Consider adding testimonials/social proof
- [ ] Demo instance still needs to be deployed and accessible
- [ ] Sales email templates ready but not yet sent