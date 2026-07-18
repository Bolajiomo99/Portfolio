# Portfolio

Personal developer portfolio — a single-page site with dark/light themes,
English/Arabic (RTL) switching, and scroll-triggered animations.

## Stack

- Static HTML, CSS and vanilla JavaScript — no build step
- [anime.js](https://animejs.com/) for animation
- Font Awesome + Google Fonts (Tajawal, Fira Code) via CDN
- Tailwind CDN is loaded but the layout is driven by `css/style.css`

## Layout

```
index.html          markup for all six sections
css/style.css       theming (CSS custom properties), layout, RTL rules
js/main.js          app state, theme + language toggles, scroll spy
js/animations.js    loader, scroll-triggered reveals, parallax
```

## Running locally

No build or dependencies — serve the directory over HTTP:

```bash
python3 -m http.server 5500
```

Then open <http://127.0.0.1:5500>.

Opening `index.html` straight from the filesystem mostly works, but serving it
over HTTP avoids `file://` restrictions in some browsers.

## Theming

Colours live as custom properties on `:root` in `css/style.css`, with a
`[data-theme="light"]` block overriding them. To retheme the site, change the
variables rather than individual rules.

Language switching is driven by `data-text-en` / `data-text-ar` attributes on
each translatable element, with `data-placeholder-en` / `data-placeholder-ar`
for form fields. Preferences persist to `localStorage`.

## Status

Content is still the starter template — copy, work history and contact details
are placeholders pending real details.
