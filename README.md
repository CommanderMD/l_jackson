# Laila Jackson — Tigers Dance Team Fundraiser (l_jackson)

One-page fundraising site for Laila Jackson's 2026–2027 Arlington Middle School
Tigers dance team season — covering travel, uniforms, and monthly fees across
regionals (Memphis), state (Knoxville), and nationals (Florida). Hosted on
Cloudflare Workers (static assets).

**Dev URL (after deploy):** `https://l-jackson.<your-account-subdomain>.workers.dev`
(Worker name is `l-jackson` — Cloudflare doesn't allow underscores; GitHub repo is `l_jackson`.)

## Edit the fundraising goal / amount raised

In `public/index.html`, find the progress bar line:

```html
<div class="bar" id="bar" data-raised="0" data-goal="5000">
```

Change `data-raised` and `data-goal` to the real numbers, then push. The bar,
percentage, and the "Raised / Goal" figures all update automatically.

## Payment

- Zelle QR (official, from Tynesha Jackson's banking app): `public/assets/zelle-qr.png`
- Zelle / Apple Pay number: (901) 707-0225 — recipient Tynesha Jackson
- A "Copy" button copies the number; donors are prompted to add a note "Laila dance".

## Assets

Processed copies live in `public/assets/` (hero.jpg, photo-1.jpg, photo-2.jpg,
dance.mp4, zelle-qr.png). Source originals (`*.mov`, `image*.jpeg`, the screenshot)
stay in the project root but are git-ignored to keep the repo lean.

Photo credit: the action shot is courtesy of Tammy McKinnon Photography — confirm
permission to use it publicly.

## Deploy

```bash
git add -A && git commit -m "..." && git push
```
Cloudflare Workers Builds auto-deploys on push to `main`.

```bash
npm install && npm run dev   # local preview
```
