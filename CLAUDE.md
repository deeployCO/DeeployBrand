# Deeploy Brand System — AI Reference

This file is the primary machine-readable brand brief for Claude Code, design automation, and marketing pipelines. Reference it when building UI, generating creative assets, or producing social/marketing content for Deeploy.

---

## Identity

**Brand:** Deeploy
**Category:** Digital marketing agency
**Tagline:** Digital marketing powered by Human + AI
**Website:** deeploy.ca
**Brand docs:** brand.deeploy.co
**Google Premier Partner:** Yes — top 3% globally
**Markets:** Canada (HQ), 35+ countries, 200+ clients

---

## Logo Files

All logos are SVG with transparent backgrounds. No white or colored backgrounds baked in.

| File | Usage | Background it works on |
|------|-------|------------------------|
| `assets/logos/logo-primary.svg` | Default — red mark + navy wordmark | White, light surfaces |
| `assets/logos/logo-white.svg` | Reversed | Dark navy, photography overlays, dark sections |
| `assets/logos/logo-black.svg` | Monochrome | Light surfaces when color printing unavailable |
| `assets/logos/mark.svg` | Compact — squares + D | White, light surfaces |
| `assets/logos/mark-white.svg` | Compact reversed | Dark surfaces |

**Logo viewBox:** Wordmark = 800×300. Mark = 600×600.

