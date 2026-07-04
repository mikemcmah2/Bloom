# Two of Us — Cycle Tracker (static version)

No build step. Two files: `index.html` and `bloom-icon.svg`.

## Deploy on GitHub Pages (matches how your other repos are set up)

1. Put `index.html` and `bloom-icon.svg` at the **root** of the repo (same level, not inside a subfolder).
2. Repo **Settings → Pages** → **Source: Deploy from a branch** → branch `main`, folder `/ (root)`.
3. Save, wait ~30–60 seconds, then visit `https://mikemcmah2.github.io/Bloom/`.

That's it — no `npm install`, no build, no GitHub Actions needed.

## How it works

- React, Babel, and Tailwind load from public CDNs at page load, and the page's own script is transformed from JSX to JS right in the browser. This is why there's no build step, at the cost of a slightly slower first load than a bundled app.
- Your password is hashed and stored in `localStorage`; it's a screen against casual snooping, not encryption of the data itself.
- Cycle and intimacy data live in `localStorage` in whatever browser you use — no sync between devices.

## Editing

Everything — logic, styling, and markup — is in `index.html`. Search for the part you want to change (e.g. `SEED_CYCLES` for the starting data, `COLORS` for the palette) and edit directly; refresh the page to see changes, no rebuild required.
