# Iván García — Portfolio

Personal portfolio site for Iván Felipe García Sánchez — Technical Director at Globant, specializing in mobile engineering and applied AI.

**Live site:** [ivanfgarcias.dev](https://ivanfgarcias.dev)

## Stack

Single self-contained `index.html` — no build step, no framework, no dependencies. CSS and JS are inlined directly in the file. This keeps the site fast, easy to deploy anywhere, and simple to edit without tooling.

## Structure

```
index.html              Entire site: markup, styles, and behavior
CNAME                    Custom domain config for GitHub Pages (ivanfgarcias.dev)
assets/
  icons/                 App icons for the iOS/Android app cards
  screenshots/           Screenshots for the Archive section (legacy apps)
```

## Sections

1. **Hero** — name, role, and a fact list (experience, focus, education, location)
2. **Experience** — career timeline at Globant plus earlier roles (YellowPepper, Mercadoni, Tappsi)
3. **Skills** — grouped skill chips (mobile, AI/data, engineering, leadership)
4. **Apps** — current published apps on the App Store and Google Play, pulled with real icons and descriptions
5. **Archive** — earlier/legacy apps no longer in the stores (Astral Numerology, Golera, Mercadoni)
6. **Education & Languages**
7. **Contact** — footer with email

## Local development

No build step required. Open `index.html` directly in a browser, or serve it locally:

```bash
python3 -m http.server 8000
```

Then visit `http://localhost:8000`.

## Theming

The site supports light and dark mode: it follows the OS/browser preference by default, with a manual toggle in the nav (persisted via `localStorage`). All colors are defined as CSS custom properties in `:root`.

## Deployment

Hosted on **GitHub Pages**, served from the `main` branch root, with a custom domain configured via the `CNAME` file and DNS records pointed at GitHub's Pages IPs. Pushing to `main` deploys automatically — no CI config needed beyond what GitHub Pages provides out of the box.

## Updating content

- **Experience / Skills / Education** — edit the corresponding `<section>` directly in `index.html`.
- **Apps section** — each app is an `.app-card` block with an icon (`assets/icons/`), tagline, description, and store link.
- **Archive section** — each entry is an `.archive-card` with a `.shot-frame`; if a screenshot file referenced under `assets/screenshots/` is missing, it falls back to a "screenshot coming soon" placeholder automatically (no broken image icons).

## Pending

- Archive screenshots not yet added: `assets/screenshots/astral-numerology.png`, `assets/screenshots/golera.png`, `assets/screenshots/mercadoni.png`.
