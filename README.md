# findhue/legal

**Canonical legal/support content for FindHue** (EduMon Studios LLC). This repo holds the source
text; the live, public pages are served from the main website at **gofindhue.com**, not from here.

| Document | Canonical gofindhue.com URL | Source file in this repo |
|---|---|---|
| Legal & Support landing page | `https://gofindhue.com/legal` | generated — see `content/README` note below |
| Privacy Policy | `https://gofindhue.com/privacy` | `content/privacy-policy.md` |
| Terms of Use | `https://gofindhue.com/terms` | `content/terms-of-use.md` |
| Community Guidelines | `https://gofindhue.com/community-guidelines` | `content/community-guidelines.md` |
| Support | `https://gofindhue.com/support` | `content/support.md` |

## Where to make an edit

**Edit the Markdown in `content/*.md` in this repo. Never edit HTML in the `findhue-web` repo by
hand, and never re-introduce a second copy of this text anywhere else.**

After editing `content/*.md` here:

1. Switch to the `findhue-web` repo (the gofindhue.com site).
2. Run `node scripts/build-legal.mjs` there (it reads this repo's `content/` directory — see its
   own README's "Legal/support content" section for the exact command if the two repos aren't
   sibling checkouts on your machine).
3. Commit the regenerated `public/legal/`, `public/privacy/`, `public/terms/`,
   `public/community-guidelines/`, `public/support/` output in `findhue-web` in the same change as
   the `content/*.md` edit here, so the two repos never drift out of sync.

This repo has no build step of its own and does not render the live pages — it is the one place the
actual legal text is written and reviewed, with full edit history.

## `content/*.md` format

Plain Markdown with a short frontmatter header:

```
---
title: Privacy Policy
description: One-sentence summary used as the page's meta description.
slug: privacy
updated: October 2, 2026
---

## A heading

A paragraph. **Bold**, [links](/other-page), lists, and tables all work. An explicit heading id
can be set with `## Heading text {#custom-id}` when something elsewhere links to it by anchor;
otherwise one is generated automatically from the heading text.
```

Internal links between the four documents should use the real gofindhue.com paths directly
(`/privacy`, `/terms`, `/community-guidelines`, `/support`, `/legal`), since that's where they're
actually published.

## Why this repo still exists, separately from `findhue-web`

Keeping the legal source text in its own small repo — separate from both the private FindHue app
repo and the `findhue-web` marketing/invite site — gives it a clean, focused edit history
independent of either, without needing a CMS, a submodule, or any tooling beyond plain Markdown
files for four documents.

## This repo's own HTML pages are legacy redirects now

`index.html`, `privacy.html`, `terms.html`, `community.html`, and `support.html` in this repo's root
are **not** the canonical pages anymore — they're minimal redirect stubs (meta-refresh + canonical
tag + `noindex` + a visible fallback link) kept only so that old bookmarks, cached App Store
metadata, and search results pointing at `findhue.github.io/legal/...` keep working. GitHub Pages
on a static repo like this one can't issue a true server-side HTTP redirect for an existing path, so
a client-side meta-refresh is the most reliable mechanism available here. Each one points at its
gofindhue.com equivalent:

| Legacy URL | Redirects to |
|---|---|
| `findhue.github.io/legal/` (`index.html`) | `https://gofindhue.com/legal` |
| `findhue.github.io/legal/privacy.html` | `https://gofindhue.com/privacy` |
| `findhue.github.io/legal/terms.html` | `https://gofindhue.com/terms` |
| `findhue.github.io/legal/community.html` | `https://gofindhue.com/community-guidelines` |
| `findhue.github.io/legal/support.html` | `https://gofindhue.com/support` |

Do not restore real content to these five files — editing them would recreate exactly the
two-copies-of-the-same-policy problem this restructuring fixed. Edit `content/*.md` instead.

## Publishing

Still GitHub Pages, `main` / `/ (root)`, unchanged. `.nojekyll` stays so none of `content/`'s
frontmatter-leading Markdown is ever run through Jekyll processing.
