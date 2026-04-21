# CLAUDE.md — creative-legends-site

Instructions for Claude Code when editing Bridget Farhat's **Creative Legends Co.** portfolio.

## What this is

Single-file static portfolio for Bridget Farhat — photo + video studio, Creative Legends Co. One HTML file (`index.html`) with inline CSS + JS. No build step. No framework. Edit directly.

## How to make changes

- **Text:** find the words on the page, change them in `index.html`.
- **Images:** hero + about + marquee use CDN URLs (Unsplash, myportfolio.com, etc.) — replace `src=` attributes.
- **Videos:** add `<video autoplay muted loop playsinline>` tags pointing at hosted `.mp4` URLs. Don't commit video files into the repo.
- **Clients:** `.clients-grid` — one `<div class="client-tile">` per brand.
- **Testimonials:** `#testimonial` block. Add more by duplicating the pattern.
- **Contact:** email in `#contact`, Instagram + Shop links in `.social-links`.
- **Founder bio:** `#about` section (photo + copy about Bridget).

## Merch

Merch CTAs point to `https://automatedmerch.onrender.com/creative-legends/shop` — that's hosted separately and managed by the AutomatedMerch team. **Never** try to edit product pages, checkout, or cart code here; it lives in another repo.

If adding a featured-merch grid (like Josh's site has), fetch from:
`https://automatedmerch.onrender.com/api/trpc/products.list?input=...`
with the `creative-legends` templateId (ask Bernardo for the number).

## Deploy

Every commit to `main` auto-deploys to Render (`creative-legends-site.onrender.com`). Check status at https://dashboard.render.com.

When the custom domain (`creativelegends.co`) is wired up at the registrar, Render will serve both URLs simultaneously with free SSL. Note: there is an existing live site at creativelegends.co — the DNS cutover is a switch from her old host, not a new-build.

## What NOT to do

- **Don't** add a build step, framework, or package.json unless absolutely necessary. Simplicity is a feature.
- **Don't** change the merch URLs away from `automatedmerch.onrender.com` — they're absolute on purpose so they work from the custom domain.
- **Don't** commit large binary assets (video files, high-res photos) into the repo. Host them externally (Cloudinary, Vimeo direct, etc.) and reference by URL.
- **Don't** touch anything in the AutomatedMerch monorepo. That's a separate codebase.

## Contact

Site owner: Bridget Farhat — hello@creativelegendsco.com
Platform help: Bernardo — bernardo8605@gmail.com
