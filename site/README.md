# Quetzal website

Static site: `index.html`, `style.css`, `images/`. No build step and no external requests. All paths are relative, so it works under `https://ffkoide.github.io/quetzal-app/` and under any custom domain later.

Published by GitHub Pages through `.github/workflows/pages.yml` on every push to `main` that touches `site/` (or by hand from the Actions tab). One-time setup: Settings → Pages → Source: **GitHub Actions**.

Preview locally: `python3 -m http.server -d site 8000`, then open <http://localhost:8000/>.

Before the first release: point the Download button at the DMG of the release, remove the "Not released yet" notice, and replace `images/*.png` (test renders) with real screenshots.
