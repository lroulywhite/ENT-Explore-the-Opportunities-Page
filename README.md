# MAX | Explore the Opportunity Page [Interaction]

An open-exploration product interaction for **MomentusMAX**. Learners click through 12 tabs of the Opportunity page at their own pace, with a bottom bar tracking progress ("0 of 12 viewed").

Built by the Momentus Digital Customer Success (DCS) team for the Learning Center.

## What's in this repo

| File | Purpose |
|---|---|
| `index.html` | The complete interaction. Self-contained: CSS, JS, Inter font, and product images are all embedded. No build step, no dependencies, no network requests. |
| `.github/workflows/pages.yml` | Optional: deploys `index.html` to GitHub Pages on push to `main`. |
| `.nojekyll` | Tells GitHub Pages to serve the file as-is. |

## Run locally

Open `index.html` in any modern browser. No server required.

## Host on GitHub Pages

1. Push to GitHub.
2. **Settings → Pages → Build and deployment → Source: GitHub Actions**.
3. Push to `main` (or run the workflow manually). The site publishes at `https://<org>.github.io/<repo>/`.

> If the repo is private, GitHub Pages requires a plan that supports private Pages. Pages sites can be publicly reachable even when the repo is private, so confirm that's acceptable for product UI before enabling.

## Embed (e.g., Genially, 360Learning, LMS)

Use an iframe pointing at the hosted URL:

```html
<iframe src="https://<org>.github.io/<repo>/" title="MAX | Explore the Opportunity Page [Interaction]"
        width="100%" style="aspect-ratio:1920/1176;border:0" allowfullscreen></iframe>
```

The stage is authored at 1920×1176 and scales to fit its container.

## Notes for editors

- `index.html` is a single generated file (~1 MB) with the product screen embedded as an inner `srcdoc` iframe. Edit the source it was generated from where possible; hand-editing the base64 and escaped HTML is error-prone.
- Product UI inside the interaction comes from approved captures and should not be redesigned or approximated.
- Appending `#review` to the URL turns on review mode.
- The outer page and inner page talk via `postMessage` (`selectExample`, `stageScale`, `review`, `simSelector`, `barHighlight`).

## License

Proprietary. © Momentus Technologies. All rights reserved. Internal use only unless stated otherwise.
