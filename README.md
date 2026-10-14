# ZX Spectrum Pixel Painter

A single-page, offline pixel editor for ZX Spectrum sprite sheets stored as PNG. Open `index.html` in Chrome or Edge; there is nothing to install and files never leave your machine.

## How it works

- **Palette** is every colour in the file, in order of first appearance (scanning left to right, top to bottom), shown in rows of 10.
- **Frame colour** is the top-left pixel's colour. It is left out of the palette, can't be painted over, and fills stop at it.
- **Transparent colour** is `#646464`. It always has its own swatch on the `` ` `` key.
- **Save** writes the PNG back in the format it was opened in: same colour type, bit depth, palette order and interlacing, with other chunks copied through unchanged.

## Controls

| Input | Action |
|---|---|
| Left click / drag | Paint with the selected colour |
| Right click / drag | Restore pixels to their colour when the file was opened |
| `B` | Pencil |
| `G` | Fill (exact match, 4-way). Right-click restores the region |
| `I` | Picker (returns to the previous tool) |
| `1`–`0` | Colours 1–10 |
| `Shift` + `1`–`0` | Colours 11–20 |
| `` ` `` | Transparent |
| Arrow keys | Move through the palette grid |
| Mouse wheel | Zoom around the cursor (whole-number steps) |
| `Space` + drag, or middle drag | Pan |
| `Home` | Fit to window |
| `Ctrl+Z` / `Ctrl+Y` | Undo / redo |
| `Ctrl+O` / `Ctrl+S` | Open / save |

When a file is opened with `Ctrl+O` or dragged in, `Ctrl+S` writes straight back to it in Chrome and Edge. Other browsers download a copy instead.
