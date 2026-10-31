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

Ogden Agents is free and open source under the MIT license, for everyone. There are no paid tiers,
checkout or license keys; the site links straight to `hsmith-dev/ogden-agents` on GitHub.

## Keeping features current

The features section describes what is in the latest release on GitHub. Work that is merged or in
progress but not yet released goes only in the "On the way" section (`#next`), labelled as such.

## Local preview

```bash
python3 -m http.server 8080
```

## Design

Dark-only, with one amber accent and cool-tinted neutrals. Geist for text and Geist Mono for labels and code.
Fonts are self-hosted so the site makes **no third-party requests**. The privacy policy promises that,
so don't add Google Fonts, analytics, or CDN scripts without updating `privacy.html`.
