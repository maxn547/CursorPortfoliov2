# Portfolio — Max Nicholson

Personal portfolio site for Max Nicholson, workplace operations lead at Airtable.

The whole site is a single self-contained file, `index.html`. Markup, styles, and
scripts all live in that one file, and there are no build steps, dependencies, or
external assets beyond two Google Fonts.

## Running it locally

Open `index.html` directly in a browser, or serve the folder if you want a real
HTTP origin:

```bash
python3 -m http.server 3000
```

Then visit http://127.0.0.1:3000.

## Deploying

Any static host will serve this as-is. For GitHub Pages, enable Pages on the
repository and point it at the `main` branch root; `index.html` is already named
correctly to be served automatically.

## Notes on the build

- **Theme** — light and dark, following the system preference on first visit and
  remembering the choice in `localStorage` after that.
- **Motion** — scroll reveals, count-up numerals, a parallax gradient, and the
  animated pipelines are all driven by `IntersectionObserver` and CSS transitions.
  Everything collapses to a static layout under `prefers-reduced-motion: reduce`.
- **Colour** — one warm charcoal at varying opacity supplies every neutral, and a
  five-stop spectrum (sky, blue, pink, red, orange) supplies every accent. In light
  mode the paler accents are mixed toward the ink so small text clears WCAG AA.
