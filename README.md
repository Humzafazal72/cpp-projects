# cpp-projects
Semesters projects that i made using c++
Implementation:

•	Isvalid() function:

We pre-defined a board with some initial values and stored them in a 2D array. This two-dimensional array is the game board. So we defined the void Print_Board(int arr[9][9]) function to print the sudoku board on the console screen.
•	Checking for Number Repetition: 
Checking Columns: Additionally, according to the game’s requirements explained above, the game cannot allow the player to repeat any number in any row, column or square. Therefore, we checked the column number and the input number or value that if the number already exists in the specified column or not. After it has checked the column for repetitive values, it returns the Boolean variables based on its findings. 
Checking Rows: Similarly, the function matches the input number with every number in the specified row and returns true or false after verifying its presence.
Checking Small Squares:  Furthermore, another condition was required for checking the starting number of row and column of a specific square, and the user input to match it with the 3 by 3 square to check if the number exists in the entire square or not.
•	Placing Values in Boxes:
As all the above conditions need to be false, to place a number in a specific box, the function isvalid() takes the input and calls these above functions inside its body. It checks the output they return. For example, if all of them are false, it returns “true” to confirm that the user can write the input number in that box.
•	Soduku_Solver function:
This function is the heart of our code. It takes the row and column index as an argument along with the sudoku board. It then checks if all the cells have been filled then prints the board. If the given cell is already filled then it moved to the next cell recursively. Else if it is empty it fills it with a valid value using a for loop and isvalid () function. Then it recursively moves to the next cell. But if no value can be filled in a cell we backtrack to the previous cell.


•	The Driver Function:
In the main() function, the user is asked if he wants to input an sudoku puzzle. Then after he has entered the puzzle using the isvalidsudoku() we check if the sudoku enterd is valid or not. If valid, the sudoku puzzle is passed on to the sudokusolver() function. Else the user is prompted to enter the puzzle again.
ALTERNATIVE METHOD/ALGORITHM:
Brute force algorithm can also be used to solve the puzzle. In this algorithm we first determine all the possible combinations of the 81 cells. Then we chose the valid combination. This algorithm has relatively high time complexity (O(n!)) compared to backtracking.
