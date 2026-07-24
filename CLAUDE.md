# start-end-frame-interpolation

A single-page static site showcasing a start/end frame video interpolation
experiment made with Google Flow (Veo 3.1 - Lite). There is no build step —
`index.html` is served as-is.

## Structure

- `index.html` — the showcase page (dark theme, card grid layout, inline CSS).
- `README.md` — project write-up: prompt used, generation choices, output.
- `assets/` — media referenced by both `index.html` and `README.md`:
  - `start-frame.png` — first input frame
  - `end-frame.png` — last input frame
  - `output-animation.mp4` — generated interpolation video
- `.github/workflows/static.yml` — deploys the entire repo to GitHub Pages
  on every push to `main` (no build, just upload + deploy).

## Working on this repo

- Keep `index.html` dependency-free (no external CDN scripts/fonts) since it
  is deployed as raw static content.
- If you add or rename files under `assets/`, update both `README.md` and
  `index.html` references together — nothing else builds or checks links.
- Live site: https://rifaterdemsahin.github.io/start-end-frame-interpolation/
