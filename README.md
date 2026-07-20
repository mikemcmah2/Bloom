# Two of Us — Cycle Tracker (v3: real app icon on iPhone)

## What's new

iOS's "Add to Home Screen" requires an actual PNG image — it can't use an SVG for the home-screen icon, which is why the icon wasn't showing before. This version adds real PNG icons at the sizes iOS (and Android/desktop) expect, plus a small web manifest so the name and background color show correctly too.

## Files in this package

Upload **all of these** to the root of your repo (same place as before):
- `index.html` (updated — references the new icon files)
- `bloom-icon.svg` (still used as the browser tab favicon on modern browsers)
- `apple-touch-icon.png` (180×180 — this is the one iOS actually uses)
- `icon-192.png`, `icon-512.png` (used by the web manifest / Android)
- `favicon-32.png`, `favicon-16.png` (fallback browser tab icon)
- `manifest.json` (tells the phone the app's name, colors, and icons)

## After uploading

1. Reload the site once in Safari on the iPhone (to update the cache).
2. Tap the **Share** button → **Add to Home Screen**.
3. The Bloom icon should now appear correctly, both in the "Add to Home Screen" preview and on the home screen itself.

If it still shows a plain/blank icon, remove any previously-added home screen icon for this site first (long-press → Remove), since iOS sometimes caches the old blank one.
