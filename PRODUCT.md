# Product

<!-- impeccable:product-schema 1 -->

## Platform

web

## Users

**Primary and only first-class user:** recruiters, hiring managers, and design leads reviewing new-grad / entry-level UX and product design candidates. Two specific targets shape decisions:

- **Datadog ADP (Associate Designer Program)** — evaluators are looking for data-density fluency, systems thinking, and observability/enterprise curiosity.
- **Broad entry-level UX / product design roles** — evaluators want proof of shipped work, tool fluency, case-study depth, and hire-able judgment.

Freelance clients, peers, and the design community are welcome visitors but are not the audience the design optimizes for.

## Product Purpose

Personal design portfolio for **Kathlyn Le** (recent University of Houston graduate, Cullen College of Engineering, B.S. Digital Media / UX focus, Magna Cum Laude). Its job is to convert a scanning recruiter into an interview loop, then convince a hiring manager on a deeper read. Success is measured in interview requests and program acceptances, not visits.

## Positioning

What a neighboring new-grad portfolio cannot truthfully copy:

- **Extended real internship at FinThrive** (six months, extended beyond original term) working on production enterprise SaaS in healthcare finance — including a data-dense claims dashboard, a full mobile dark-mode prototype, and an AI chatbot experience shipped to real users.
- **A range across enterprise SaaS, healthcare, consumer app, marketplace, research, and freelance client work** — not a monoculture of student projects.
- **Explicit AI-forward tooling** (Figma AI, Claude, Claude Design, Lovable) alongside classical UX craft — current with where the industry has moved, not stuck in 2022.

## Operating Context

- Recruiters typically spend under 60 seconds on the first read, often on mobile between other tasks, before deciding to open a case study.
- Hiring managers do a longer desktop pass on 1–2 case studies before an interview decision.
- The Datadog ADP application separately asks for a single project write-up; the FinThrive Claims Dashboard is the intended answer.
- Deployed as static site on GitHub Pages at the custom domain **kathlynle.com** (CNAME in repo); media (images, videos) hosted on Cloudinary rather than in-repo.

## Capabilities and Constraints

- Static HTML site, one file per page, no framework or build step. Tailwind loaded via CDN. Custom fonts served from `brand_assets/`. Custom WebGL fluid shader on the homepage hero. Custom JS for polaroid carousel, chatbot/claims carousels, image gallery grid, and password gate on FinThrive.
- All heavy media (videos, project images, polaroids, journal images) is hosted on Cloudinary under `portfolio/...` folders. Repo stays under 1 MB for fast clones and deploys.
- Free-tier Cloudinary image cap is 10 MB per file — oversized originals must be re-encoded (e.g., palette PNG, WebP) rather than uploaded raw. JPEG conversion is prohibited for any asset that relies on transparency (see `## Brand Commitments`).
- Case studies: `finthrive.html`, `livedive.html`, `dcp.html`, `uxresearch.html`, `sttr.html`, `vendgo.html`. Additional pages: `index.html`, `about.html`, `journal.html`, `portfolio.html` (currently an orphan not linked from anywhere).
- FinThrive case study is behind a password gate (`#pw-gate`); do not remove or bypass.

## Brand Commitments

- **Identity:** the personal brand is `k.le` (also stylized `k.lê`) with the full name **Kathlyn Le**. Pronunciation guide on the about page: `/cath • leen/`.
- **Typography:** custom wordmark font **JayaGiri** (self-hosted at `brand_assets/JA JayaGiri-Sans.ttf`) for headings and logo, **Quicksand** (Google Fonts) for body. Both are locked-in unless the user explicitly changes them later in new-work.
- **Logo asset:** `brand_assets/Portfolio Logo.png` and brand guide at `brand_assets/Portfolio Brand Guidelines.png`.
- **Voice:** first person, confident but not arrogant, no em dashes, user-focused, AI-forward. Existing case-study copy sets the tone floor — new copy should match that register.
- **Protected content that must not be altered by later design passes:**
  - The named manager quote from **Matt Rife (Product Design Manager)** on the FinThrive case study.
  - The FinThrive case-study password gate and all content behind it.
  - All existing project screenshots and imagery across all case studies — do not swap or replace.

## Evidence on Hand

- **Real internship experience:** FinThrive UX/UI Design Intern, June–December 2025, extended past original term, with concrete work shipped (AI chatbot, mobile dark mode, claims dashboard collaboration) and a named manager quote.
- **Teaching and community:** UH UX Lab Teaching Assistant & Lab Manager (Jan–May 2025); Social Media Intern & Student Rep at UXPA Houston (Mar 2024–May 2025); Vice President & Co-Founder of UX Coogs (Sep 2023–May 2025).
- **Freelance work:** Digital content producer for The Nuu Moon, The Million, and Tiffany G'lam Pro (March 2025–present).
- **Case studies with source assets locally backed up** (Cloudinary-hosted for deploy).
- **Resume** at https://www.dropbox.com/scl/fi/xgbnkxe5gx43fwqydfz30/Kathlyn-Le-Resume.pdf?rlkey=9aznfdszl2gtrf9pr0js8mzw6&st=fai9iziw&dl=0.
- **A single quantified outcome** (`15%` usability improvement on FinThrive, measured against baseline task-completion and time-on-task across chatbot / dark mode / claims dashboard flows, with eight FinThrive product users). Numbers for LiveDive, STTR, VendGo are not yet on record and must not be fabricated.
- **A pre-existing broken image reference** in `portfolio.html` (4 `brand_assets/*Thumbnail.png` paths whose source files never existed there — files exist under different names in `Thumbnail PNGS/`). This page is an orphan; not currently linked from anywhere.

## Product Principles

1. **The Claims Dashboard is the money shot for Datadog ADP.** Any restructuring must not bury the data-dense enterprise work that best signals fit.
2. **Real internship > student projects.** Structural choices that give FinThrive prominence over academic work are correct.
3. **Range is a feature, not a bug.** Six different domains (enterprise SaaS, healthcare, consumer, marketplace, research, freelance client) prove adaptability — do not consolidate them into a monolith.
4. **AI-forward is a differentiator, not a footnote.** Mentioning Figma AI, Claude, Lovable in the skills stack meaningfully separates this portfolio from most 2024–2025 new-grad portfolios; keep it visible.
5. **Never fabricate outcomes.** Only the FinThrive `15%` figure is a confirmed measured result. Numbers for other case studies stay off the page until the user provides real ones.

## Accessibility & Inclusion

- **WCAG AA is the minimum bar** for color contrast, focus visibility, and text readability across all pages.
- **Honor `prefers-reduced-motion`** — the homepage WebGL fluid shader, polaroid carousel marquee, hero label bounces, and any future motion work must degrade to a static state for users who request it.
- Case-study screenshots must carry meaningful `alt` text (existing coverage is reasonable; new work should not regress it).
