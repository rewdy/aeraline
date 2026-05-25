# 🌬️ Aeraline

A lightweight, golden ratio-based CSS typography and layout library built with Sass.

> ⚠️ **Work in Progress** – API may change.

## Features

- **Golden Ratio Typography** – Font sizes, spacing, and line heights based on φ (1.618)
- **CSS Custom Properties** – Easily customizable via CSS variables
- **Dark Mode** – Automatic `prefers-color-scheme` support
- **Flexbox Grid** – 12-column responsive grid system
- **Utility Classes** – Flexbox, spacing, and typography helpers
- **Minimal Reset** – Sensible defaults without bloat

## Installation

```bash
npm install @rewdy/aeraline
# or
bun add @rewdy/aeraline
```

## Usage

### Import Compiled CSS

```html
<link rel="stylesheet" href="node_modules/@rewdy/aeraline/dist/style.css">
```

### Import as Sass Module

```scss
@use "@rewdy/aeraline" as lib;

// Apply all styles
@include lib.ratio-typography;
@include lib.extra-flexbox;
```

### Selective Imports

```scss
@use "@rewdy/aeraline" as lib;

// Pick what you need
@include lib.ratio-base;      // Reset + CSS variables
@include lib.ratio-headings;  // h1-h6 styles
@include lib.ratio-semantic;  // Paragraphs, lists, tables, etc.
@include lib.ratio-utilities; // Utility classes
@include lib.flexbox-grid;    // 12-column grid
```

## Customization

Override Sass variables before importing:

```scss
@use "@rewdy/aeraline" as lib with (
  $base-ratio: 1.5,
  $base-font-size: 16px,
  $accent-base: #0066cc,
  $font-family-base: "Helvetica Neue", sans-serif
);
```

Or override CSS custom properties:

```css
:root {
  --base-ratio: 1.5;
  --font-base-size: 16px;
  --accent-color: #0066cc;
}
```

## CSS Variables

| Variable | Description |
|----------|-------------|
| `--font-size-{xs,sm,base,md,lg,xl,xxl}` | Typography scale |
| `--spacing-{xs,sm,base,md,lg,xl,xxl}` | Spacing scale |
| `--line-height-{tight,base,loose}` | Line heights |
| `--text-color`, `--background-color` | Theme colors |
| `--accent-color` | Primary accent |

## Grid

```html
<div class="container-fluid">
  <div class="row">
    <div class="col-xs-12 col-md-6">Half width on medium+</div>
    <div class="col-xs-12 col-md-6">Half width on medium+</div>
  </div>
</div>
```

Breakpoints: `xs` (default), `sm` (48em), `md` (62em), `lg` (75em)

## Development

```bash
bun install
bun run dev     # Start demo site
bun run build   # Build library
```

## License

MIT

---

Made with 😂 by [Rewdy](http://rewdy.lol)
