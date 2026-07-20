# Two of Us — Cycle Tracker (v2: mood phase + timeline)

Two files: `index.html` and `bloom-icon.svg`. No build step, no Babel, no Tailwind — JSX is pre-compiled to plain ES5 JavaScript, same approach as the last working version.

## What's new in this update

- **Mood is now a multi-day phase, not a single day.** Log every day the mood lasts (as many as you need) — each one is its own entry, and nothing gets overwritten. The app automatically figures out which upcoming period each mood day belongs to by finding the earliest logged mood day before that period's bleeding start.
- **Fixes the "29 days" bug**: previously, logging a mood day before that cycle's bleeding start had been recorded could silently overwrite an unrelated earlier cycle's mood day and badly skew the prediction. That's no longer possible — mood days are stored independently and grouped automatically.
- **New Timeline tab**: shows every single thing you've ever logged — bleeding starts, ovulation, mood days, intimacy — in one chronological list, each with a small × button to delete a mistaken entry.
- Home screen now shows "Mood phase" instead of "Mood day," including a live indicator if you're currently mid-phase (e.g. "day 2, started Wed").

## If your existing data has the July mix-up

Deploying this update won't automatically fix mood days that got tangled up under the old logic. After updating:
1. Open the **Timeline** tab.
2. Delete any mood-day entry that looks wrong (e.g. one attached to the wrong month).
3. Re-log the correct days from the **Log** tab (you can pick any past date).

## Deploy on GitHub Pages

1. Put `index.html` and `bloom-icon.svg` at the **root** of the repo.
2. Repo **Settings → Pages** → **Source: Deploy from a branch** → branch `main`, folder `/ (root)`.
3. Wait ~30–60 seconds, then reload your Pages URL.

## Notes

- Password is hashed and stored in `localStorage`; it deters casual snooping, it isn't encryption.
- Data lives in `localStorage` in whatever browser you use — no sync between devices.
- If anything ever fails to load, the page shows the exact error as readable text instead of staying blank.
