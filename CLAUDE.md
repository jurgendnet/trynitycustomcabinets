# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

Static HTML website for **Trinity Builder LLC** — a custom cabinet company based in Murfreesboro, Tennessee. Deployed to GitHub Pages at `trinitycustomcabinets.com`.

The site is based on the iSTUDIO Bootstrap 5 template (HTML Codex / ThemeWagon), heavily customized for the business.

## Local Preview

No build step — open any `.html` file directly in a browser, or run a quick local server:

```bash
python3 -m http.server 8080
# then open http://localhost:8080
```

## Deployment

Changes are deployed by pushing to the `main` branch on GitHub. GitHub Pages serves the repo root. The `CNAME` file sets the custom domain (`trinitycustomcabinets.com`) and `.nojekyll` disables Jekyll processing.

## Architecture

| Path | Purpose |
|------|---------|
| `*.html` | One file per page (index, about, service, project, feature, team, testimonial, contact, 404) |
| `css/style.css` | All custom styles — edit this for visual changes |
| `css/bootstrap.min.css` | Bootstrap 5 compiled (do not edit) |
| `scss/` | Bootstrap SCSS source — not compiled as part of any automated build |
| `js/main.js` | jQuery-based JS: spinner, sticky nav, back-to-top, Owl Carousel init, WOW.js init |
| `lib/` | Vendored JS/CSS: animate, counterup, easing, owlcarousel, waypoints, wow |
| `img/` | Site images (`.webp` for most, `.jpg` for team/testimonials) |
| `sitemap.xml` | Manual sitemap — update `<lastmod>` dates when pages change |

## SEO & Analytics

- **Google Ads tag**: `AW-17632932395` (in `<head>` of every page)
- **JSON-LD**: Local Business schema on `index.html` — update if business info changes
- **Open Graph / Twitter cards**: defined per page in `<head>`
- **Canonical URLs**: each page has a `<link rel="canonical">` pointing to `https://trinitycustomcabinets.com/<page>.html`
- When adding a new page, add it to `sitemap.xml` and add canonical/OG tags matching the pattern in existing pages

## Business Info (used across pages)

- **Phone**: 615-796-5862
- **Service area**: Murfreesboro, Nashville, Franklin, Smyrna, La Vergne, Lebanon (Middle Tennessee)
- **Domain**: trinitycustomcabinets.com
