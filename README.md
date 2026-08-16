# Ogden — Marketing Site

The public-facing landing/pricing page for Ogden — deliberately a **separate
repo from the app itself** (`ogden-aiagents`), since this is a sales surface,
not the product.

A single self-contained static page: `index.html` + `styles.css`. No build
step, no framework, no backend — it doesn't need one. Deploy it anywhere that
serves static files (GitHub Pages, Netlify, Vercel, Cloudflare Pages, an S3
bucket, or a one-line `nginx` container). Intended domain:
**ogden.harrisonsmith.ai** (a subdomain of the main `harrisonsmith.ai` site,
not yet pointed anywhere as of this writing) — whichever static host you
land on, add a CNAME/ALIAS record for `ogden` pointing at it.

## Scope: self-host only, for now

This site sells exactly one thing: a one-time self-host license (source +
deployment files, delivered as a private GitHub repo invite). There is no
Ogden Cloud / hosted offering here — running a hosted product is a real
ongoing DevOps and cost commitment that isn't being taken on right now.
The backend still has the Cloud billing/provisioning code (`billing.py`'s
`fulfill_cloud_subscription`, the Postgres-backed multi-tenant tier, etc.)
so nothing was removed there — it's just not being marketed or sold on
this site until that changes.

## Before you deploy this for real

- **Self-host license "Buy license" buttons** already point at real, live
  Stripe Payment Links (Single User $500 / Small Business $3,000 / Large
  Business $10,000 / Enterprise $25,000). If you ever regenerate these in
  the Stripe dashboard, update the four `href`s in the pricing section.
- **Favicon** is an inline SVG placeholder (a simple crew-manifest glyph) —
  swap for a real logo mark whenever you have one.

## Local preview

No build tooling needed — just open `index.html` in a browser, or serve it:

```bash
python3 -m http.server 8080
```

## Design

Dark, single-theme "command deck / crew manifest" aesthetic (see
`styles.css`'s header comment for the full rationale) — Archivo for display
type, Work Sans for body copy, IBM Plex Mono for labels/pricing/data, one
amber accent. Deliberately not a light/dark toggle: the concept only reads
correctly against a dark ground.
