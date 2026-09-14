# kartavyeah.com — KARTAVYEAH! studio site

Static single page. No build step: open `index.html` or serve the folder.

```bash
cd ~/Desktop/Github/kartavyeah.com && python3 -m http.server 8080
# → http://localhost:8080
```

## Links (one place)

All Shabdkhoj links are driven by the `SHABDKHOJ_URL` const at the bottom of
`index.html`. Currently `https://shabdkhoj.kartavyeah.com` (planned subdomain).
Swap in the Cloud Run web-service URL any time — every button updates at once.

## Assets

- `assets/shabdkhoj.png` — real gameplay capture from Shabdkhoj-web (1280×633).
  Re-capture: run Shabdkhoj-web dev server (proxied API), play a guess, screenshot.
- `assets/logo-combo-dark.svg` — master lockup (V3 runner mark + KARTAVYEAH!
  wordmark). Also inlined in the nav of `index.html` (IDs prefixed `lg`
  to avoid collisions).
- `assets/mark-k-solid.svg` — the V3 runner mark alone; also the favicon.

## Deploy (suggested)

Any static host: GitHub Pages / Cloud Storage + CDN / Cloud Run (nginx).
Custom domain: `kartavyeah.com`; map `shabdkhoj.kartavyeah.com` → Shabdkhoj-web
Cloud Run service when ready.
