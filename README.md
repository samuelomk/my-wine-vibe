# My Wine Vibe

Interactive one-page wine preference experience designed for embedding into an app or website.

## What it does

- Guides users through a 5-question mood/sensory flow in ~60-90 seconds.
- Recommends a primary wine archetype plus alternates.
- Shows a swipeable product rail (5 items) with direct product links.
- Supports embed integration using `postMessage` events.

## Demo locally

Open `index.html` directly in a browser, or run a local static server:

```bash
python3 -m http.server 8000
```

Then visit [http://localhost:8000](http://localhost:8000).

## Project structure

- `index.html` - full UI, quiz logic, archetype mapping, product rail, and embed events.
- `wine-archetype/` - archetype visual assets used in result hero.
- `assets/default-wine-bottle.svg` - default bottle image for product cards.

## Embed contract

The page emits the following events to parent windows:

- `wine-vibe:resize` - sends `{ contentHeight, version }`
- `wine-vibe:complete` - sends quiz answers and selected archetypes
- `wine-vibe:cta` - sends CTA click metadata

## Notes

- Built as a static artifact for quick sharing/deployment.
- Styling uses Tailwind CDN + shadcn-inspired token variables.

## Suggested topics

`wine`, `recommendation`, `interactive`, `html`, `ux`, `onepager`
