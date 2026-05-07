# Aela — PWA Installation Guide

## What's in this package
- `index.html` — the app shell
- `app.jsx` — the full Aela application
- `manifest.json` — PWA manifest (enables "Add to Home Screen")
- `sw.js` — service worker (enables offline use)
- `icon.svg` — the Aela brand mark

## How to install on your phone

### Option 1 — Serve locally (fastest for testing)
You need a simple HTTP server. If you have Python:
```bash
python3 -m http.server 8080
```
Then open `http://YOUR_IP:8080` on your phone (must be on same WiFi).

### Option 2 — Deploy to the web (best for sharing)
Free options that work in minutes:

**Netlify Drop** (easiest):
1. Go to app.netlify.com/drop
2. Drag the entire `aela-pwa` folder onto the page
3. You'll get a URL like `random-name.netlify.app`
4. Open that URL on your phone

**Vercel**:
```bash
npm i -g vercel
cd aela-pwa
vercel
```

**GitHub Pages**:
1. Push this folder to a GitHub repo
2. Enable GitHub Pages in Settings → Pages
3. Select root as source

## Add to Home Screen

### iPhone / iPad (Safari only)
1. Open the app URL in Safari
2. Tap the Share button (box with arrow pointing up)
3. Scroll down → tap "Add to Home Screen"
4. Tap "Add" — Aela appears on your home screen
5. Open it — it runs fullscreen like a native app

### Android (Chrome)
1. Open the app URL in Chrome
2. A banner will appear after a few seconds: "Add Aela to Home Screen"
3. Tap "Install App"
4. OR tap the three-dot menu → "Add to Home Screen"

### Desktop (Chrome / Edge)
1. Look for the install icon (⊕) in the address bar
2. Click it → "Install"
3. Aela opens as a standalone window

## Notes
- The app works offline after first load (service worker caches everything)
- All data is stored locally on your device (localStorage)
- The Anthropic API features (food search, research, explore) require internet
- Your data never leaves your device except for those API calls
