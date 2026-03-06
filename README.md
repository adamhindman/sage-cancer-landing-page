# Cancer Landing Page

A responsive landing page project focused on providing information and resources related to cancer. This project is built using modern web development practices, including a build system and Hot Module Replacement (HMR).

## Features

- **Responsive Design**: Includes pre-configured breakpoints for mobile, tablet, and desktop views.
- **Build System**: Powered by [Parcel](https://parceljs.org/) for fast builds and a seamless development experience.
- **Hot Module Replacement (HMR)**: Instant updates in the browser during development.
- **Material UI Icons**: Integrated via CDN for easy access to a vast library of icons.

## Getting Started

### Prerequisites

Ensure you have [Node.js](https://nodejs.org/) installed on your machine.

### Installation

1. Clone the repository (or navigate to the project folder).
2. Install the dependencies:
   ```bash
   npm install
   ```

### Development

To start the development server with HMR:
```bash
npm start
```
By default, the application will be available at `http://localhost:1234`.

### Production Build

To create a production-ready build in the `dist` folder:
```bash
npm run build
```

## Project Structure

- `src/index.html`: The main HTML entry point.
- `src/index.js`: The JavaScript entry point, importing styles and logic.
- `src/style.css`: The main stylesheet containing base styles and responsive media queries.
- `package.json`: Project configuration and scripts.

## Breakpoints

The design follows a mobile-first approach with the following breakpoints:
- **Mobile**: Default styles
- **Tablet**: `min-width: 768px`
- **Desktop**: `min-width: 1024px`

## Spacing System

This project uses a **4px base spacing unit**. You can apply spacing in two ways:

### 1. Utility Classes (Recommended for HTML)
Apply margins and padding using classes in the format `{property}{side}-{multiplier}` where the multiplier is a unit of 4px (0-20).

- **Properties**: `m` (margin), `p` (padding)
- **Sides**: `t` (top), `b` (bottom), `l` (left), `r` (right), `x` (horizontal), `y` (vertical)
- **Examples**: 
  - `.mt-4` = `margin-top: 16px`
  - `.px-2` = `padding-left: 8px; padding-right: 8px;` (Horizontal padding)
  - `.py-6` = `padding-top: 24px; padding-bottom: 24px;` (Vertical padding)
  - `.pb-10` = `padding-bottom: 40px`
  - `.pt-2 .pr-4` = Use multiple classes for specific sides (8px top, 16px right)

### 2. SCSS Function (For Stylesheets)
Use the `space($multiplier)` function in your SCSS files.
```scss
.custom-element {
    padding: space(3); // 12px on all sides
    margin-bottom: space(6); // 24px bottom margin
    
    // Using for multiple sides (standard CSS shorthand)
    padding: space(2) space(4); // 8px vertical, 16px horizontal
    margin: space(1) space(2) space(3) space(4); // Top: 4px, Right: 8px, Bottom: 12px, Left: 16px
}
```

## Visibility Utilities

You can show or hide elements at specific breakpoints using these classes:

| Class | Description |
|-------|-------------|
| `.hide-mobile` | Hidden on mobile (shown when $\ge$ 768px) |
| `.show-mobile` | Only visible on mobile (hidden when $\ge$ 768px) |
| `.hide-tablet` | Hidden when screen width is $\ge$ 768px |
| `.show-tablet` | Only visible when screen width is $\ge$ 768px |
| `.hide-desktop` | Hidden when screen width is $\ge$ 1024px |
| `.show-desktop` | Only visible when screen width is $\ge$ 1024px |
| `.visually-hidden` | Hidden visually but remains accessible to screen readers |

**Note**: For `.show-tablet` and `.show-desktop`, the default display is `block`. You can combine them with `.flex` or `.grid` if you need a specific display type (e.g., `<div class="show-desktop flex">`).

## UI Components

This project uses [Material Icons](https://fonts.google.com/icons) for iconography. You can use them by adding a span with the `material-icons` class:
```html
<span class="material-icons">favorite</span>
```
