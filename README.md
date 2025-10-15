# Kraken Airlines WebAR

Immersive paper plane demonstration that pairs Three.js with MediaPipe hand tracking for a single-page WebAR experience.

## Project Structure
- `paper-plane-ar_9.html` – main WebAR entry point including inline styles and module script.
- `assets/` – static assets used by the experience.
    - `logo-air.svg` – brand mark shown in the UI header.
    - `ico.ico` – site favicon.

## Getting Started
1. Install dependencies: `npm install`
2. Start a local dev server: `npm run dev`
3. Open `http://localhost:5173/paper-plane-ar_9.html` in Chrome or Edge.
4. Allow camera access and verify gestures (pinch, point, peace, open palm, fist).

## Formatting
- `npm run format`

## Deployment
- Vercel rewrites the root route to `paper-plane-ar_9.html` via `vercel.json`.
