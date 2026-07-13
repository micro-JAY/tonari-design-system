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

## App-owned semantic color systems

The shared palette governs structure: typography, geometry, surfaces, spacing, focus treatment, and standard controls. Apps may additionally define semantic tokens when color encodes domain information that the shared structural palette cannot communicate clearly.

Harmony Hash is an approved case. Its music-semantic palette must remain app-owned and must survive future design-system syncs:

- Fretboard and scale intervals use strongly distinct colors. The root remains gold, while thirds, fourths, fifths, and sevenths must be distinguishable from the root and from one another.
- Match scores use a meaningful continuum from pale pink/red at low values to pastel green at high values.
- Chord-grid suggestion modes may use contrasting palettes so suggestion categories remain easy to scan.
- Playback uses gold. Hanz focus and status cues remain separate from playback and include text, icons, shapes, or state labels so color is never the only indicator.

Do not flatten these tokens into the category accent, shared status colors, or a single tonal family during an update. A replacement is only appropriate after an app-specific accessibility review confirms that it preserves the same distinctions and non-color cues.

## Apps using this

- [tonarilabs.com](https://tonarilabs.com)
- [cadence.tonari.ai](https://cadence.tonari.ai)
- [tutor.tonari.ai](https://tutor.tonari.ai)
- [beat.tonari.ai](https://beat.tonari.ai)
- [foley.tonari.ai](https://foley.tonari.ai)
- PitchPup (webapp)

## Updating

Edit `tokens.css`, commit, and push. jsDelivr CDN caches will refresh within ~24h, or purge manually at `https://purge.jsdelivr.net/gh/micro-JAY/tonari-design-system@main/tokens.css`.
