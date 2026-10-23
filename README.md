# Anokath

A fourteen-segment display face after the Burroughs B-7971, a mid-1960s
neon alphanumeric tube best known from Ultronic Letrascan stock tickers.

Reference: [display-tubes.org, Burroughs B-7971](https://display-tubes.org/other/burroughs-b-7971/).

## The layout

```
  TL ------A------ TR
  |  \     |     /  |
  F   H    I    J   B
  |     \  |  /     |
  ML--G1--MM--G2---MR
  |     /  |  \     |
  E   K    L    M   C
  |  /     |     \  |
  BL ------D------ BR

  ---------U---------
```

Fourteen wire cathodes on one plane, plus a fifteenth underscore wire below
the character. The single wires across the top and bottom are what separate
this from a sixteen-segment display. The segment set for each glyph is read
off photographs of the tube lighting every character.

An outline font cannot draw light, so a lit cathode here is a flat stroke of
the glow's width. On the tube the glow runs straight through every node, so
two lit wires that share one read as a single stroke with a square corner.

## Character set

A-Z, 0-9, space, `- _ + * / \ < > =`. The tube has no lowercase and no
decimal point, so neither does the font. The figures follow the tube, which
reaches for diagonals more than a modern display would. The punctuation is
not on the tube and is this font's own.

## Styles

`wght` 300-700. Static instances: Light, Regular, Medium, Bold.

## ss01: Unlit

Each glyph has an `.unlit` twin holding the wires it leaves dark, drawn at
the bare-wire width on the same centre-lines. Set a run twice at the same
position, once plain and once with `ss01`, in two colours, and the dark cage
shows behind the lit cathodes.

```css
.lit   { font-family: "Anokath"; color: #ff7a1a; }
.unlit { font-family: "Anokath"; color: #3a2a20; font-feature-settings: "ss01"; }
```

## Files

```
fonts/
  variable/   Anokath[wght].ttf
  ttf/        static TrueType, one per instance
  otf/        static CFF OpenType, one per instance
  webfonts/   woff2 and fonts.css
OFL.txt       license
```

## License

Copyright 2026 Durable Programming, LLC. Anokath is licensed under the
[SIL Open Font License, Version 1.1](OFL.txt).

Published by [Cast Iron Type](https://castirontype.com). Designed by
David J Berube.
