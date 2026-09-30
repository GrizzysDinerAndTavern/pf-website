# Priority Fitness Design System

## Design premise

The interface should make a complicated equipment problem feel easier before the visitor ever contacts Priority Fitness. The lifecycle is the core organizing idea:

**BUY → DELIVER → INSTALL → MAINTAIN → REPAIR → MOVE → REPLACE → REMOVE**

## Color tokens

- `--pf-red: #CE202D`
- `--pf-red-dark: #A61621`
- `--ink: #101214`
- `--charcoal: #191C1F`
- `--charcoal-2: #23272B`
- `--steel: #61676C`
- `--line: #D8DCDF`
- `--mist: #F2F4F5`
- `--paper: #FFFFFF`
- `--warm: #F8F7F4`

Red is an action / selection / emphasis color, not a page-filling background system.

## Typography

### Display
**Barlow Condensed**
- 600 / 700 / 800
- Uppercase or tight headline casing
- Large scale, short line lengths

### UI / body
**Inter**
- 400 / 500 / 600 / 700 / 800
- Forms, navigation, paragraphs, labels, buttons

## Geometry

- Mostly square corners
- Small `3–8px` radius only where it improves polish
- Thin industrial rules / dividers
- No floating SaaS-card aesthetic
- Wide editorial photography

## Page rhythm

Preferred visual cadence:

**LIGHT → DARK → LIGHT → DARK → LIGHT**

This rhythm keeps long service pages from becoming a monochrome scroll tunnel.

## Button hierarchy

1. Red primary CTA
2. Charcoal / black secondary CTA
3. Border-only light or dark secondary

CTA arrows move slightly on hover. No glow effects.

## Responsive behavior

Desktop:
- expansive photography
- asymmetric grids
- full lifecycle rail
- sticky proof blocks where useful

Tablet:
- controlled grid collapse
- touch-friendly controls
- two-column patterns where space permits

Mobile:
- lifecycle becomes horizontal swipe / scroll
- high-intent pages can use sticky Call / Request Service bar
- forms collapse to one column
- minimum practical touch target ~48px
- no horizontal page overflow

## Motion

Allowed:
- subtle reveal
- image crossfade
- active-state transition
- hover scale
- arrow movement

Not used:
- scroll hijacking
- autoplay audio
- custom cursor
- WebGL
- heavy 3D

`prefers-reduced-motion` is respected.
