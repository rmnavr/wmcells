# WMCells — visually organized stylesheet for Mathematica

WMCells is stylesheet for proper visual structuring of Wolfram Mathematica cells (inside notebooks).

WMCells provides following features:
* Makes cells hierarchy clearly visible; Header cells have logically expected grouping
* Clearly visually distinguishes Input cells from Output cells
* Implements nice indents for every cell style (for Headers/Input/Output/Print/Echo/Error cells)
* Introduces «Deactivate cell» button (see green triangle) for Input Cell (deactivated cells will not be executed neather by hand, nor by «Evaluate All» command)

<p align="center">
<img src="https://github.com/rmnavr/wmcells/blob/main/docs/demo.png?raw=true" alt="WM Cells Stylesheet" />
</p>

Cells styles has following hotkeys:
* `Alt+1..6` — headers
* `Alt+7` — Text
* `Alt+8` — Input cell
* `Alt+9` — Output cell

All style info can be seen with «Format -> Edit stylesheet...» command.

# Usage

Stylesheet was tested mainly on WM version 12.2.
It should work in earlier and later versions too, although can't guarantee it.

## Usage from scratch

Use `wmcells.nb` file directly. Just delete all demo cells.

## Applying style to existing notebooks

To apply WMCells style to existing notebook you have 2 options.

Both options have following limitations:
* If you are using same styles as used in `wmcells.nb` (Title, Chapter, Subchapter...), all will work OK
* If some cells do not change automatically — you are probably using styles that are not used in `wmcells.nb` (Subtitle, Subitem, ...).
  You'll have to apply `Alt+1..6` styles to such cells by hand.

### Option 1

Pasting cells from another notebook to `wmcells.nb` will automatically update those cells to `wmcells.nb` style.

### Option 2

1. Open `wmcells.nb`.
2. Open «Format -> Edit stylesheet...» menu
3. `Ctrl+C` all style-defining cells of `wmcells.nb`
4. Open your notebook (for example `your.nb`) file.
5. Open «Format -> Edit stylesheet...» menu
6. Delete all style-defining cells from `your.nb` file
7. Paste cells from step 3

For reference, «Format -> Edit stylesheet...» menu of `wmcells.nb` looks like this:

<p align="center">
<img src="https://github.com/rmnavr/wmcells/blob/main/docs/style_def.png?raw=true" alt="WM Cells Stylesheet" />
</p>
