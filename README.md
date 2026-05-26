# Password Generator — Solarpunk

A beautiful, Solarpunk-themed password generator. Fully client-side, zero dependencies, zero tracking.

**Live:** [password.mrwuliu.top](https://password.mrwuliu.top)

## Features

- **Cryptographically secure** — uses `crypto.getRandomValues()` for randomness
- **Bilingual** — Chinese / English toggle (🌐)
- **Customizable** — length slider (8–64), uppercase / lowercase / numbers / symbols toggles
- **Exclude characters** — filter out confusing chars like `iIl1o0O`
- **Strength indicator** — Weak → Medium → Strong → Very Strong
- **Generation history** — keeps last 100 records in `localStorage`
- **One-click copy** — copies to clipboard with visual feedback
- **Responsive** — desktop, tablet, and mobile layouts
- **Zero dependencies** — single HTML file, inline CSS + JS, no build step

## Tech Stack

- Vanilla HTML / CSS / JavaScript
- Deployed on [Cloudflare Workers](https://workers.cloudflare.com/) (static assets)
- CI/CD via GitHub Actions — push a `v*` tag to deploy

## Deployment

```bash
# Tag a new release to trigger deployment
git tag v1.0.0
git push origin v1.0.0
```

GitHub Actions workflow (`.github/workflows/deploy.yml`) will:
1. Build static assets into `dist/`
2. Deploy to Cloudflare Workers via `wrangler`

### Required GitHub Secret

| Secret | Description |
|--------|-------------|
| `CLOUDFLARE_API_TOKEN` | Cloudflare API token with Workers deployment permissions |

## License

MIT
