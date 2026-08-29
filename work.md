# Theme Accessibility & Performance Work Log

## Accessibility Fixes (Agentic Browsing)
- **Discernible Text on Slider Links**: Added `aria-label` to `.hero__slide-link` in `sections/slideshow.liquid` and `snippets/page-block-image-hero.liquid` to ensure screen readers can read where the slide links to.
- **Slick Slider ARIA Fixes**: Disabled slick slider's automatic accessibility attributes globally by setting `accessibility: false` in `assets/theme.js.liquid`. This prevents slick from injecting invalid ARIA states (`role="presentation"` with `aria-selected`, missing accessible names on `listbox`).
- **Discernible Text on Promo Grid Links**: Added `aria-label` to anchor tags wrapping promotional images in `snippets/promo-grid.liquid` (covering `sale_collection`, `image`, and `banner` blocks).
- **Cleanup**: Removed the previously added `slick-accessibility-fix.liquid` hack as disabling the native slick accessibility option natively resolves the issue more cleanly.
- **Appropriate ARIA Roles for Navigation**: Removed invalid `role="navigation"` from the `ul` element in `snippets/header-desktop-nav.liquid` to conform to ARIA standards for `ul` tags.
- **Discernible Text on Newsletter Button**: Added `aria-label` to the submit button (`.footer__newsletter-btn`) in `snippets/footer-newsletter.liquid`.
- **Third-Party App (Loox) Accessibility**: Added a `MutationObserver` script to `layout/theme.liquid` (just before `</body>`) to dynamically inject `aria-label="Close dialog"` on `.loox-pn-close` links, ensuring screen readers can announce the popup close button.
