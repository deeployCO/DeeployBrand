# Deeploy Brand System

Design system and brand reference for [Deeploy](https://deeploy.ca) — digital marketing agency.

## Usage

### For developers

**Tokens only** — raw CSS custom properties:

```css
@import url('./tokens/tokens.css');
```

**Full component library** — tokens + `.db` namespace components (buttons, forms, stats, etc.):

```css
@import url('./tokens/foundations.css');
```

Wrap any section in `.db` to activate the baseline:

```html
<div class="db">
  <h2 class="section-title">...</h2>
  <button class="btn btn--primary btn--lg">Book a strategy call</button>
</div>
```

Use CSS custom properties directly:

```css
.button {
  background: var(--db-red);
  color: var(--db-red-fg);
  font-family: var(--db-ff);
  font-weight: 700;
}
```

### For Claude Code / AI tools

`CLAUDE.md` in this repo root is the primary machine-readable brand brief. Reference it when building Deeploy UI or generating marketing assets.

### For designers

Open `brand/index.html` in a browser for the full visual brand book. Hosted on GitHub Pages at `[org].github.io/DeeployBrand`.

## File Structure

```
DeeployBrand/
├── CLAUDE.md                    ← AI brand reference (start here)
├── .impeccable.md               ← Design context for Claude Code /impeccable
├── assets/
│   └── logos/
│       ├── logo-primary.svg     ← Default: red mark + navy wordmark
│       ├── logo-white.svg       ← Reversed: all white
│       ├── logo-black.svg       ← Mono: Blue King only
│       ├── mark.svg             ← Compact: squares + D, two-color
│       └── mark-white.svg       ← Compact: squares + D, white
├── tokens/
│   ├── colors.json              ← Color palette with hex/RGB/CMYK
│   ├── typography.json          ← Font family, scale, rules
│   ├── spacing.json             ← 4pt spacing scale and grid
│   ├── tokens.css               ← CSS custom properties (import this)
│   └── foundations.css          ← Component primitives (.db namespace)
├── brand/
│   └── index.html               ← Visual brand book
└── templates/
    ├── social/specs.json        ← Social media dimensions + composition rules
    └── marketing/specs.json     ← Landing page, print, email specs
```

## Brand Colors

| Name | Hex | Use |
|------|-----|-----|
| Deploy Red | `#d81d4d` | Accent, mark, CTAs (10% max) |
| Blue King | `#0e2d3f` | Text, dark sections (30%) |
| Baby Blue | `#8BC9DB` | Secondary accent |
| Off-white | `#fafaf8` | Page background (60%) |

## Typography

**Font:** Avenir (full family — load via Adobe Fonts for web)
**Weights:** Light 300 · Book 400 · Medium 500 · Heavy 700 · Black 900
**Web fallback:** Nunito (Google Fonts)

## Logo Rules

- All logos are SVG with transparent backgrounds
- Primary: light surfaces | White: dark surfaces | Mono: print only
- Wordmark viewBox: `800 × 300` | Mark viewBox: `600 × 600`
- Minimum digital: 120px wide (wordmark), 40px (mark)
- Never distort, recolor, rotate, or add effects

## GitHub Pages

Enable GitHub Pages from the `brand/` directory to host the brand book at:
`https://[your-org].github.io/DeeployBrand`
