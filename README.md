# WMCells — visually organized stylesheet for Mathematica notebooks

WMCells is stylesheet for proper visual structuring of Wolfram Mathematica cells (inside notebooks).

WMCells provides following features:
* Makes cells hierarchy clearly visible, header cells have logically expected grouping
* Visually distinguishes Input cells from Output cells
* Implements nice indents for every cell style (for Headers/Input/Output/Print/Echo/Error cells)
* Introduces «Deactivate cell» button (see green triangle) for Input Cell — deactivated cells will not be executed either by hand or by «Evaluate Notebook» command

<p align="center">
<img src="https://github.com/rmnavr/wmcells/blob/main/docs/demo.png?raw=true" alt="WM Cells Stylesheet" />
</p>

Use following hotkeys to assign style of selected cell (or for creating new cell):
* `Alt+1..6` — headers
* `Alt+7` — Text
* `Alt+8` — Input cell
* `Alt+9` — Output cell

All style info can be seen with «Format -> Edit stylesheet...» command.
For reference, stylesheet of `wmcells.nb` looks like this:

<p align="center">
<img src="https://github.com/rmnavr/wmcells/blob/main/docs/style_def.png?raw=true" alt="WM Cells Stylesheet" />
</p>

# Usage

WMCells stylesheet was tested mainly on WM version 12.2.
It should work in earlier and later versions too, although can't guarantee it.

## Usage from scratch (recommended option)

Use `wmcells.nb` file directly. Just delete all demo cells.
Use fresh `wmcells.nb` file for every new notebook.

## Applying WMCells style to existing notebooks

You have 2 options, but both of them will have following limitations:
* If you are using same styles for headers as used in `wmcells.nb` (Title, Chapter, Subchapter...), all will work OK.
  But if some cells do not change automatically — you are probably using styles that are not used in `wmcells.nb` (like Subtitle, Subitem, ...).
  You'll have to apply `Alt+1..6` styles to such cells by hand.
* If you have cells with user-overriden styles (defined for particular cell, rather than at cells-style-definition level),
  automatic style update will probably mix with this overriden style

### Option 1

Pasting cells from another notebook to `wmcells.nb` will automatically update those cells to `wmcells.nb` style.

### Option 2

Applying `wmcells.nb` style to existing notebook.

How to do it:
1. Open `wmcells.nb`.
2. Open «Format -> Edit stylesheet...» menu
3. `Ctrl+C` all style-defining cells of `wmcells.nb`
4. Open your notebook (for example `your.nb`)
5. Open «Format -> Edit stylesheet...» menu
6. Delete all style-defining cells from `your.nb` file
7. Paste cells from step 3

## Adding WMCells style to Stylesheet menu

You can make WMCells style accessible from «Format -> Stylesheet -> ...» menu.

> I am personally not a big fan of this method, because if you'll send your file to a college who has no WMCells style installed in the same way,
> he'll get very poorly styled document.

How to do it:
1. Create empty `wmcells_style.nb` file (or rename it to your taste)
2. Copy style-defining cells of `wmcells.nb` (which are accessed through «Format -> Edit stylesheet...» menu)
3. Paste these cells DIRECTLY into `wmcells_style.nb` file (NOT into it's «Format -> Edit Stylesheet...» menu)
4. Save `wmcells_style.nb` and put it in folder `D:\Soft\WM\SystemFiles\FrontEnd\StyleSheets` (change folder to your WM installation path)
5. Reload WM, and you'll see «wmcells_style» in «Format -> Stylesheet -> ...» menu.

