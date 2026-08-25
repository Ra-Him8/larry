# Larry — character & identity pitch

An eight-sheet scrolling pitch for **Larry**, a mascot-led cat food brand.
Presented as an animation studio model sheet: turnaround, expression range,
icon system, and two brand territories the viewer can switch between.

**Live:** https://ra-him8.github.io/larry/

## What's here

| Path | What it is |
|---|---|
| `index.html` | The page. 33 KB — assets stream in from `assets/`, so it paints immediately on mobile. |
| `assets/` | 22 stills and 3 films, already compressed for web (2.9 MB total). |
| `larry-offline.html` | The same page with **everything embedded** in one 3.8 MB file. No internet needed — use this one if the meeting room wifi is bad. |
| `.nojekyll` | Stops GitHub Pages running the files through Jekyll. |

## The eight sheets

1. **Cover** — Larry's 10s loop
2. **The case** — why a character beats a photograph
3. **Model sheet** — turnaround, walk cycle, named poses
4. **Expression range** — 8 selectable moods (the core of the pitch)
5. **Icon system** — reduction down to a favicon, plus the seamless pattern
6. **Territories** — A/B switch between the Playful and Premium routes
7. **Off screen** — walk-around costume and inflatable
8. **The ask** — next steps

## Editing

The page is one self-contained HTML file — styles and script are inline, no
build step and no dependencies. Edit `index.html` directly and push.

Two things to know before you change colours:

- Every colour is a CSS custom property at the top of the `<style>` block, and
  each one is defined three times: bare `:root` (light), a
  `prefers-color-scheme: dark` block, and a `[data-theme="dark"]` block. Change
  all three or the page will render one theme's text on the other theme's
  background.
- `--plate` is baked into the artwork — the hero film's background was recoloured
  to match it. If you change `--plate`, re-render the film to match.

Fonts come from Google Fonts (Bricolage Grotesque, Newsreader, Martian Mono).
`larry-offline.html` still needs a connection for those; everything else in it
is embedded.

## Regenerating

Source artwork lives outside this repo, in `laary1/`. The web assets here were
derived from it — stills resized and re-encoded, films re-compressed, and the
cutout PNGs background-removed by flood-filling inward from the border (a plain
colour key eats Larry's white chest and paws).
