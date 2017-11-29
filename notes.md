Bugs In Original Code:
* syntax was poor and unreadable (missing brackets and proper spacing)
* logic did not handle edges
* poor variable names
* 10 x 10 board was too small for flower pattern
* logic did not capture next generation
* logic did not handle when n was equal to 2

* Within NextStep:
  - n=3 should have been a comparison check not an assignment
  - inner loop did not increment var y


Working Code:
* Got rid of extra code and highlighted primary functionality (initializing a board, drawing a board, updating the board)
* Initialized Board as an empty array to clean up redundancy in original
  - made understandable variable names (ie, rows and cols)
* updateBoard:
  - explicitly checked for top left, top center, top right, middle left, middle right,
  bottom left, bottom center, bottom right cells
  - created neighbor count from true values
  - created a loop through the rows and inner loop for each individual cell in a row. While initializing result 2-d array.
  - result array captures the following generation and validating ruleset.
  - For any cell within the row, if it is greater than zero then ruleset will apply the following logic:
    - set variable alive equal to the return value from the ternary operator

* When user clicks on "Next ->" the script executes DrawBoard(result). Result being the next generation representation.
