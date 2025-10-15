# Repository Guidelines

## Project Structure & Module Organization
Kraken Airlines ships as a single-page WebAR experience in `paper-plane-ar_10.html`. The `<style>` block holds UI styling and overlay states; keep shared tokens near the top. The `<script type="module">` block bootstraps Three.js scene setup, MediaPipe Hands detection, and controls. Introduce new helpers as inline modules near the bottom or move them into a future `scripts/` directory and load with `type="module"`. Place future assets under `assets/`.

## Build, Test, and Development Commands
- `python3 -m http.server 5173` from the repo root starts a local server so camera APIs and module imports behave correctly. Open `http://localhost:5173/paper-plane-ar_10.html`.
- `open paper-plane-ar_10.html` (macOS) is fine for quick layout checks, but gesture capture requires HTTPS or localhost.
- `npx prettier@latest --check paper-plane-ar_10.html` verifies formatting before committing.

## Coding Style & Naming Conventions
Indent HTML, CSS, and JS with 4 spaces and align closing tags. Use semantic HTML; reserve Tailwind utility classes for rapid prototypes. Prefer `const` and `let` with `camelCase` identifiers (`planeGroup`, `updateGestureDisplay`). Keep CSS selectors kebab-case and annotate complex gesture or state logic with brief comments.

## Testing Guidelines
Manual testing only for now; run in Chrome or Edge on desktop. Allow camera access, then verify pinch, point, peace, open-palm, and fist transitions while watching the trail renderer respond. Toggle recording to confirm UI state updates. Use `console.log(results.multiHandLandmarks)` temporarily when debugging and remove before committing. Capture short clips for regressions.

## Commit & Pull Request Guidelines
Follow the existing short, imperative commit style (`Add orbit easing`). Group related changes and add bodies when behavior shifts. Pull requests should note user impact, manual test evidence, linked issues, and screenshots or GIFs for UI updates. Mention any new browser or permission requirements.

## Security & Configuration Tips
Three.js and MediaPipe load from CDNs; upgrade intentionally and smoke-test offline fallbacks. Avoid storing camera calibration files or secrets. Re-test first-run flows by clearing browser permission caches before demos.
