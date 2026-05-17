# DataHub — Personal File Transfer Hub

A zero-backend file hub. Drop files on your PC, access them on your phone via browser.

## How it works

- Files stored in **browser IndexedDB** — no server, no cloud account needed
- A QR code on the page lets you open the same URL on your phone instantly
- Supports any file: PDF, DOCX, XLSX, PPTX, images, ZIPs, MP4, etc.
- Quick note/clipboard for copy-pasting text between devices
- Export all files as a ZIP at any time

> **Note:** IndexedDB is per-browser. Files saved on your PC browser won't auto-appear
> on your phone. Workflow: upload on PC → open URL on phone → download the file.
> This is intentional — no cloud = no account, no leaks, no limits.

---

## Deploy in 5 minutes

### Option A — Cloudflare Pages (recommended, free)

1. Push this folder to a GitHub repo
2. Go to [dash.cloudflare.com](https://dash.cloudflare.com) → Pages → Create project
3. Connect your GitHub repo
4. Build settings: **none** (static site, no framework)
5. Deploy — you get a `.pages.dev` URL instantly

### Option B — GitHub Pages (also free)

1. Push to a GitHub repo
2. Settings → Pages → Source: Deploy from branch `main`, folder `/`
3. Done — available at `https://yourusername.github.io/repo-name`

### Option C — Auto-deploy via GitHub Actions

Add these secrets to your GitHub repo (Settings → Secrets):
- `CLOUDFLARE_API_TOKEN` — from Cloudflare dashboard → API Tokens → Create Token (Pages: Edit)
- `CLOUDFLARE_ACCOUNT_ID` — shown in Cloudflare dashboard sidebar

Every push to `main` will auto-deploy.

---

## File size limits

IndexedDB can hold **hundreds of MB** depending on browser/OS.
Chrome on desktop typically allows up to **60–80% of free disk space**.
For very large files (>500 MB), use the Export ZIP flow.

---

## Privacy

- No data ever leaves your browser
- No analytics, no tracking, no backend
- Clearing browser data deletes all files
