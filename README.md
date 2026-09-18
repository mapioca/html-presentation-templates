# html-presentation-templates

A library of reusable single-file HTML slide-deck templates, designed so that
any coding agent can pick the right one and produce a beautiful deck on the
user's behalf, automatically.

Each template is **one self-contained `.html` file**: no build step, no
dependencies, no CDN. Open it from `file://`, present it offline, print it.

Agents using the library should read [AGENTS.md](AGENTS.md). It's the
operating manual: how to read `index.json`, match the user's brief to a
template, clone it, and adapt the content.

## Get started

Copy this to your coding agent:

```
Clone https://github.com/<you>/html-presentation-templates and follow the instructions in AGENTS.md
```

## Gallery

All templates. Three slides per template (cover · mid-deck · later) to give a
sense of how each visual system handles different layouts. Click any template
name to open its folder — the HTML, metadata, and thumbnails are all there.

### [Elegant Paper](templates/elegant-paper/)

| Cover | Mid-deck | Later |
|---|---|---|
| ![cover](templates/elegant-paper/thumbnails/cover.png) | ![mid](templates/elegant-paper/thumbnails/mid.png) | ![later](templates/elegant-paper/thumbnails/later.png) |

> Warm paper background, Didone serif display titles with a sturdier Georgia
> for body headings, gold accents and ornaments. Built for facilitators:
> labeled activity tags (leer / ver / analizar / meditar / actividad /
> informar / compromiso), timed section dividers, a live lesson-timeline
> footer, offline video embeds, and an on-the-fly font-size control (A− /
> 100% / A+) for room readability.

## Template catalog

| Template | Description | Tags |
|---|---|---|
| [Elegant Paper](templates/elegant-paper/) | Premium facilitator deck: warm paper, serif titles, gold accents, section timeline, font-size control, offline video | `elegant` `premium` `serif` `facilitator` `timeline` `offline-video` `font-control` |

Machine-readable catalog: [`index.json`](index.json).
