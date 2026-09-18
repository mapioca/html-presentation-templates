# AGENTS.md — operating manual for coding agents

This repo is a library of reusable single-file HTML slide-deck templates.
Each template lives in `templates/<template-id>/index.html` and is fully
self-contained: no build step, no npm, no CDN dependencies. A deck opens from
`file://`, works offline, and prints cleanly.

## How to build a deck for the user

1. **Read `index.json`.** Match the user's brief (tone, audience, language) to
   a template's `tags` and `description`. When in doubt, ask the user which
   template to use — never restyle a template into a different visual system.
2. **Copy, don't edit in place.** Copy `templates/<id>/` to a new working
   folder (e.g. `~/workspace/decks/<topic>/`). The library copies stay pristine.
3. **Configure the script block** at the bottom of the HTML:
   - `CONFIG`: labels, nav hint, and a unique `fontStorageKey` per deck.
   - `LESSON_PLAN`: the sections with `{ id, name, minutes }`.
4. **Replace the sample slides.** Keep one sample of each component you need as
   a reference, then write the real content into `<section class="slide">`
   blocks. Available components (see the sample slides):
   - `.eyebrow`, `.ornament`, `h1/h2/h3`
   - `.tag` + activity class: `leer ver analizar meditar actividad informar compromiso`
   - `.timer` (pill with a per-slide time budget)
   - `.card` + activity class (gold top accent, colored side spine)
   - `blockquote` + `cite` (centered quote with gold quotation mark)
   - `table.budget`, `.columns`, `.video-wrap`
   - `.slide.divider` + `.ghost-num` (section dividers)
5. **Tag every content slide** (timeline templates only — `elegant-paper`)
   with `data-section="<LESSON_PLAN id>"` and
   `data-min="<minutes elapsed within that section>"`. This drives the
   timeline footer: per-section progress, remaining time, and elapsed-vs-total.
   Cover/agenda slides omit these attributes. General templates (like
   `keynote`) have no timeline: skip `LESSON_PLAN` and the tags entirely.
6. **Offline video:** download the video (e.g. `yt-dlp -f "bv*[ext=mp4]+ba[ext=m4a]/b[ext=mp4]/b" --merge-output-format mp4`)
   and place the `.mp4` next to the HTML file; set it as the `<video>` `src`.
   Verify the file is valid (h264/AAC) — a missing file shows a generic
   "no video with supported format" error in the browser.
7. **All type is rem-based.** The A−/100%/A+ control scales the root font size
   (70%–200%), so every text element scales proportionally. Don't set fixed
   pixel font sizes on new elements.

## How to add a new template to the library

1. Create `templates/<new-id>/index.html` (single file, self-contained).
2. Add `templates/<new-id>/metadata.json` (same shape as the existing ones).
3. Register it in the root `index.json` `templates` array.
4. Capture three thumbnails at 1280×800 — `cover.png`, `mid.png`, `later.png`
   (cover · mid-deck · later) — into `templates/<new-id>/thumbnails/`.
   Headless Chromium works: open the file, navigate via `#sN` hash, screenshot.
5. Add a gallery section to `README.md` following the existing pattern.

## Template component quick-reference

- **elegant-paper** (facilitator, timeline): `.eyebrow` `.tag.leer|ver|analizar|meditar|actividad|informar|compromiso`
  `.timer` `.card` `blockquote`+`cite` `table.budget` `.columns` `.video-wrap` `.slide.divider`+`.ghost-num`
- **keynote** (Apple, Liquid Glass): `.eyebrow` `.btn` `.link-arrow` `.liquid` `.shape.s1–s5`
  `.cards3` `.columns` `.stat-row` `blockquote.quote` `table.spec` `.video-wrap` `.slide.dark` `.agenda`
- **atelier** (fashion editorial): `.masthead` `.kicker` `h1.display`+`em` `.lede` `.colophon`
  `.dropcap` `.body-copy` `.figure`+`figcaption` `blockquote.ed` `.tri` `.principles` `.video-wrap`
- **deco** (art deco, gold): `.frame` (double) `.rays` `.deco-label` `h1.deco`+`em` `.chevrons`
  `.tri`+`.rn` `blockquote.dq` `.video-wrap` `.slide.dark` `.slide.light`
- **washi** (Japanese minimal): `.enso` `.hanko` `.vtext` `h1.zen`/`h2.zen`+`b` `.rule-red`
  `.principles`+`.n` `blockquote.zq` `.foot` `.video-wrap`

## Conventions

- One template = one visual system. Don't mix systems inside a deck.
- **No gradients, ever.** Solid colors only — this is a standing user rule.
  (Hard-stop 1px hairlines drawn with `linear-gradient` for the grid technique
  are fine; visible color transitions are not.)
- Sample content in a template should demonstrate every component, with
  `[BRACKETED]` placeholders where the user fills in.
- Keep chrome strings (nav hints, timeline labels) in the deck's language via
  `CONFIG`; keep code comments in English.
- Never add external font/CDN dependencies — offline-first is a hard rule.
