# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Development

This is a static HTML website with no build process. To preview locally:

```bash
# Using Python
python3 -m http.server 8000

# Using Node.js
npx http-server
```

Then visit `http://localhost:8000` (or port shown).

## Architecture

Single-page responsive website (`index.html`) for Flora's Cakes bakery business.

**Tech Stack:**
- Bootstrap 3 (responsive grid)
- jQuery (DOM manipulation)
- Owl Carousel (reviews slider, service carousel)
- Isotope (gallery filtering)
- Magnific Popup (lightbox)

**Sections:**
- Hero with sidebar navigation and 6 service cards
- Gallery with category filtering (special, birthday, cupcakes, jaincakes)
- Reviews carousel (auto-rotating testimonials)
- Footer with contact info

## CSS Organization

Custom styles are split into focused files:

| File | Purpose |
|------|---------|
| `css/style.css` | Base template styles (do not modify) |
| `css/custom-fonts.css` | Typography (Alkatra for headings, Lato for body) |
| `css/hero-cards.css` | Service cards with zoom hover effects |
| `css/reviews-slider.css` | Review carousel styling and star animations |
| `css/smooth-scroll.css` | Smooth scrolling behavior |
| `styles/maincolors.css` | Brand color definitions |

**Brand Colors:**
- Primary Pink: `#d4145a`
- Text: `#2d2d2d`
- Gold (stars): `#f39c12`

## JavaScript

- `js/custom.js` - Main functionality: smooth scroll, carousel init, gallery filtering, lightbox
- `js/plugins.js` - Bundled jQuery plugins (Owl Carousel, Isotope, Magnific Popup)

Gallery categories are defined via CSS classes on gallery items: `.special`, `.birthday`, `.cupcakes`, `.jaincakes`

## Adding Content

**Gallery images:** Add to `img/gallery/`, reference in index.html with appropriate category class

**Reviews:** Add new `.review-item` elements within the Owl Carousel container in index.html

**Navigation:** Anchor links use smooth scroll (e.g., `#gallery`, `#reviews`)
