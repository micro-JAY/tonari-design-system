# Tonari Labs Design System

Shared design tokens for all Tonari Labs applications.

## Usage

Add this to your app's `<head>`:

```html
<link rel="stylesheet" href="https://cdn.jsdelivr.net/gh/micro-JAY/tonari-design-system@main/tokens.css" />
```

Or import in CSS:

```css
@import url('https://cdn.jsdelivr.net/gh/micro-JAY/tonari-design-system@main/tokens.css');
```

## What's included

- Color palette (gold accent, warm neutrals)
- Surface/background tokens
- Typography scale (Zalando Sans + JetBrains Mono)
- Spacing, radius, shadow, motion tokens
- Interactive/button tokens (light primary, gold accent)
- Semantic status colors
- Base reset and utility classes

## Apps using this

- [tonarilabs.com](https://tonarilabs.com)
- [cadence.tonari.ai](https://cadence.tonari.ai)
- [tutor.tonari.ai](https://tutor.tonari.ai)
- [beat.tonari.ai](https://beat.tonari.ai)
- [foley.tonari.ai](https://foley.tonari.ai)
- PitchPup (webapp)

## Updating

Edit `tokens.css`, commit, and push. jsDelivr CDN caches will refresh within ~24h, or purge manually at `https://purge.jsdelivr.net/gh/micro-JAY/tonari-design-system@main/tokens.css`.
