# The Daily Log

A quiet, single-file habit tracker. No accounts, no backend, no telemetry. Open it in a browser, define your habits, log your days. Everything saves to your own browser.

Live demo: _your URL once deployed_

---

## What it does

- Track any number of habits, of four kinds:
  - **Yes/no** — did it or didn't
  - **Counter** — count toward a daily target
  - **Yes/no with a note** — for things you want to document (e.g. "did one hard thing today")
  - **Multi-choice** — three options, where the first means "didn't do it" (e.g. None / Light / Heavy)
- Daily check-in with a calm, editorial layout
- Dashboard with weekly, monthly, quarterly, and all-time views
- Heatmap calendar, per-habit consistency bars, current streak, completion rate, "vs prior period" deltas
- A running log of all the documented notes from your "yes/no with note" habits
- Export and import your data as JSON
- Configure everything: log title, habit list, habit types, targets, options

## Use cases

- Daily habit accountability
- Weekly/monthly review of practice
- Recording one hard thing per day, with the documented log doubling as a personal archive of what you've pushed yourself to do
- Any small set of practices you want to do consistently and look back on

## How to use it

1. Open the deployed URL (or `index.html` locally in a browser)
2. On first run, pick a starter pack or build your own habits in Settings
3. At night, open it and tap through the day's check-in
4. Anytime, switch to Month / Quarter / All-Time tabs to see how you're trending

Your data lives in your browser's localStorage tied to that URL. Different browser or different device = different log. Use Export and Import to move data between them.

## Deploy your own copy

This is one HTML file with no build step. Two simple options:

### Option A — Netlify (free, recommended)

1. Fork or download this repo
2. Sign up at [netlify.com](https://www.netlify.com) (free)
3. Click **Add new site → Import from Git** and connect your fork, or use **Drop** and drag the `index.html` file in
4. You'll get a permanent URL like `your-name.netlify.app`
5. Open that URL on your phone, tap Share → Add to Home Screen, and it behaves like an app

### Option B — GitHub Pages (free)

1. Fork this repo
2. Repo Settings → Pages → Deploy from branch → main → root → Save
3. URL will be `your-username.github.io/daily-log`

### Option C — Just open the file

Download `index.html`, double-click. Works in any browser. No deploy needed if you only ever use it on one device.

## Customizing

Everything user-facing is configurable in the Settings panel — log title, subtitle, and the full list of habits.

If you want to change deeper things (color palette, fonts, layout), they live as CSS variables at the top of the `<style>` block in `index.html`. Search for `:root`.

## Tech

- Single HTML file, ~2000 lines
- Vanilla JS, no frameworks, no build tools
- Fonts: Fraunces (display) and IBM Plex Mono (numerals) via Google Fonts
- Storage: `localStorage`
- No external dependencies beyond the two webfonts
- Works offline once loaded

## Privacy

There's no server. Nothing leaves your browser. The site doesn't track you, doesn't have analytics by default, doesn't know who you are. If you fork it, the same applies to your fork. Anyone who visits your deployed URL gets their own private log in their own browser.

## License

MIT. Do whatever you want with it.

## Credits

Built as a small piece of personal infrastructure. If you fork it, no need to credit — but if it changes how you log your days, that'd be nice to hear about.
