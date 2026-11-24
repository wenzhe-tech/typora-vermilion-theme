# Vermilion

A pair of Typora themes for Chinese writing: **warm paper by day, near-black by night**, with cinnabar-red accents. Built for text-heavy explanatory documents — long paragraphs, frequent tables and quotations, dense bold text and lists, and relatively little code.

## At a glance

| | Vermilion Light | Vermilion Dark |
|---|---|---|
| File | `vermilion-light.css` | `vermilion-dark.css` |
| Page background | `#f9f6ef` (warm cream paper) | `#12100f` (warm near-black) |
| Body text | `#26231f` | `#ded7cb` |
| Accent | `#b23a2b` (cinnabar) | `#e06a51` (lifted cinnabar) |

Both themes share the same layout and hierarchy; only paper and ink change. Night mode avoids `#000`: pure black looks washed out on LCD panels and makes text appear to float, while a warm near-black keeps depth in the shadows and is easier on the eyes.

## Typography

- **Type pairing**: body text uses SF Pro Text (Latin/digits) + PingFang SC (Chinese); headings use Charter + Noto Serif SC; code uses SF Mono + Sarasa UI SC (monospaced Chinese comments). Latin fonts carry no CJK glyphs, so the stack splits scripts through fallback. Table numbers use `tabular-nums` for column alignment.
- **Measure and leading**: 54rem measure, 16px base size, roughly 49 full-width characters per line, line-height 1.72.
- **Alignment**: left by default, keeping character spacing constant. `hanging-punctuation: allow-end` lets trailing `。，、）」` hang outside the measure for a cleaner right edge. Set `--p-align: justify` if you prefer full justification.
- **Headings**: h1/h2 are serif, underlined by a 1px hairline with a 2px cinnabar segment at the left; h3 starts with a 3px cinnabar bar. Red is an accent, never a colour block.
- **Bold**: darker ink and weight 600 only, **never coloured** — in bold-heavy documents, coloured bold turns the whole page red. Italics are replaced by upright cinnabar text, avoiding ugly synthetic obliques for Chinese glyphs.
- **Quotations**: a paper-white card with a 1px border, 3px cinnabar left edge and 10px radius; no solid tinted background.
- **Tables**: the whole table sits in a light card (thin border, radius, subtle shadow) with a faint cinnabar header strip. Wide tables automatically reduce font size and padding by column count, so they usually fit without horizontal scrolling.
- **Code blocks**: a warm sand panel (one step deeper than the paper) with a thin border, visually distinct from the white table cards.
- **Lists**: cinnabar bullets and tabular numerals; dividers are short centred rules rather than full-width lines.

## Installation

1. Download `vermilion-light.css` and `vermilion-dark.css`.
2. In Typora, open Preferences → Appearance → Open Theme Folder.
3. Put both files there and restart Typora.
4. Select Vermilion Light / Vermilion Dark from the theme menu.

## Customization

Common parameters are exposed as variables at the top of `:root`:

- Measure: `#write { max-width: 54rem }` — 46rem is tighter, 60rem wider.
- Font size: `html { font-size: 16px }` — 15px denser, 17px larger; everything scales proportionally.
- Line height: `body { line-height: 1.72 }`.
- Alignment: `--p-align: left` (default) or `justify`.
- Accent: change only `--red` and `--red-deep`. True red `#c02b1d`, brownish red `#9b4b31`, softer red `#c4553f`.
- Fonts: `--font-sans` / `--font-serif` / `--font-mono` — adjust to the fonts installed on your machine.

## License

Free to use and modify. No attribution required.