**Logo rules:**
- Minimum digital size: 120px wide for wordmark, 40px for mark
- Clear space: equal to the height of the descending-squares mark on all sides
- Never distort, rotate, recolor, or add effects
- Never place red logo on red backgrounds or white logo on white backgrounds
- Never use logo-black on pure black (#000) — it disappears

---

## Color Tokens

```css
--color-red:       #d81d4d;   /* Deploy Red — brand primary accent */
--color-navy:      #0e2d3f;   /* Blue King — primary text + dark bg */
--color-blue:      #8BC9DB;   /* Baby Blue — secondary accent */
--color-white:     #ffffff;
--color-bg:        #fafaf8;   /* page background */
--color-surface:   #ffffff;   /* elevated surfaces */
--color-separator: #dce6ea;   /* borders, dividers */
--color-text:      #0e2d3f;   /* primary text */
--color-text-2:    #4a6878;   /* secondary text */
--color-text-3:    #7a9aaa;   /* tertiary / placeholder */
--color-red-tint:  #fdf0f3;   /* hover / error surface */
--color-navy-tint: #eef2f5;   /* code blocks / inactive */
```

**Color usage ratios:**
- 60% — Off-white / White (surfaces, backgrounds)
- 30% — Blue King (text, structure, dark sections)
- 10% — Deploy Red (CTAs, accents, active states, mark)
- Baby Blue — supporting only, never dominant

**Never:**
- Gradient text using Deploy Red or Baby Blue
- Pure black (#000) or pure white (#fff) — always use brand values
- Baby Blue as text color on white (fails contrast)
- Red on red backgrounds

---

## Typography

**Font family:** Avenir (full family)
```css
font-family: 'Avenir Next', 'Avenir', 'Nunito', system-ui, sans-serif;
```

**Web delivery:** Load Avenir via Adobe Fonts / TypeKit (commercial license required). Nunito (Google Fonts) as open-source fallback.

**Weights:**
- 300 Light — decorative numerals, captions, large watermark text
- 400 Book — body copy
- 500 Medium — UI labels, emphasis
- 700 Heavy — subheadings, strong emphasis
- 900 Black — display headings, hero text, logo wordmark

**Type scale:**
```
--text-xs:   0.8125rem (13px)   labels, legal
--text-sm:   0.9375rem (15px)   captions
--text-base: 1rem      (16px)   body
--text-md:   1.125rem  (18px)   lead paragraph
--text-lg:   1.375rem  (22px)   H4
--text-xl:   1.75rem   (28px)   H3
--text-2xl:  2.25rem   (36px)   H2
--text-3xl:  3rem      (48px)   H1
--text-4xl:  4rem      (64px)   Display
--text-5xl:  5.5rem    (88px)   Hero
```

**Rules:**
- Max line length: 68ch for body text
- Uppercase + wide tracking for short labels only — never body copy
- Line-height: 1.1–1.25 for headings, 1.5–1.65 for body
- Large display headings (>48px): tracking -0.02em

---

## Spacing System

4pt base scale. Use `gap` not margins for sibling spacing.

```
--space-1:   4px      micro-nudges
--space-2:   8px      icon gaps
--space-3:   12px     input padding
--space-4:   16px     default component padding
--space-6:   24px     card padding
--space-8:   32px     between related blocks
--space-12:  48px     section internal margin
--space-16:  64px     major section gap (mobile)
--space-24:  96px     major section gap (desktop)
--space-32:  128px    hero padding
--space-40:  160px    cover breathing room
```

---

## UI Design Rules

### Always
- White or off-white (`#fafaf8`) as dominant background
- Blue King (`#0e2d3f`) as primary text color
- Avenir Heavy or Black for headings
- Generous negative space — breathing room communicates authority
- Use `gap` for component spacing, not margins
- Container max-width: 1200px content, 720px text columns
- Prefer grid layout with `repeat(auto-fit, minmax(280px, 1fr))` for card grids

### Never
- Gradient text (no `background-clip: text` with gradients)
- `border-left` or `border-right` wider than 1px as colored accent stripes on cards/alerts
- Glassmorphism (blur + transparency effects)
- Pure black (#000) backgrounds — use Navy (#0e2d3f)
- Purple, cyan, or neon colors — they are not part of the Deeploy palette
- Identical card grids with icon + heading + text repeated
- Centered body text layouts
- Generic rounded rectangles with drop shadows as the primary container style

---

## Brand Voice

**Personality (scored 1–10):**
- Formal ↔ Casual: 5 — Professional, not stiff
- Rational ↔ Emotional: 3 — Data and proof first
- Playful ↔ Serious: 3 — B2B credibility; no humor
- Bold ↔ Subtle: 7 — Strong headlines, direct claims
- Traditional ↔ Innovative: 8 — AI-first, future-forward
- Expert ↔ Accessible: 4 — Industry language OK

**Voice in one sentence:** Authoritative agency that leads with proof, speaks in results, and treats AI not as a trend but as infrastructure.

**Headline formula:** Lead with credential or result, not feature.
- ✓ "Top 3% Google Partner. Every dollar tracked."
- ✗ "We offer comprehensive digital marketing solutions."

**Copy rules:**
- Short sentences. Active voice.
- No superlatives without evidence.
- Numbers beat adjectives: "200+ clients" not "many clients."
- CTA: "Book a strategy call" not "Learn more."

---

## Photography Direction

**Style:** Professional, cinematic — dark overlays on urban/professional environments.
**Motion:** Speed and movement blur — conveys pace, forward momentum.
**Subjects:** Marketing professionals, analytics dashboards, diverse business teams, city environments.
**Forbidden:** Cheesy stock (handshakes, staged smiles), low-quality lifestyle imagery, consumer-grade visuals.
**Treatment:** Dark overlay at 40–60% opacity on photography when used as section backgrounds.

---

## Social Media Template Specs

See `templates/social/specs.json` for pixel dimensions and composition rules per platform.

Key formats:
- Instagram Feed: 1080×1080 (1:1), 1080×1350 (4:5)
- Instagram Story/Reels: 1080×1920 (9:16)
- LinkedIn Single Image: 1200×627 (1.91:1)
- LinkedIn Story: 1080×1920 (9:16)
- Meta Feed: 1080×1080 (1:1), 1200×628 (landscape)
- Google Display: 300×250, 728×90, 300×600, 160×600, 970×250
- YouTube Thumbnail: 1280×720 (16:9)
- Twitter/X: 1200×675 (16:9)

**Composition rules for all social:**
1. Deploy Red used as accent only — never as a full background
2. Logo always in top-left or bottom-left, never centered
3. Headline: Avenir Black, white or Navy
4. Data/stat callouts: Avenir Black, Deploy Red
5. Background: Navy section OR professional photography with dark overlay

---

## Motion Principles

Animation is brand-native — the Deeploy mark itself implies motion (descending squares suggest acceleration, momentum).

- Default easing: `cubic-bezier(0.16, 1, 0.3, 1)` (expo out)
- Duration: 120ms (micro), 220ms (standard), 380ms (emphasis), 600ms (page)
- Animate `transform` and `opacity` only — never layout properties
- Staggered reveals for lists: 40ms delay between items
- No bounce or elastic easing

---

## File Structure

```
DeeployBrand/
├── CLAUDE.md                    ← this file — AI brand reference
├── README.md
├── .impeccable.md               ← design context for Claude Code
├── assets/
│   └── logos/
│       ├── logo-primary.svg     ← red mark + navy wordmark (800×300)
│       ├── logo-white.svg       ← all white (800×300)
│       ├── logo-black.svg       ← all navy (800×300)
│       ├── mark.svg             ← squares + D, two color (600×600)
│       └── mark-white.svg       ← squares + D, white (600×600)
├── tokens/
│   ├── colors.json
│   ├── typography.json
│   ├── spacing.json
│   └── tokens.css               ← import this in any web project
├── brand/
│   └── index.html               ← visual brand book (GitHub Pages)
└── templates/
    ├── social/specs.json
    └── marketing/specs.json
```

---

## Quick-Start for Developers

```html
<!-- In any web project, import the token stylesheet -->
<link rel="stylesheet" href="https://raw.githubusercontent.com/[org]/DeeployBrand/main/tokens/tokens.css">

<!-- Or copy tokens.css locally -->
@import url('./tokens/tokens.css');
```

```css
/* Then use tokens directly */
.button-primary {
  background: var(--color-red);
  color: var(--color-white);
  font-family: var(--font-primary);
  font-weight: var(--font-weight-heavy);
  letter-spacing: var(--tracking-wide);
}
```

---

## Quick-Start for Design Automation

When generating marketing or social content for Deeploy, always:
1. Use Deploy Red (`#d81d4d`) as accent only — not as full background
2. Use Blue King (`#0e2d3f`) for dark sections and primary text
3. Font: Avenir Black for headlines, Avenir Book for body
4. Avoid purple, cyan, neon, gradients — these are explicitly not Deeploy
5. Include logo (white version on dark, primary on light)
6. Keep composition clean — generous white space
7. Lead headline with a result or credential, not a service description
