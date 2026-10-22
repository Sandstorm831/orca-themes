# orca-themes

Terminal themes for [Orca](https://onorca.dev) that stay readable with deuteranopia (red-green colour blindness).

For deuteranopes, ANSI red and green, the colours behind git diffs and pass/fail output, fold into the same brown. Each theme here keeps them apart on the blue-yellow axis and by lightness. Every theme was checked through a full-strength deuteranopia simulation (Machado 2009) using CIEDE2000 colour difference.

## Themes

| Theme | Mode | Red/green gap | Origin |
| --- | --- | --- | --- |
| Secant Night | dark | 39 | Built from the Secant design palette |
| GitHub Dark Colorblind (Fixed) | dark | 58 | GitHub Dark Colorblind with its duplicate blue and red/yellow clash fixed |
| Rose Pine Moon (CB Fixed) | dark | 29 | Rose Pine Moon with blue, magenta and cyan re-tuned |
| London Embankment Dusk | dark | 22 | Unchanged from iTerm2-Color-Schemes |
| Synthwave | dark | 22 | Unchanged from iTerm2-Color-Schemes |
| Kurokula | dark | 24 | Unchanged from iTerm2-Color-Schemes |
| Secant Paper | light | 43 | Built from the Secant design palette |
| GitHub Light Colorblind | light | 61 | Unchanged from iTerm2-Color-Schemes |

The gap is the CIEDE2000 difference between ANSI red and green as a deuteranope sees them. Above 20 reads as clearly different. For comparison, Tango Light, Orca's default light theme, scores 8.

## Install on a new machine

1. Clone this repo.
2. In Orca, open **Settings → Terminal**, then the theme picker, and click **Import from YAML**.
3. Select every file in `themes/`.
4. Pick a dark theme. Set the light theme to **GitHub Light Colorblind** or **Secant Paper**, so a system switch to light mode doesn't fall back to Tango Light.

Two things the import doesn't cover:

- Claude Code draws its own red/green diff backgrounds. Run `/theme` in Claude Code and choose a colour-blind-friendly option.
- To rotate themes, pick another one in the same theme picker.

## Format

The files use Warp's YAML theme format, which Orca imports natively: `background`, `foreground`, `cursor`, `accent`, `details` (`darker` or `lighter`) and `terminal_colors.normal` / `terminal_colors.bright`.

## Credits

London Embankment Dusk, Synthwave, Kurokula and GitHub Light Colorblind, plus the bases of the two "Fixed" themes, come from [iTerm2-Color-Schemes](https://github.com/mbadolato/iTerm2-Color-Schemes) by Mark Badolato and contributors, under the MIT License (see `THIRD_PARTY_LICENSE`).
