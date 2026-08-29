# Theme Accessibility & Performance Work Log

## Accessibility Fixes (Agentic Browsing)
- **Discernible Text on Slider Links**: Added `aria-label` to `.hero__slide-link` in `sections/slideshow.liquid` and `snippets/page-block-image-hero.liquid` to ensure screen readers can read where the slide links to.
- **Slick Slider ARIA Fixes**: Disabled slick slider's automatic accessibility attributes globally by setting `accessibility: false` in `assets/theme.js.liquid`. This prevents slick from injecting invalid ARIA states (`role="presentation"` with `aria-selected`, missing accessible names on `listbox`).
- **Discernible Text on Promo Grid Links**: Added `aria-label` to anchor tags wrapping promotional images in `snippets/promo-grid.liquid` (covering `sale_collection`, `image`, and `banner` blocks).
- **Cleanup**: Removed the previously added `slick-accessibility-fix.liquid` hack as disabling the native slick accessibility option natively resolves the issue more cleanly. (Pending removal)
