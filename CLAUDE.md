# start-end-frame-interpolation

A multi-page static site showcasing a start/end frame video interpolation
experiment made with Google Flow (Veo 3.1 - Lite). There is no build step —
each `.html` page is served as-is.

## Structure

- `index.html` — the showcase page (dark theme, card grid layout, inline CSS).
- `comparison.html` — side-by-side of the generated output vs. the YouTube
  source reference clip (embedded, not downloaded).
- `api.html` — docs + in-browser snippet builder for driving the same
  start/end frame + prompt workflow programmatically via fal.ai or the
  Gemini API (Veo). The builder only formats text client-side; it never
  makes network calls or handles real API keys.
- `cost.html` — what Google Flow, fal.ai, and the Gemini API charge for
  this workflow, plus a client-side calculator. Only the one known figure
  (10 Flow credits per 8s video, from this project's own generation) is
  hardcoded — everything else links to live provider pricing pages since
  rates change.
- `README.md` — project write-up: prompt used, generation choices, output.
- `assets/` — media referenced by the HTML pages and `README.md`:
  - `start-frame.png` — first input frame
  - `end-frame.png` — last input frame
  - `output-animation.mp4` — generated interpolation video
- `.github/workflows/static.yml` — deploys the entire repo to GitHub Pages
  on every push to `main` (no build, just upload + deploy).

## Working on this repo

- Keep the HTML pages dependency-free (no external CDN scripts/fonts) since
  they're deployed as raw static content.
- The four pages share a `.topnav` nav bar and CSS variables — duplicated
  per file rather than templated, since there's no build step. Keep them in
  sync when styling changes.
- If you add or rename files under `assets/`, update `README.md` and every
  HTML page that references them — nothing else builds or checks links.
- Live site: https://rifaterdemsahin.github.io/start-end-frame-interpolation/
