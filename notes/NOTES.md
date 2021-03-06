https://en.wikipedia.org/wiki/Tic-tac-toe

# Pomodoro 1
- ✅ Understand the problem area a bit
- ✅ Skim read the wikipedia
- ✅ Use the DDL in wikipedia to start thinking about tests
- ✅ Hook up the tests to _something_.

## Rough ideas of possible e2e test
- Tic-tac-toe is a paper-and-pencil game for two players, X and O, who take turns marking the spaces in a 3×3 grid.
- The player who succeeds in placing three of their marks in a horizontal, - vertical, or diagonal row is the winner.

- The first player is designated "X"
- The second player is designated "O"

- There are 3 possible 'end' states
- win - you've got got '3 in a row' (either horizontally or vertically)
lose - your opponent has got '3 in a row' (either horizontally or vertically)
- draw - a draw occurs when neither player has won, and there's no more available moves

when the games not in an end state, it can keep going!

## Possible unit tests
A player can play a perfect game of tic-tac-toe (to win or at least draw) if, each time it is their turn to play, they choose the first available move from the following list, as used in Newell and Simon's 1972 tic-tac-toe program.[16]

Win: If the player has two in a row, they can place a third to get three in a row.
Block: If the opponent has two in a row, the player must play the third themselves to block the opponent.
Fork: Create an opportunity where the player has two ways to win (two non-blocked lines of 2).
Blocking an opponent's fork: If there is only one possible fork for the opponent, the player should block it. Otherwise, the player should block all forks in any way that simultaneously allows them to create two in a row. Otherwise, the player should create a two in a row to force the opponent into defending, as long as it doesn't result in them creating a fork. For example, if "X" has two opposite corners and "O" has the center, "O" must not play a corner move in order to win. (Playing a corner move in this scenario creates a fork for "X" to win.)
Center: A player marks the center. (If it is the first move of the game, playing a corner move gives the second player more opportunities to make a mistake and may therefore be the better choice; however, it makes no difference between perfect players.)
Opposite corner: If the opponent is in the corner, the player plays the opposite corner.
Empty corner: The player plays in a corner square.
Empty side: The player plays in a middle square on any of the 4 sides.


# Pomodoro 2
- ✅ Advance a board
- ✅ Able to move one board at a time 

# Pomodoro 3
- ✅Able to detect a winner
- ✅Added all test cases

# Pomodoro 4
- ✅Able to retry random moves
- ✅Able to detect if no more moves
- ✅ Play until winner or no more moves


# Refactor
- ✅Should split the code a little more around the states
- ✅test make move
- ✅work out better print to screen
- ✅Use constants more

# NYI
- 🚧 Ensure test titles are perfect
- 🚧 Get 100% coverage, by setting the same value twice - and checking that the makeMove() function is called twice
- 🚧 We _could_ push board states to an array of all states ala event sourcing, and work out who's playing by the index and whether it's even or not
- 🚧 The flattening of the board doesn't make _too_ much sense if you're not aware of that being how you solve the problem - add a comment?
