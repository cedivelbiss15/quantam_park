# Quantum Park — Resident Information Site

A single-page, mobile-first informational website for the proposed Quantum Park
project in Lewisburg, Marshall County, Tennessee.

## Deploy

This is a static site — no build step. Serve the folder, or push to GitHub Pages:

1. Commit `index.html` and the `assets/` folder to your repo.
2. In **Settings → Pages**, set the source to your branch root.
3. The site is served at the Pages URL.

Open `index.html` locally for a quick look (the site plan renders best when
served over http, e.g. `python3 -m http.server`).

## Files

- `index.html` — the entire site (HTML, CSS, and JS inline).
- `assets/` — images, the Volunteer Materials logo/icon, and the subdivision
  plat PDF (`site-plat.pdf`, rendered on-page via pdf.js from a CDN).

## Notes

- **Question form** posts to Formspree (endpoint `mvzngeqp`), delivering to
  info@madeformarshall.com. If the service is unreachable it falls back to the
  visitor's email app. The form ID lives in the `FORMSPREE_ID` constant near
  the bottom of `index.html`.
- **Google Analytics** (GA4 `G-NL3SWER6D3`) is installed in the `<head>`.
- The site plan is drawn from `assets/site-plat.pdf` using pdf.js loaded from
  jsDelivr, so the page needs internet access to render the plan and submit the
  form. Everything else works offline.
