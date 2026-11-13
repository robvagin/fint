# FINT

Ukrainian letters for any font. Version 0.9.

Many fonts ship with Russian Cyrillic and stop there: no Ґ, Є, І, Ї. FINT opens a `.ttf` or `.otf`, builds the
missing letters from the font's own parts and writes them back into the same file.

**Open it:** https://robvagin.github.io/fint/

## What it does

- **Є** takes the font's own С and the crossbar of its own Э, mirrored.
- **Ґ** takes the font's own Г and adds the upturn, measured from the arm of that Г. A cursive г gets the upturn at its start.
- **Ї** takes I and two dots from the font's own dieresis, set closer the Ukrainian way.
- **І** is the Latin I.
- The apostrophe ʼ comes from the font's own quote.
- Kerning, OpenType features and the slant stay in place: the letters are inserted into the source file, the font is not rebuilt.
- Real Ukrainian text in seven blocks: every letter FINT added sits on a grey mark, and the letters themselves are shown first, large, above the whole alphabet.

A font with no Cyrillic at all gets a whole Cyrillic set, built from its Latin. Look through the letters before you use
the font: this part is younger than the Ukrainian one. Add `?scope=all` to the address to see the demo font rebuilt this way.

## Settings

- **Build:** only the missing letters, or the whole Cyrillic from Latin.
- **Ё Ъ Ы Э:** add them or leave them out.
- **Ї dots:** set closer the Ukrainian way, or as wide as the Latin dieresis.
- **Ґ upturn:** low, regular or tall.
- **Name suffix:** what is added to the family name of the saved font, `UA` by default.
- **View:** before, after and, in the demo, the designer's original; new letters marked or clean.

Settings sit below the letters, folded: the page opens with the result, not with choices.

## Privacy

Everything runs in your browser. The font never leaves your computer. The only network request happens on the first
save: the page loads Pyodide and fontTools (about 10 MB) to write the file.

## Fonts and licenses

FINT changes a font file. Whether you may do that, and whether you may pass the result on, depends on the license of
that font. Open licenses such as the SIL OFL allow it; many commercial licenses do not. FINT shows a note when a font
does not state an open license.

The demo uses Onest Regular (SIL OFL 1.1) with its Ukrainian letters hidden, so the page can show the designer's
originals next to the rebuilt ones.

## Run it locally

Open `index.html` in a browser. No build step, no server.

## License

[MIT](LICENSE) © 2026 Robert Vagin. Third-party software: [licenses/THIRD-PARTY.md](licenses/THIRD-PARTY.md).
