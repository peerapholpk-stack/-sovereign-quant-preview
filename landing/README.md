# SovereignQuant — Landing Page

Single-page marketing site for **SovereignQuant** built with **Nuxt 3 + Tailwind CSS**, optimized for one-click deployment on **Vercel**.

## Stack

- Nuxt 3 (`nitro preset: vercel`)
- Tailwind CSS via `@nuxtjs/tailwindcss`
- `lucide-vue-next` for icons
- Inter + JetBrains Mono (Google Fonts)

## Local Development

```bash
# from this folder
npm install
npm run dev          # http://localhost:3000
```

## Build

```bash
npm run build        # produces .output/ for server deployments
npm run preview      # local preview of production build
```

## Deploy to Vercel

### Option A — Vercel Dashboard (recommended)

1. Push this folder to a Git repository (GitHub / GitLab / Bitbucket).
2. In Vercel, click **"Add New Project"** and import the repo.
3. Set **Root Directory** to `landing` (if this folder sits inside a larger repo).
4. Vercel will auto-detect **Nuxt.js**. Leave defaults:
   - **Build Command**: `nuxt build`
   - **Output Directory**: `.output` (managed by Nitro Vercel preset)
   - **Install Command**: `npm install`
5. Click **Deploy**.

### Option B — Vercel CLI

```bash
npm i -g vercel
vercel             # follow prompts, link project
vercel --prod      # production deploy
```

## Customization Checklist

Before going live, update these placeholders in `app.vue`:

- [ ] Replace Lemon Squeezy checkout URLs:
  - `https://yourstore.lemonsqueezy.com/checkout/buy/sovereign-license`
  - `https://yourstore.lemonsqueezy.com/checkout/buy/enterprise-license`
- [ ] Update contact email in footer (`peeraphol.ka@gmail.com`)
- [ ] Adjust OG/meta description in `nuxt.config.ts` if needed
- [ ] Swap `public/favicon.svg` for your final mark

## Structure

```
landing/
├── app.vue                    # single-page landing (all sections)
├── nuxt.config.ts             # Nuxt + Vercel preset + meta
├── tailwind.config.js         # design tokens
├── assets/css/tailwind.css    # base layer + utilities
├── public/favicon.svg         # favicon
├── package.json
└── tsconfig.json
```

## Sections

1. **Hero** — headline, sub-headline, dual CTAs
2. **Architecture Window** — ASCII diagram in IDE-style card
3. **Core Capabilities** — 3-column grid (Execution · Monte Carlo · Regime)
4. **Pricing** — Sovereign $349 · Enterprise $899
5. **Support & Constraints** — async GitHub support model + financial disclaimer

---

*Light mode only. Stripe / Apple Developer / Notion aesthetic. Zero-friction.*
