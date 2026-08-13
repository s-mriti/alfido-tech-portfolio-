# Smriti Pandey — Personal Portfolio

A responsive single-page portfolio built with **HTML, CSS and Bootstrap 5**, featuring a fixed
navbar with smooth scrolling, scroll-triggered reveal animations, a reading-progress bar and
active-section highlighting.

## Sections

Home · About · Skills · Projects · Experience · Certifications · Contact

## Tech

- HTML5, CSS3 (custom properties, Flexbox, CSS Grid)
- Bootstrap 5.3 (grid, navbar, collapse) via CDN
- Vanilla JavaScript (IntersectionObserver for animations and scrollspy)
- Google Fonts: Fraunces + Inter
- No build step, no dependencies to install — one file

## Files

```
index.html      the whole site (CSS + JS inlined)
portrait.jpg    optional headshot for the hero; if missing, an "SP" monogram shows instead
README.md
```

## Run locally

Open `index.html` in a browser, or serve it:

```bash
python3 -m http.server 8000
# then visit http://localhost:8000
```

## Deploy to GitHub Pages

1. Create a new **public** repository on GitHub — name it `smriti-portfolio`
   (or `<your-username>.github.io` if you want it at the root domain).
2. Upload `index.html`, `README.md` and `portrait.jpg` — either by dragging them into
   the repo's "Add file → Upload files" page, or from the terminal:

   ```bash
   git init
   git add .
   git commit -m "Add portfolio site"
   git branch -M main
   git remote add origin https://github.com/<your-username>/smriti-portfolio.git
   git push -u origin main
   ```
3. In the repo go to **Settings → Pages**.
4. Under *Build and deployment*, set **Source** to `Deploy from a branch`,
   **Branch** to `main` and folder to `/ (root)`. Save.
5. Wait about a minute. The live site appears at:
   `https://<your-username>.github.io/smriti-portfolio/`

That URL is the "live hosted version" deliverable; the repo URL is the "source code" deliverable.

## Adding the headshot

Drop a photo named exactly `portrait.jpg` next to `index.html`. Portrait orientation
(roughly 4:5) works best. Without it the site still looks complete — it falls back to a
monogram tile automatically.

## Accessibility & performance notes

- Respects `prefers-reduced-motion` — all animations disable for users who ask for that.
- Semantic landmarks, descriptive link text, and keyboard-navigable navbar.
- Single HTML file, ~30 KB before fonts; loads fast on mobile connections.
