# Ogden — Marketing Site

The public landing page for Ogden. It lives in a **separate repo from the app itself** because it's a sales surface, not the product.

Plain static files with no build step, framework, or backend. It deploys anywhere that serves static files and is currently on GitHub Pages at **ogden.harrisonsmith.ai** (see `CNAME`).

```
index.html      landing page (features, deployment, licensing)
setup.html      setup guide
privacy.html    privacy policy (draft)
terms.html      terms & conditions (draft)
404.html        not-found page (GitHub Pages picks this up automatically)
styles.css      all styles
site.js         scroll reveals, tile spotlight, doc TOC highlighting
favicon.svg
fonts/          Geist + Geist Mono variable fonts (SIL OFL 1.1), self-hosted
```

## Licensing model shown on the site

- **Individuals**: free for personal, single-user use. "Request access" is a `mailto:` asking for the
  person's GitHub username, and we invite them to the release repo by hand.
- **Organizations**: paid self-host license following `LICENSE.txt` in the release repo
  (`hsmith-dev/ogden-ai-agent-release`): Small Business (≤25 users), Large Business (≤1,100),
  Enterprise (unlimited). Includes 12 months of releases/support, with optional renewal at 30% of the price paid.
  Delivery is by private repo invite.

The organization "Buy license" buttons point at live Stripe Payment Links. If you regenerate them,
update the three `href`s in the `#license` section of `index.html`. **Only put prices on the
organization tiers.** Keep the individual tier free of any cost wording.

## Local preview

```bash
python3 -m http.server 8080
```

## Design

Dark-only, with one amber accent and cool-tinted neutrals. Geist for text and Geist Mono for labels and code.
Fonts are self-hosted so the site makes **no third-party requests**. The privacy policy promises that,
so don't add Google Fonts, analytics, or CDN scripts without updating `privacy.html`.
