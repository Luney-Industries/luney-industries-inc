# AGENTS.md — Luney Industries Website

## What this repo is

Static website for [luneyindustries.com](https://luneyindustries.com), hosted on GitHub Pages.
Single `index.html` with embedded CSS and JS. No build step. No framework. No npm. Just vibes and HTML.

## Structure

```
index.html              — the entire website (HTML + CSS + JS, self-contained)
luney_industries.svg    — logo (light background variant)
luney_industries.png    — logo (light background variant, raster)
luney_industries_dark.svg  — logo (dark background variant)
luney_industries_dark.png  — logo (dark background variant, raster)
AGENTS.md               — this file
CLAUDE.md               — symlink to AGENTS.md
```

## Deployment

GitHub Pages serves directly from the `main` branch root. Push to `main` = live.

**Before merging to main:** run `/critique` to get code review sign-off.

## Development

No build step. Open `index.html` in a browser. That's it.

To preview locally with a real server (avoids CORS quirks):
```bash
python3 -m http.server 8080
# then open http://localhost:8080
```

## Conventions

- All styling lives in the `<style>` block inside `index.html`
- All scripts live in the `<script>` block at the bottom of `index.html`
- CSS custom properties (variables) are defined in `:root` — use them, don't hardcode colors
- No external dependencies or CDN links — keep it self-contained
- Logos: use `luney_industries_dark.svg` on dark backgrounds (the default), `luney_industries.svg` on light
- Favicon is defined inline as a data URI — update the `<link rel="icon">` tag if needed

## Products Luney Industries links to

- **FartyBobo.com** — the AI assistant, Luney Industries' sole product
- **theSilentCamera.com** — second Luney Industries product

Both should be linked prominently and open in a new tab with `rel="noopener"`.

## Easter eggs

- Konami code (↑↑↓↓←→←→BA) triggers a secret overlay — don't break this
- Stock ticker in nav randomizes every 3 seconds — leave it alone, it's funny

## Style guide

- Tone: corporate parody. Fake corporate speak wrapped around genuine humor.
- The company is a joke. FartyBobo.com and theSilentCamera.com are real links.
- All legal disclaimers reference "Todd (Legal)". Keep Todd.
- Never add real legal language — this is satire.

## Branch policy

- Never commit directly to `main`
- Branch from `main`, PR back to `main`
- Run `/critique` before opening any PR
