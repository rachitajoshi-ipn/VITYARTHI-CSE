Tic-Tac-Toe (Python / Tkinter)

A simple two-player Tic-Tac-Toe game built with Python's built-in tkinter GUI library.

Features
3x3 grid of clickable buttons
Turn indicator label showing whose turn it is (X or O)
Automatic win detection across all 8 winning combinations (rows, columns, diagonals)
Winning cells are highlighted in green
Draw detection when the board fills up with no winner
Popup dialog announcing the winner or a tie
Requirements
Python 3.x
tkinter (included with most standard Python installations)

No external dependencies or pip install steps are needed.

How to Run
bash
python tic_tac_toe.py

(Replace tic_tac_toe.py with whatever filename you saved the script as.)

How to Play
The game starts with Player X.
Click any empty cell to place your mark.
Players alternate turns automatically after each valid move.
The game checks for a winner after every move:
Three matching marks in a row, column, or diagonal wins the game.
The winning combination is highlighted in green, and a popup announces the winner.
If all 9 cells are filled with no winner, a "It's a tie!" popup appears.
To play again, simply restart the script (there is currently no in-app reset button).
Code Structure
Function	Purpose
check_winner()	Scans all winning combinations; highlights and announces a win if found
check_draw()	Checks if the board is full with no winner and announces a tie
button_click(index)	Handles a cell click: places the mark, checks win/draw, toggles turn
toggle_player()	Switches the active player and updates the turn label
Known Issues

The current script has a couple of leftover duplications worth cleaning up:

tk.Tk() is called twice (creating two root windows) — only the second root is actually used.
The buttons list is populated twice (once before root.mainloop() setup, once after), so buttons are created twice and the grid is built twice.

These don't necessarily crash the game, but they do create an extra unused window and duplicate widgets. Removing the first root = tk.Tk() block and the first button-creation loop (keeping only the second set) would clean this up.

License

Free to use, modify, and share.
