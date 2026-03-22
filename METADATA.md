# TONARI LABS — Metadata & Naming Convention

This document defines the standard metadata patterns for all Tonari Labs properties.
Follow this for every new page, tool, or academy material.

---

## Title Pattern

| Type | Format | Example |
|------|--------|---------|
| Main site | `TONARI LABS — INNOVATIVE AUDIO TECHNOLOGIES` | tonari.ai |
| Tool / App | `APP NAME — TONARI LABS` | `TUTOR — TONARI LABS`, `FOLEY — TONARI LABS` |
| Academy hub | `AUDIO ACADEMY — TONARI LABS` | academy.tonari.ai |
| Academy course | `COURSE @ AUDIO ACADEMY — TONARI LABS` | `BEAT @ AUDIO ACADEMY — TONARI LABS` |
| Lab / Research | `LAB LOGS — TONARI LABS` | lab.tonari.ai |
| Lab post | `Post Title — TONARI LABS` | individual blog posts |

**Rules:**
- `TONARI LABS` is always fully capitalized when used as a title or header. Never "Tonari Labs" in titles.
- App/tool names are always fully capitalized in titles: `TUTOR`, `FOLEY`, `PITCHPUP`, `BEAT`, `HARMONY HASH`
- The subtitle "INNOVATIVE AUDIO TECHNOLOGIES" is always fully capitalized wherever it surfaces.
- Use `—` (em dash), not `-` (hyphen), as the separator.
- Academy courses use `@` to denote they belong to Audio Academy: `BEAT @ AUDIO ACADEMY`
- Never write "TONARI LAB" (singular). It's either "TONARI LABS" (the org) or "LAB LOGS" (the blog).

---

## Description Pattern

Descriptions are **normal case** and use **short, punchy sentences**. No corporate filler.

| Property | Description |
|----------|-------------|
| tonari.ai | Tools for musicians. Sounds for games. Education for everyone. |
| Tutor | Structured, high-impact interview practice assistant for multi-lingual candidates. |
| Harmony Hash | Interactive chord explorer. Discover harmony across keys and modes. |
| Beat | Explore music production basics from a core concept: the beat. Feel the rhythm through bite-size interactive lessons. |
| Audio Academy | Learn about music production and the creative process through play. Interactive toys for every level. Prerequisite: don't stress, have fun, be you. |
| Lab Logs | Research and build logs from TONARI LABS — documenting experiments in audio ML, sound design tools, and music technology. |
| PitchPup | Train your ear. Tune your instrument. A pitch detection and ear training tool. |
| Foley | Interactive audio fabrication for game and film sound design. |

---

## Required Meta Tags

Every Tonari Labs page must include all of these:

```html
<title>APP NAME — TONARI LABS</title>
<meta name="description" content="..." />
<meta name="theme-color" content="#09090b" />
<link rel="icon" type="image/png" href="/favicon.png" />

<!-- Open Graph -->
<meta property="og:type" content="website" />
<meta property="og:url" content="https://subdomain.tonari.ai" />
<meta property="og:title" content="APP NAME — TONARI LABS" />
<meta property="og:description" content="..." />
<meta property="og:image" content="https://tonari.ai/brand/og-appname.png" />
<meta property="og:image:width" content="1200" />
<meta property="og:image:height" content="630" />

<!-- Twitter / X -->
<meta name="twitter:card" content="summary_large_image" />
<meta name="twitter:title" content="APP NAME — TONARI LABS" />
<meta name="twitter:description" content="..." />
<meta name="twitter:image" content="https://tonari.ai/brand/og-appname.png" />
```

**Critical rules:**
- `<title>`, `og:title`, and `twitter:title` must always match exactly.
- `og:description` and `twitter:description` must always match exactly.
- `og:image` and `twitter:image` must always match exactly.
- All OG images are hosted at `tonari.ai/brand/og-{appname}.png` (1200×630).
- OG images are generated via `tonarilabs-web/scripts/gen-og-images.cjs`.
- `og:url` must use the canonical `tonari.ai` domain (not `tonarilabs.com`).

---

## OG Image Generation

All OG images use the design system fonts and colors. Generate with:

```bash
cd /Volumes/TONARI_DRIVE/Dev/tonarilabs/tonarilabs-web
node scripts/gen-og-images.cjs
```

To add a new app, edit `scripts/gen-og-images.cjs` and add an entry to the `apps` array.

---

## Color Accents by Category

| Category | Accent | Token | Use for |
|----------|--------|-------|---------|
| Tools | Gold | `--palette-gold`, `--text-accent` | Harmony Hash, Tutor, Foley, PitchPup |
| Academy | Sky blue | `--palette-sky`, `--text-academy` | Audio Academy, Beat, Funk, future courses |
| Lab / Research | Gold | `--palette-gold` | Lab Logs, Patch Pilot |
