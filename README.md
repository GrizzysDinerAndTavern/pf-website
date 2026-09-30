# Priority Fitness Front-End Website

This package is a complete static front-end build for the Priority Fitness website brief. It is intentionally focused on design, UX, responsive behavior, real supplied assets, and front-end interactions. It does **not** implement CRM, GoHighLevel, analytics, tracking, schema, ad pixels, backend APIs, or live form submission.

## Run locally

Double-click `index.html` to open it straight from disk. All links and assets use relative paths (see `make_portable.py`), so no server is needed.

Or serve it:

```bash
cd priority-fitness-site
python -m http.server 8080
```

Then open `http://localhost:8080/`.

## Public pages included

- `/`
- `/services/`
- `/services/equipment-sourcing/`
- `/services/equipment-installation/`
- `/services/equipment-service-repair/`
- `/services/preventative-maintenance/`
- `/services/equipment-relocation/`
- `/services/equipment-extraction/`
- `/residential-repair/`
- `/equipment-health-check/`
- `/used-equipment/`
- `/industries/`
- `/sell-equipment/`
- `/projects/`
- `/about/`
- `/contact/`
- `/request-quote/`

## Key interactions implemented

- Sticky transparent-to-solid header
- Desktop services mega-menu
- Mobile navigation
- Interactive homepage lifecycle selector
- Dynamic lifecycle photography / copy / CTA routing
- One-machine ↔ full-facility visual toggle
- Question-based service router
- Responsive project gallery
- Project category filters
- Guided multi-step quote UI
- Mobile sticky action bar on high-intent service pages
- Front-end form validation shell / integration hooks
- Reduced-motion support
- Responsive image `srcset` generation

## Brand system

The primary red is sampled from the supplied Priority Fitness mark: `#CE202D`.

Typography:
- Barlow Condensed 600 / 700 / 800 for display
- Inter 400 / 500 / 600 / 700 / 800 for body and UI

Core tokens live at the top of `assets/css/styles.css`.

## Form integration handoff

Forms are intentionally front-end only. Search for:

- `data-front-end-only`
- `#quoteWizard`
- `.integration-hook`

`assets/js/app.js` currently intercepts submission so an unconnected build cannot send data nowhere. Jasper can replace those handlers with the production GoHighLevel submission logic.

## Important content states

- **Used Equipment:** no real inventory was supplied, so the page renders a polished empty state. Do not fabricate listings.
- **Equipment Health Check:** pricing is structured around the confirmed `$49` Health Check and `$99` Deluxe Tune-Up, but the final inclusions still need approved copy before publication.
- **Testimonials:** no approved testimonial text was supplied. The homepage uses the confirmed 4.6 Google rating and real-work proof rather than fabricated quotes.
- **Address:** the build uses only `433 S Industrial Park Rd`. City / state / ZIP were not added.
- **Hours:** only `8:00 AM–5:00 PM` is shown. No operating days were invented.

## Asset handling

All supplied Priority Fitness photography is included in `assets/images/` and used throughout the site. WebP images also have 720px and 1080px derivatives for responsive loading. Supplied logos are used directly rather than recreated.

## Rebuilding

`build.py` generates the public HTML pages from shared functions and service data. It uses Pillow + BeautifulSoup only to enrich generated image tags with dimensions and responsive `srcset` metadata.

```bash
python build.py
```

The site itself has no runtime framework dependency.

## Development templates

`templates/equipment-card.html` and `templates/equipment-detail.html` provide non-public inventory templates. They intentionally use placeholders and should only be rendered after real inventory data exists.
