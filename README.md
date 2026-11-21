# nervousai

Static site for [nervous.ai](https://nervous.ai), replacing the Super.so site published from Notion.
Plain HTML and CSS, no build step. Hosted on GitHub Pages from `main`.

## Layout

- `movement/index.html` — The Movement landing page (`/movement`), ported 21 Nov 2026.
- `assets/css/site.css` — shared styles (cream page, Inter headings, Space Mono body).
- `assets/fonts/` — Inter and Space Mono, self-hosted (both SIL Open Font Licence).
- `assets/img/logo.png` — site logo, also used as the favicon.

Pages link to assets with relative paths, so the site works both at
`zerozero.github.io/nervousai/` and at the root of `nervous.ai`.

## Preview locally

    python3 -m http.server 8000
    # then open http://localhost:8000/movement/

## Signup form

`/movement` embeds the Tally form `aO2dPX` ("Join the alpha"). Tally's embed script
sizes the iframe to the form, so no fixed height is needed.

## Still to port

- Home, About (30 years, not 20; drop the hidden summariser text), Works, blog posts.
- Header links currently point at `https://nervous.ai/…` (the Super site). Switch them
  to relative links as each page is ported.

## Cutover

1. Port the remaining pages.
2. Add a `CNAME` file containing `nervous.ai` and set the custom domain in the repo's Pages settings.
3. Repoint the nervous.ai DNS to GitHub Pages, check HTTPS, then cancel Super.
