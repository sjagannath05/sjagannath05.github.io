# Repository Guidelines

## Project Structure & Module Organization
- Root pages: `index.html`, `generic.html`, `elements.html` drive the site.
- Blog: `blog/` contains listing and templates; images under `blog/images/`.
- Assets: `assets/css/` (compiled CSS), `assets/js/` (theme scripts), `assets/sass/` (source `.scss`), `assets/webfonts/` (icons).
- Images: `images/` stores site visuals referenced by root pages.

## Build, Test, and Development Commands
- Serve locally: `python3 -m http.server 4000` (open http://localhost:4000/).
- Sass (optional): `sass assets/sass/main.scss assets/css/main.css --style=compressed` and `sass assets/sass/noscript.scss assets/css/noscript.css --style=compressed`.
- Quick link check: `rg -n "href=|src="` to review added links/assets.

## Coding Style & Naming Conventions
- HTML: follow existing tab indentation and semantic tags; wrap lines reasonably (~100–120 chars).
- CSS/Sass: use `assets/sass/` as the source of truth; keep variables/mixins in `libs/`, page/layout rules in `layout/` and `components/`.
- JS: keep small utilities in `assets/js/`; avoid adding build steps—use plain, modern JS compatible with the theme.
- Filenames: lowercase, hyphen-separated (e.g., `my-section.html`, `hero-image.jpg`).

## Testing Guidelines
- Manual QA: load pages locally, verify no console errors, and check responsive behavior across breakpoints (xsmall → xlarge).
- Navigation: ensure all internal anchors (`#...`) and blog links resolve and scroll correctly.
- Assets: confirm new images are optimized and paths are correct under `images/` or `assets/...`.

## Commit & Pull Request Guidelines
- Commits: imperative, present tense with scope. Examples:
  - `blog: add single post template`
  - `assets: tweak main.scss colors`
- PRs: concise summary, screenshots/GIFs for visual changes, linked issue (if any), and notes on assets added/removed. Verify GitHub Pages renders correctly after merge.

## Security & Configuration Tips
- Do not commit secrets or tokens; this is a public static site.
- Respect third‑party licenses (HTML5 UP theme in use); keep attributions intact.
- Keep dependencies vendored (fonts, JS) and prefer HTTPS for all external links.

