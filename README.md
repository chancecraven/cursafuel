# Cursa Fuel Co. — Authority Website
## CursaFuel.com | Cloudflare Pages

---

## File Structure

```
cursafuel/
├── index.html          # Homepage
├── services.html       # All services — full list with anchor links
├── industries.html     # Industries served
├── service-area.html   # Service area — primary states + national emergency
├── about.html          # Brand story, mission, operating principles
├── contact.html        # Request form + 24/7 emergency line
├── styles.css          # Single stylesheet — all pages
├── sitemap.xml         # XML sitemap
├── robots.txt          # Search crawler rules
├── images/
│   ├── cursa-logo-dark.png     # Light background use (nav)
│   ├── cursa-logo-light.png    # Dark background use (hero, footer)
│   ├── favicon-dark.png        # Dark mark
│   └── favicon.png             # Browser favicon
└── README.md
```

---

## Deploying to Cloudflare Pages

1. Push this folder to a GitHub or GitLab repository.
2. Log in to the [Cloudflare Dashboard](https://dash.cloudflare.com).
3. Navigate to **Pages** → **Create a project** → **Connect to Git**.
4. Select your repository.
5. Set **Build command** to _(leave blank — static site, no build step)_.
6. Set **Build output directory** to `/` or leave as default root.
7. Click **Save and Deploy**.
8. Connect your custom domain `cursafuel.com` under **Custom Domains**.

No build tools required. This is a pure HTML/CSS static site — Cloudflare serves it directly from edge.

---

## Contact Form

The contact form on `contact.html` uses a `formspree.io` action as a placeholder:
```
action="https://formspree.io/f/contact"
```

Replace `contact` with your actual Formspree form ID after creating a free account at [formspree.io](https://formspree.io), or swap for any other form endpoint (Netlify Forms, EmailJS, custom endpoint).

---

## Brand Tokens

| Name      | Hex       | Use                        |
|-----------|-----------|----------------------------|
| Crude     | #111111   | Primary dark — nav, hero, footer |
| Blaze     | #E8571A   | Accent — buttons, dividers, CTAs (use sparingly) |
| Dustroad  | #F0EAE0   | Warm off-white — alternating sections |
| Gravel    | #888884   | Body copy, secondary text  |
| White     | #FFFFFF   | Clean field                |

**Typography**
- Display: Futura Bold (all caps, wide letter-spacing)
- Body: Helvetica Neue / system sans

---

## SEO Notes

- Each page has a unique `<title>` and `<meta name="description">`.
- Canonical URLs point to `https://cursafuel.com/`.
- `index.html` includes JSON-LD structured data (LocalBusiness schema).
- `services.html` includes JSON-LD for Service schema.
- `service-area.html` includes JSON-LD for areaServed schema.
- `sitemap.xml` covers all six pages.
- `robots.txt` allows all crawlers and references sitemap.

---

## Accessibility

- Skip-to-content link on every page.
- All navigation has `aria-label`.
- Current page marked with `aria-current="page"`.
- Mobile menu toggle has `aria-expanded` state.
- Form fields have associated `<label>` elements.
- `prefers-reduced-motion` respected via CSS.
- Color contrast meets WCAG AA on all primary text.

---

## Performance

- Zero JavaScript frameworks.
- Single CSS file.
- No external fonts (system font stack for Helvetica Neue; Futura falls back to Century Gothic, then Trebuchet MS).
- Images served as PNG from `/images/`.
- No render-blocking resources.

---

*Cursa Fuel Co. — Always Running. Always There.*
