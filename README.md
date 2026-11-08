# AIPG Grid Explorer

A tiny, single-file web page that gives developers a live view of the
[AI Power Grid](https://api.aipowergrid.io/v1) OpenAI-compatible API:

- **Text & vision models** — pulled live from the public `GET /v1/models`
  endpoint, with input modalities and USD prices per million tokens.
- **Image generation** — the `/v1/images/generations` surface and its models,
  which are *not* listed by `/v1/models` (optionally refreshed live with a key).
- **Developer gotchas** — the non-obvious things that cost integration time
  (the `Python-urllib` 403, reasoning `content: null`, no balance endpoint,
  the retired `/api/v2`, missing endpoints).
- **Copy-paste quickstarts** — curl, Python, JS and image examples.

> **Unofficial & community-built.** Not affiliated with AI Power Grid.
> Data is fetched live in your browser from `api.aipowergrid.io`.

## Use it

Open `index.html` in any browser, or visit the GitHub Pages deployment.
No build step, no dependencies, no server — one static HTML file.

### Optional key probe

Browsing needs **no API key** (`/v1/models` is public and CORS-enabled).
If you paste a `grid_…` key into the *Live key probe* box, it is used only to
refresh the image-model list and show your linked account. **The key stays in
your browser's `localStorage`** and is sent only to `api.aipowergrid.io` — it is
never uploaded or committed anywhere.

## Why

Built while testing the grid as an external developer. The findings behind the
"gotchas" section are filed as issues on the AI Power Grid repos
(grid-skill #22, grid-text-worker #46/#47, aipg-documentation #44/#45/#46).

## License

MIT — see [LICENSE](LICENSE).
