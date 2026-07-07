# Third Night Selections

Wine, spirits, and stories from places worth staying.

A single-page static website for Third Night Selections — a Washington, DC
venture in small-lot wine, spirits, food, travel, content, and consumer
technology.

## Structure

```
docs/                 ← the published site (GitHub Pages serves this folder)
  index.html          ← the entire site: inline CSS + JS, no build step
  .nojekyll           ← tells Pages to serve files as-is
  images/             ← photography, logo (transparent PNGs), favicon
assets/
  third-night-logo.png ← original master logo (not published)
```

The site is one self-contained HTML file. No framework, no build, no
dependencies — open `docs/index.html` in any browser and it runs.

## Preview locally

```bash
open docs/index.html                 # quickest
# or serve it (mirrors GitHub Pages)
cd docs && python3 -m http.server 8000   # → http://localhost:8000
```

## Deploy (GitHub Pages)

1. Push this repo to GitHub.
2. **Settings → Pages → Source: “Deploy from a branch” → Branch `main`, folder `/docs` → Save.**
3. The site publishes at `https://<user>.github.io/<repo>/` within a minute.

Image paths are relative, so it works at that subpath or on a custom domain.

### Custom domain

Add a file `docs/CNAME` containing `thirdnightselections.com`, point the
domain’s DNS at GitHub Pages, and set the domain under Settings → Pages.

## Editing

Everything lives in `docs/index.html`. Section content is plain HTML near the
top of `<body>`; styling is the `<style>` block in `<head>`; the small amount of
behavior (parallax, scroll reveals, mobile menu, signup form) is the `<script>`
at the end.
