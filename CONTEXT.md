# Project Context: Cancer Landing Page

## Overview
This project is a modern, responsive landing page focused on cancer-related information and resources. It is designed to be highly performant, accessible, and maintainable using a minimal but effective toolchain.

## Tech Stack
- **Bundler:** Parcel (configured for HMR and production builds).
- **Styling:** SCSS (Sass preprocessor) with a mobile-first responsive strategy and smooth scrolling.
- **Icons:** Material Icons (Google Fonts) loaded via CDN.
- **Typography:** DM Sans (loaded via Google Fonts).
- **Entry Points:** 
    - HTML: `src/index.html`
    - JS: `src/index.js` (using ES Modules)
    - SCSS: `src/style.scss` (referenced in HTML)

## Design Tokens
- **Colors:**
    - `black`: `#0E101A`
    - `brand-gray-dark`: `#1F3042`

- **Layout:**
    - `spacing-unit`: `4px`
    - `slat-horizontal-margin`: `16px` (mobile), `40px` (desktop)
    - `slat-vertical-margin`: `48px` (mobile), `128px` (desktop)
    - `partnerships-content-wrapper`: `668px` max-width, centered horizontally, and text-aligned center.

## Project Structure
```
cancer landing page/
├── src/
│   ├── assets/
│   │   └── images/    # Project images and graphics
│   ├── index.html     # Main entry point & HTML structure
│   ├── index.js       # JS entry point & CSS imports
│   └── style.scss      # Responsive styles & breakpoints
├── package.json       # Project scripts and dependencies
└── README.md          # Human-readable documentation
```

## CSS Architecture
The project uses a mobile-first approach. Styles are structured as follows:
1.  **Base/Reset Styles:** General normalization.
2.  **Mobile Styles:** Default styles (applied to all screens).
3.  **Tablet Breakpoint:** `@media (min-width: 768px)`
4.  **Desktop Breakpoint:** `@media (min-width: 1024px)`

## Development Workflow
- **Start Dev Server:** `npm start` (Runs Parcel with HMR on `localhost:1234`).
- **Build for Production:** `npm run build` (Outputs optimized files to `dist/`).
- **Adding Assets:** Place assets in `src/` and import them directly into JS or reference them in HTML.
- **Navigation:** Supports anchor linking (e.g., `#overview`) with smooth scroll behavior.

## AI Instructions
- Use the `.slat` class for section containers (e.g., `<section id="overview" class="slat">`) to ensure consistent horizontal and vertical padding.
- The Overview section (`#overview`) is configured as a hero slat with a background image (`src/assets/images/overview-bg.png`) aligned to the bottom right.
- Use the 4px spacing system via the `space()` function in SCSS or utility classes in HTML.
- **Responsive Spacing Utilities**: Use the format `{property}{side}[-{breakpoint}]-{multiplier}`.
    - Breakpoints: `tablet` (768px+), `desktop` (1024px+).
    - Example: `.mb-4 .mb-tablet-8 .mb-desktop-12`.
- When adding new components, ensure they follow the established media query pattern in `style.scss` or the breakpoint-specific files in `src/styles/`.
- Use Material Icon class names (e.g., `<span class="material-icons">icon_name</span>`) for iconography.
- Maintain the clean separation of concerns: logic in `.js`, structure in `.html`, and presentation in `.scss`.

## Accessibility
- The page will be accessible by default: semantic HTML, proper heading structure, alt text on images, color contrast checks, and landmarks; ensure skip links and WCAG-aware semantics where appropriate.
- All interactive elements are keyboard accessible with visible focus states and ARIA-labels/roles where appropriate.
- Consider implementing skip links, ARIA-labels, and descriptive titles for links and controls where appropriate.

## Testing / CI
- There is no testing or CI in this HTML project, YOLO.

## Deployment
- The project builds to `dist/` and is deployed to a static hosting provider; preview deployments are created for PRs and production deployment occurs via merging to main.
- Preview deployments on PRs; production deployment via a simple push to main/main-branch workflow; rollback plan in case of failed deployments.

## Project Status
- Status: Active development; MVP scaffold released; current focus on accessibility, performance optimization, CI/CD groundwork, and growing test coverage.

## Conventions
- File paths and conventions:
  - Root: `cancer landing page/`
  - Assets: `src/assets/`
  - HTML entry: `src/index.html`
  - JS entry: `src/index.js`
  - Styles: `src/style.scss`
  - Tests: `tests/` (if added)
- Use the `.slat` class for sections as described; all components follow the responsive pattern defined in `style.scss`; ensure tokens and color decisions remain centralized.
