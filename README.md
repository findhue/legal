# findhue/legal

Published legal/support pages for **FindHue** (EduMon Studios), served via GitHub Pages.

Live at: `https://findhue.github.io/legal/` once Pages is enabled (Settings → Pages → Deploy from
a branch → `main` / `/ (root)`).

| Page | Path |
|---|---|
| Privacy Policy | `/privacy.html` |
| Terms of Use | `/terms.html` |
| Community Guidelines | `/community.html` |
| Support | `/support.html` |

## Source of truth

This is a static HTML rendering. The canonical Markdown content this was generated from lives in
the main app repo at `docs/legal/*.md` (private repo — not this one), along with the full evidence
trail (which code/schema/function backs each claim) and the App Store Connect App Privacy data map.
Edit content there first, then re-render/update the HTML here to match.

## Why a separate repo

The main app repo is private; GitHub Pages on a free plan only serves from public repos. This repo
holds nothing but these four static pages — no app code, no configuration, no secrets — so it can
be public without exposing anything else.

## Updating

Plain HTML/CSS, no build step, no JavaScript. Edit the `.html`/`.css` files directly and push to
`main` — GitHub Pages redeploys automatically within a minute or two.

Once live, set the app's `EXPO_PUBLIC_PRIVACY_POLICY_URL` / `_TERMS_URL` /
`_COMMUNITY_GUIDELINES_URL` / `_SUPPORT_URL` env vars (see the app repo's `src/lib/config/legal.ts`)
to this site's real URLs if they differ from its built-in fallback.
