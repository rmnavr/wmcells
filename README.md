# WMCells — visually organized stylesheet for Mathematica notebooks

WMCells is stylesheet for proper visual structuring of Wolfram Mathematica cells (inside notebooks).

<p align="center">
<img src="https://github.com/rmnavr/wmcells/blob/main/docs/demo.png?raw=true" alt="WM Cells Stylesheet" />
</p>

Use following hotkeys to assign style of selected cell (or for creating new cell):
* `Alt+1..6` — headers (they have logically expected grouping)
* `Alt+7` — Text
* `Alt+8` — Input cell
* `Alt+9` — Output cell

As a nice feature, WMCells makes Input cells to have «Deactivate cell» button (see green ▲ symbol).
Deactivated cells will not be executed either by hand or by «Evaluate Notebook» command.
> Those ▲-buttons are implemented via CellDingbat option

All style info can be seen and edited inside "Format -> Edit stylesheet..." menu.
For reference, stylesheet of `wmcells.nb` looks like this:

<p align="center">
<img src="https://github.com/rmnavr/wmcells/blob/main/docs/style_def.png?raw=true" alt="WM Cells Stylesheet" />
</p>

# Usage

> WMCells stylesheet was tested mainly on WM version 12.2.
> It should work in earlier and later versions too.

Simply download `wmcells.nb` file, delete demo cells and start programming.

If you want to update existing notebook with WMCells style, you can copy stylesheet cells of `wmcells.nb`
(access them via "Format -> Edit stylesheet..."), and paste them in stylesheet of your notebook.
Don't forget to delete your original stylesheet cells.
> Be aware that if you are using other cells styles that are used in `wmcells.nb` (Title, Chapter, Subchapter...), 
> you'll have to apply `Alt+1..6` styles to such cells by hand.
> 
> Also, cells with user-overriden styles (defined for particular cell, rather than at cells-style-definition level)
> will mix their style with `wmcells.nb` styles.

# Adding WMCells style to Stylesheet menu

You can make WMCells style accessible from «Format -> Stylesheet -> ...» menu.

> I am personally not a big fan of this method, because if you'll send your file to a college who has no WMCells style installed in the same way,
> he'll get very poorly styled document.

How to do it:
1. Create empty `wmcells_style.nb` file (or rename it to your taste)
2. Copy style-defining cells of `wmcells.nb` (which are accessed through «Format -> Edit stylesheet...» menu)
3. Paste these cells DIRECTLY into `wmcells_style.nb` file (NOT into it's «Format -> Edit Stylesheet...» menu)
4. Save `wmcells_style.nb` and put it in folder `D:\Soft\WM\SystemFiles\FrontEnd\StyleSheets` (change folder to your WM installation path)
5. Reload WM, and you'll see «wmcells_style» in «Format -> Stylesheet -> ...» menu

