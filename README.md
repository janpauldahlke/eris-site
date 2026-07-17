# eris-system.dev

Static landing page for [Eris](https://github.com/janpauldahlke/eris): local-first vault agent.

No build step. No analytics. No cookies.

## Local preview

```bash
python3 -m http.server 8080
# open http://localhost:8080
```

## Deploy: Cloudflare Pages

Use **Pages** (Connect Git), not Workers / `wrangler deploy`.

1. Workers & Pages → Create → Pages → Connect Git → this repo
2. Build command: *(empty)* · Build output directory: `/` or `.`
3. Deploy command: *(empty / none)* — do not set `npx wrangler deploy`
4. Custom domain: `eris-system.dev` (+ `www` → apex)
5. `_headers` in the repo root is applied automatically on Pages

`/*` in `_headers` means “all paths”, not a comment.

## Deploy: GitHub Pages (interim)

Settings → Pages → Deploy from branch → `/` (root).  
Custom domain / Cloudflare can replace this later.

## Assets

| File | Role |
|------|------|
| `assets/eris_logo.svg` | Header mark (circuit glyph, no wordmark) |
| `assets/eris_logo.png` | Full lockup: apple-touch / brand kit |
| `assets/screenshots/web-console-light.png` | Hero screenshot |
| `assets/demo.gif` | Web console session recording |
| `assets/gpu_metrics.png` | Hardware honesty figure |
| `assets/og-image.png` | Open Graph card (1200×630) |
| `assets/favicon.svg` | Favicon |

Eris: [https://en.wikipedia.org/wiki/Eris](https://en.wikipedia.org/wiki/Eris)
