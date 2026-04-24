# BP Daily — Legal pages

Public privacy policy and terms of service for the BP Daily mobile app.
Hosted as a static site via GitHub Pages.

## Files

- `privacy.md` — Privacy Policy
- `terms.md` — Terms of Service
- `index.md` — landing page
- `_config.yml` — Jekyll config for GitHub Pages

## Before publishing — fill in placeholders

Open `privacy.md` and `terms.md` and replace:

- `[YOUR FULL NAME]` — your full legal name (or company name if you're
  publishing through a legal entity). Appears in the "data controller" and
  "developer" fields.
- `[YOUR COUNTRY / JURISDICTION]` — governing-law country (in `terms.md`,
  §12). If you're an individual Google Play developer in Russia, write
  "the Russian Federation". If you have a different arrangement, adjust
  accordingly.

Both files currently list `nazmievjob@gmail.com` as the contact email. Change
if needed.

## Publishing on GitHub Pages (one-time, ~5 min)

1. Create a new **public** GitHub repo. Suggested name: `bp-daily-legal`.
2. Copy the contents of this folder to the repo root.
3. Commit and push to `main`.
4. In the repo on GitHub: **Settings → Pages**.
5. Under "Build and deployment", set:
   - **Source:** Deploy from a branch
   - **Branch:** `main` / `(root)`
6. Save. Wait ~60 seconds.
7. Your pages will live at:
   - `https://<YOUR-GITHUB-USERNAME>.github.io/bp-daily-legal/privacy/`
   - `https://<YOUR-GITHUB-USERNAME>.github.io/bp-daily-legal/terms/`

## Using these URLs

- **Google Play Console → Store listing → Privacy policy URL:** paste the
  `/privacy/` URL.
- **In-app links:** Settings → "Privacy Policy" and "Terms of Service"
  should open the URLs via `url_launcher`. The paywall sheet footer should
  do the same. (Implementation pending on the app side.)

## Updating a document

1. Edit `privacy.md` or `terms.md`.
2. Update the "Last updated" date at the top of the file.
3. Commit and push. GitHub Pages rebuilds automatically within ~1 min.
4. If the change is material (e.g. a new data-processing activity), also
   announce it in-app and give users a chance to review before it takes
   effect.

## Migration to a custom domain (later)

When you buy a brand domain (e.g. `bpdaily.app`), point a subdomain like
`legal.bpdaily.app` at GitHub Pages (CNAME record), add a `CNAME` file at
the repo root with that hostname, and update the URLs in Google Play
Console and the app. Old URLs will 301-redirect automatically.
