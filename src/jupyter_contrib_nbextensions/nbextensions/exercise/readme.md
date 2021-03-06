# Exercises extensions

These are two extensions for Jupyter, for hiding/showing solutions cells. They use the same approach and codebase and differ only by the type of <code>cell widget</code> used the show/hide the solutions. The two extensions can be used simultaneously. They require the <code>rubberband</code> extension to be installed and enabled.

The example below demonstrates some of the features of the exercise extensions.

- First, an solution or "details" cell is created by (a) selecting two cells with the rubberband and (b) clicking on the menu-button [exercise extension]
- Second, the two next cells are selected using the keyboard shortcut Shift-J and a solution is created using the shortcut Alt-D [exercise2 extension]
- Third, the two solutions are expanded by clicking on the corresponding widgets
- Fourth, the solutions are removed by selecting them and clicking on the buttons in the toolbar.

![](image.gif)


## The extensions provide

- a menubar button
- a cell widget -- A plus/minus button in <code>exercise</code> and a sliding checkbox in <code>exercise2</code>.

The menubar button is devoted to the creation or removing of the solution. The solution consists in several consecutive cells that can be selected either by multicell selection (*Shift-J* (select next) or *Shift-K* (select previous) keyboard shortcuts --
*Shift-up* and *Shift-down* will probably work in a near future) or using the <a href="https://github.com/ipython-contrib/jupyter_contrib_nbextensions/wiki/Rubberband" target="_blank">rubberband extension</a>.

**Creating a solution **
Several cells being selected, pressing the menubar button adds a <code>cell widget</code> and hides the cells excepted the first one which serves as a heading cell. *Do not forget to keep the Shift key pressed down while clicking on the menu button
(otherwise selected cells will be lost)*. It is also possible to use a keyboard shortcut for creating the solution from selected cells: Alt-S for exercise extension and Alt-D for exercise2.

**Removing a solution** If a solution heading (first) cell is selected, then clicking the menu bar button removes this solution and its solutions cells are shown. Using the keyboard shortcut has the same effect.

**Showing/hiding solution**  At creation of the solution, the solution cells are hidden. Clicking the <code>cell widget</code> toggles the hidden/shown state of the solution.

**Persistence** The state of solutions, hidden or shown, is preserved and automatically restored at startup and on reload.  <

**Internals** exercise and exercise2 add respectively a solution and solution2 metadata to solution cells, with for value the current state hidden/shown of the solution. For exercise, a div with the plus/minus character is prepended to the solution heading cell. For exercise2, a flex-wrap style is added to the solution heading cell and a checkbox widget, with some css styling, is appended to the cell.

