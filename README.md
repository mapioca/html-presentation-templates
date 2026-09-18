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

### [Keynote](templates/keynote/)

| Cover | Mid-deck | Later |
|---|---|---|
| ![cover](templates/keynote/thumbnails/cover.png) | ![mid](templates/keynote/thumbnails/mid.png) | ![later](templates/keynote/thumbnails/later.png) |

> Apple-inspired general presentation template with Liquid Glass: SF type
> stack, giant tight headlines, Apple blue, pill buttons, frosted refractive
> glass cards floating over solid color — zero gradients. Solid-black
> statement and closing slides, agenda, quote, stats, two-column with
> offline video slot, spec table, and the A−/100%/A+ font control. No
> lesson timeline: built as a general Canva substitute.

### [Atelier](templates/atelier/)

| Cover | Mid-deck | Later |
|---|---|---|
| ![cover](templates/atelier/thumbnails/cover.png) | ![mid](templates/atelier/thumbnails/mid.png) | ![later](templates/atelier/thumbnails/later.png) |

> Fashion-editorial general presentation template: ivory paper, ink black,
> rouge accents, Didone serif display titles with italic accent words,
> small-caps kickers, a masthead bar with issue numbering on every slide,
> drop-cap editorial columns, stat band, quote, process, agenda, an offline
> video slot, and the persisted A−/100%/A+ font control. Zero gradients,
> no timeline.

### [Deco](templates/deco/)

| Cover | Mid-deck | Later |
|---|---|---|
| ![cover](templates/deco/thumbnails/cover.png) | ![mid](templates/deco/thumbnails/mid.png) | ![later](templates/deco/thumbnails/later.png) |

> Gilded art-deco general presentation template: deep emerald and cream
> slides, solid gold ornament, a double gold frame on every slide,
> sunburst ray texture, chevron dividers, roman numerals, Georgia serif
> headlines, stat band, quote, process, agenda, an offline video slot, and
> the persisted A−/100%/A+ font control. Zero gradients, no timeline.

### [Washi](templates/washi/)

| Cover | Mid-deck | Later |
|---|---|---|
| ![cover](templates/washi/thumbnails/cover.png) | ![mid](templates/washi/thumbnails/mid.png) | ![later](templates/washi/thumbnails/later.png) |

> Japanese-minimalist general presentation template: warm stone background,
> sumi ink, vermillion hanko seals, an ensō circle, vertical accent text,
> vast whitespace, light-weight sans headlines with Georgia italic quotes,
> stat band, process, agenda, an offline video slot, and the persisted
> A−/100%/A+ font control. Zero gradients, no timeline.



## Template catalog

| Template | Description | Tags |
|---|---|---|
| [Elegant Paper](templates/elegant-paper/) | Premium facilitator deck: warm paper, serif titles, gold accents, section timeline, font-size control, offline video | `elegant` `premium` `serif` `facilitator` `timeline` `offline-video` `font-control` |
| [Keynote](templates/keynote/) | Apple-inspired general deck: Liquid Glass, SF type, pill buttons, solid black statement/closing, font-size control, offline video | `apple` `minimal` `liquid-glass` `general` `font-control` `offline-video` `premium` |
| [Atelier](templates/atelier/) | Fashion-editorial general deck: ivory, ink, rouge, Didone serif, masthead bars, font-size control, offline video | `editorial` `fashion` `serif` `elegant` `general` `font-control` `offline-video` `premium` |
| [Deco](templates/deco/) | Gilded art-deco general deck: emerald, gold ornament, double frames, roman numerals, font-size control, offline video | `art-deco` `gold` `luxury` `elegant` `general` `font-control` `offline-video` `premium` |
| [Washi](templates/washi/) | Japanese-minimalist general deck: stone, ink, vermillion seals, whitespace, font-size control, offline video | `japanese` `minimalist` `zen` `elegant` `general` `font-control` `offline-video` `premium` |

Machine-readable catalog: [`index.json`](index.json).
