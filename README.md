# Tita Maricar's Carinderia — Website

Static marketing site for Tita Maricar's Carinderia (Panciteria & Lutong Ulam) in Calo, Bay, Laguna. No build step, backend, CMS, login, or payment system.

## Structure

```
tita-maricar-website/
├── index.html          ← page markup + all text
├── css/styles.css      ← styles + design tokens
├── js/main.js          ← sticky nav, mobile menu, scroll reveals (vanilla JS)
├── img/
│   ├── hero/           ← hero photo
│   ├── trays/          ← made-to-order photos
│   ├── logo/           ← logo + favicon/app icons
│   └── og-image.png    ← link-preview image
├── favicon.ico
├── site.webmanifest    ← app name + icons
├── EDITABLE-CONTENT.md ← how to update text/photos/links
└── README.md
```

All asset paths are **relative**, so the site works correctly when deployed at a domain root *or* under a sub-path (e.g. a project page on a free host).

## Open locally

Opening `index.html` directly works, but the Google Map embed and web-font/manifest behave best over `http://`. Quick local server:

```bash
# from inside tita-maricar-website/
python -m http.server 8080
# then open http://localhost:8080
```

## Before publishing

Open `EDITABLE-CONTENT.md` and replace the placeholders (search `EDIT:` in `index.html`):
Instagram + TikTok links, phone number, exact address + map location, and confirm the daily ulam / tray lists and photos.

## Deploy to GitHub Pages (free)

1. Create a new GitHub repository.
2. Upload the **contents** of this `tita-maricar-website` folder (so `index.html` is at the repo root).
3. `Settings` → `Pages` → Build and deployment → **Deploy from a branch**.
4. Choose the `main` branch and `/ (root)` folder. Save.
5. Your site publishes at `https://<username>.github.io/<repo>/` after a short wait. Because paths are relative, the favicon, icons, and images all resolve under that sub-path.

## Deploy to Netlify (free)

1. Sign in to Netlify → `Add new site` → `Deploy manually`.
2. Drag this `tita-maricar-website` folder into the upload area.
3. Netlify publishes it and gives you a free `*.netlify.app` address.

## Favicon / logo

The browser-tab icon and app icons are generated from the logo and live in `img/logo/` + `favicon.ico` + `site.webmanifest`. To change the logo, see the "Replacing the logo" section in `EDITABLE-CONTENT.md`.
