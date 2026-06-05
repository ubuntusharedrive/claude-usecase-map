# The Claude Usecase Map

A single-file, offline-capable reference for choosing the right **Claude model**, **effort level**, and **thinking** setting for a given task — and seeing roughly how much usage each combination burns before you commit to it.

Built as one self-contained `index.html`. No build step, no dependencies, no tracking. Open it in any browser, pin the tab, and go.

![status: maintained](https://img.shields.io/badge/status-maintained-5fcf8e) ![license: MIT](https://img.shields.io/badge/license-MIT-79b8ff) ![no dependencies](https://img.shields.io/badge/dependencies-none-c792ea)

**Live version:** https://ubuntusharedrive.github.io/claude-usecase-map/

## What it does

- **Search-first.** The search box is focused on open — type a task (`project planning`, `confluence`, `debug`, `research`) and rows filter live.
- **Two views.** *Cards* for scanning by category, *Table* for sorting by model, effort, thinking, or cost.
- **Cost meter.** A 1–5 bar gauge on every row showing roughly how fast that model + effort combo eats your usage limits.
- **Hover tooltips.** Hover any tag to see what it means — effort levels show the full ladder, models show the relevant principle.
- **Freshness built in.** An age-tinted date badge (green → orange → red) and a monthly check-up panel nudge you to refresh before the data goes stale.
- **Refresh guide.** A one-click sub-page with the exact prompt to paste back to Claude to regenerate an updated version.

## Use it

Either open the live link above, or run it locally:

1. Download `index.html` from this repo.
2. Open it in your browser.
3. Pin the tab, or create a desktop/taskbar shortcut to the file.

## Host your own copy (GitHub Pages)

This repo is already set up for it. To enable the live site:

1. Go to **Settings → Pages**.
2. Under **Build and deployment → Source**, choose **Deploy from a branch**.
3. Pick your default branch and the **`/ (root)`** folder, then **Save**.
4. After a minute, your map is live at `https://<your-username>.github.io/claude-usecase-map/`.

## Keep it current

Claude's model lineup and effort defaults change over time, and the suggested settings here are **practical heuristics, not official Anthropic figures**. Once a month (the date badge turns orange to remind you), open the in-app **Refresh guide**, copy the prompt, paste it to Claude, and replace `index.html` with the updated version.

## Customise

All the rows live in a single `DATA` array near the bottom of `index.html`. Each entry is:

```js
{ cat, task, model, effort, think, why, tags }
```

Edit, add, or remove rows there — the cost meter and tooltips update automatically. The `tags` field is invisible search fuel (synonyms/keywords). See [CONTRIBUTING.md](CONTRIBUTING.md) if you'd like to suggest changes.

## Disclaimer

Not affiliated with or endorsed by Anthropic. "Claude" is a product of Anthropic. The model/effort recommendations reflect general guidance and personal judgement; verify against the official docs for anything critical.

## License

MIT — see [LICENSE](LICENSE). Use it, fork it, remix it.
