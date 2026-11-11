# AIPG Grid Explorer

A small static web page that gives a live view of the
[AI Power Grid](https://aipowergrid.io), read in your browser from the public API.
It looks and reads like [AIPG Desktop](https://github.com/speteai/aipg-desktop), the
desktop app by the same author.

- **Overview** — network status, workers and models online, jobs today, validators, and
  the work done on the grid by type.
- **Models** — text and vision models with the number of workers serving each one, the
  measured speed and the list price; image, video and audio models with their prices.
- **Network** — which worker serves which model, with recent activity, and the latest
  jobs on the grid. Refreshes every 15 seconds.
- **Account** (needs an API key) — your credit and free allowance, your workers and
  their recent jobs.
- **Developers** — the non-obvious things that cost integration time, copy-paste
  quickstarts and the image API parameters.

> **Unofficial & community-built.** Not affiliated with AI Power Grid.
> Data is fetched live in your browser from `api.aipowergrid.io`.

## Use it

Visit the GitHub Pages deployment, or open `index.html` in any browser (keep
`aipg-logo.png` next to it). No build step, no dependencies, no server.

### API key

Everything except *Account* works without a key. If you save a `grid_…` key under
*Account*, it is used only to read your credit, your workers and their jobs. **The key
stays in your browser's `localStorage`** and is sent only to `api.aipowergrid.io` — it is
never uploaded or committed anywhere. The page cannot run a worker, chat or generate
images; AIPG Desktop does that.

## Why

Built while testing the grid as an external developer. The findings behind the
"gotchas" section are filed as issues on the AI Power Grid repos
(grid-skill #22, grid-text-worker #46/#47, aipg-documentation #44/#45/#46).

## License

MIT — see [LICENSE](LICENSE).
