# Soutuk Website (`soutuk.pb-aim.com`) — 3-Minute GitHub Pages Deploy Guide

This folder contains a complete, zero-dependency static site ready for **GitHub Pages** and **Google Play Console**:
- `index.html` — Official Soutuk landing page (App overview, Solo vs. Cloud modes, Tiered Picker, 72-Byte `S`-Cryptex story, and Free App vs. Paid Kilonova SDK licensing).
- `privacy.html` — Google Play Store & Generative AI Policy compliant Privacy Policy (`https://soutuk.pb-aim.com/privacy.html`).
- `CNAME` — Pre-configured for **`soutuk.pb-aim.com`**.
- `assets/icon-512.png` & `assets/favicon.png` — Your Gold & Silver `S`-Cryptex (`LISTEN` Sign Tile) emblem.

---

## Step 1 — Push This Folder to a Public GitHub Repository
Create a new public repository on GitHub (for example, `soutuk-site`), then run in PowerShell:

```powershell
cd D:\SoutukAPP\website
git init
git add .
git commit -m "Launch Soutuk official site and Play Store privacy policy"
git branch -M main
git remote add origin https://github.com/<YOUR_GITHUB_USERNAME>/soutuk-site.git
git push -u origin main
```

---

## Step 2 — Add 1 `CNAME` Record in Your `pb-aim.com` DNS (Cloudflare / Registrar)
In your DNS dashboard for **`pb-aim.com`**, add:
- **Type:** `CNAME`
- **Name:** `soutuk`
- **Target:** `<YOUR_GITHUB_USERNAME>.github.io`
- **Proxy Status (if Cloudflare):** Set to **DNS only (gray cloud)** so GitHub Pages can issue and auto-renew its free HTTPS SSL certificate cleanly.

---

## Step 3 — Turn On GitHub Pages
1. Open your GitHub repo → **Settings** → **Pages**.
2. Under **Build and deployment**, set **Source** to **Deploy from a branch** → Branch: `main` / `/ (root)` → **Save**.
3. Under **Custom domain**, `soutuk.pb-aim.com` will auto-populate from `CNAME`. Once DNS verifies (~1–3 minutes), check **Enforce HTTPS**.

---

## URLs to Paste into Google Play Console
- **Developer / App Website:** `https://soutuk.pb-aim.com`
- **Privacy Policy URL:** `https://soutuk.pb-aim.com/privacy.html`
