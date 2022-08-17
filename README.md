Objective:
The aim of this project is to design a 2-D Sudoku Solver Game using OpenGL

Rules to solve Sudoku:
Every row, column, and the square box should have all numbers between 1 to 9. 
No number should be repeated in any row, column, and square.

Methodology:
Create a struct named ‘Cell’ which will represent the cells in the Sudoku grid.
Sudoku Model
Declare an array of struct ‘Cell` of size 81 (9 x 9)
Create a valid board by filling in all the cells in such a way that all the rows, columns and boxes have digits from 1 to 9 without repetition.
Now, create the Sudoku puzzle by hiding some cell numbers such that a unique solution always exists from the new configuration formed after hiding some digits.
Check_validity function:
Checks if a number is present in the corresponding row, column and box. Used to fill in while solving.
5. NoUniqueSolution function:
Recursive function to check if current puzzle has a unique solution or not.
6. Print_board function:
Used to print the board on screen.
7. Find_unassigned_cell function:
Used to find any empty cell in the board
C. Sudoku Controller
This class contains functions for controlling the different stages of Sudoku solving and maintaining error lists as well as checking errors while solving.
1. ErrorList:
A member variable of type vector<int> to store list of cell positions which contain incorrect numbers (either row-wise, column-wise or box-wise)
2. CheckforErrors:
A function which is used to find out errors in the board such as duplicates in row, column and/or box.
3. CheckRowColBoxErrors:
A function which contains the logic for checking duplicates in row, column and box.
4. CheckExistingErrorCells:
A function to check if the existing errored cells are cleared or not.
5. SingleCellErrors:
D. Sudoku View
This class contains methods which control the view of the Sudoku grid and input features
reshape:
Function to resize the viewport and projection matrix according to input width and height. Called by GLUT.
2. display:
Displays the Sudoku grid as well as timer along with filled in cell numbers. Called by GLUT.
3. keyboard:
Sets number in selection box according to the input given by user.
4. specialkeys:
Let's user move the selection box using arrow keys.
5. mouseclick: 
Let's user select a particular cell using mouse. And deselect any cell if clicked outside sudoku.
Sudoku Code : 
/*
SUDOKU GAME USING OPENGL and MVC Design Pattern
To run this game, type make and then type ./Sudoku
A window will be launched. You can use the mouse or
the keyboard to select the box and enter the number.


Conclusion:
In this project, we have used  the OpenGL library to design a 2-D grid and write numbers in the cell. Then we wrote an efficient algorithm to check the correctness of solved sudoku.
