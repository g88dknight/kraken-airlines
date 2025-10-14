# Kraken Airlines WebAR

Immersive paper plane demonstration that pairs Three.js with MediaPipe hand tracking for a single-page WebAR experience.

## Project Structure
- `paper-plane-ar_9.html` – main WebAR entry point including inline styles and module script.
- `assets/` – static assets used by the experience.
    - `logo-air.svg` – brand mark shown in the UI header.
    - `ico.ico` – site favicon.

## Getting Started
1. Start a local server from the repository root so camera APIs work correctly:
   - `python3 -m http.server 5173`
2. Open `http://localhost:5173/paper-plane-ar_9.html` in Chrome or Edge.
3. Allow camera access and verify gestures (pinch, point, peace, open palm, fist).

## Formatting
- `npx prettier@latest --check paper-plane-ar_9.html`

