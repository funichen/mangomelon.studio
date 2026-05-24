# MangoMelon Studio Static Site

Static HTML site for **MangoMelon Studio** and **Bumochi**. Zero build, suitable
for GitHub Pages.

## What's here

```
index.html                    # MangoMelon company homepage
bumochi/index.html            # Bumochi landing page
bumochi/privacy/index.html    # Bumochi privacy policy for /bumochi/privacy/
CNAME                         # GitHub Pages custom domain: www.mangomelon.studio
.nojekyll                     # Disable GitHub Pages Jekyll processing
SQUARESPACE-COPY.md           # Copy blocks for updating the current Squarespace site
```

## Preview locally

```bash
# from this folder
python3 -m http.server 4173
# open http://localhost:4173
```

The local URLs should be:

```text
http://localhost:4173/
http://localhost:4173/bumochi/
http://localhost:4173/bumochi/privacy/
```

## Deploy to GitHub Pages

Recommended: publish this folder as its own GitHub repo, for example
`funichen/mangomelon.studio`.

```bash
# one-time setup from this folder
git init
git add .
git commit -m "Initial MangoMelon Studio site"
git branch -M main
git remote add origin https://github.com/funichen/mangomelon.studio.git
git push -u origin main
```

Then in GitHub:

1. Open the repo.
2. Go to `Settings > Pages`.
3. Set source to `Deploy from a branch`.
4. Choose `main` and `/root`.
5. Confirm the custom domain is `www.mangomelon.studio`.
6. Enable `Enforce HTTPS` after GitHub finishes issuing the certificate.

If you keep this folder inside the existing monorepo instead, use a GitHub
Actions workflow or subtree deployment so GitHub Pages publishes this folder
as the site root.

## Squarespace DNS

Keep the domain subscription in Squarespace, but point the DNS records to
GitHub Pages.

Remove Squarespace default website records first, then add:

```text
@     A      185.199.108.153
@     A      185.199.109.153
@     A      185.199.110.153
@     A      185.199.111.153
www   CNAME  funichen.github.io
```

Optional IPv6:

```text
@     AAAA   2606:50c0:8000::153
@     AAAA   2606:50c0:8001::153
@     AAAA   2606:50c0:8002::153
@     AAAA   2606:50c0:8003::153
```

Do not delete email records such as `MX`, `TXT`, SPF, DKIM, or DMARC.

## Before going live

- [ ] Add real App Store / Play Store links when live; current CTAs use `mailto:support@mangomelon.studio`
- [ ] Add the real `og-image.png` (1200×630) at `/bumochi/og-image.png` — see `1-Projects/Kids-Time-Manager/ICON-PROMPT-2026-05-23.md` for the prompt
- [x] Create `/bumochi/privacy/` page
- [x] Add GitHub Pages `CNAME`
- [ ] Create GitHub repo and enable Pages
- [ ] Point Squarespace DNS to GitHub Pages
- [ ] Swap Tailwind CDN for a built CSS file (run `npx tailwindcss -i input.css -o output.css --minify`) before production — CDN is dev-only per Tailwind docs
- [ ] Replace `🐰` emoji phone mockup with a real Flutter app screenshot
- [ ] Set up Plausible or Buttondown if you want privacy-friendly analytics / newsletter

## Design tokens

Copied from the Flutter app's `FocusPetTheme` so the web feels like the same product:

- `coral` = `#FF8A7A`
- `peach` = `#FFE0DC`
- `cream` = `#FFF4E2`
- `ink-primary` = `#3D2E26`
- `ink-secondary` = `#7A6B5F`
- Display font: Fraunces (serif)
- Body font: Nunito (sans)
