# Agent Operations — study PWA

An installable, offline-capable study app for the "Agent Operations" curriculum: a four-tier course on moving from writing code to directing agents that write it.

Live: served via GitHub Pages from this repo's `main` branch.

## Install on mobile

Open the live URL in Chrome (Android) or Safari (iOS), then:
- **Android/Chrome:** menu → "Add to Home screen" / "Install app"
- **iOS/Safari:** share icon → "Add to Home Screen"

Once installed, it launches full-screen with no browser chrome and keeps working with zero connection — the service worker caches the whole app on first load.

## Local dev

No build step. Any static file server works:

```bash
python3 -m http.server 8000
```

Progress ("mark done" per module) is stored in `localStorage`, per-device.

## Tech stack

- Vanilla JavaScript Progressive Web App (PWA) with no build step
- Offline‑first service worker (`sw.js`) for caching
- Web app manifest (`manifest.json`) for installability
