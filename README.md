# PROJECT: TIC-TAC-TOE-GAME

* *A simple 2 player TIC TAC TOE Game made with help of PYTHON.* 
* *You can play this game with your friend using command line interface to cherish your childhood memories.*
* *Happy Coding :)*

*😊😊😊 Show some :heart: by giving the repo a ⭐*

## 💠 CODE:

```
# Tic-Tac-Toe game in Python

board = [" " for x in range(9)]

def print_board():
    row1 = "| {} | {} | {} |".format(board[0], board[1], board[2])
    row2 = "| {} | {} | {} |".format(board[3], board[4], board[5])
    row3 = "| {} | {} | {} |".format(board[6], board[7], board[8])

    print()
    print(row1)
    print(row2)
    print(row3)
    print()

def player_move(icon):
    if icon == "X":
        number = 1
    elif icon == "O":
        number = 2

    print("Your turn player {}".format(number))

    choice = int(input("Enter your move (1-9): ").strip())
    if board[choice - 1] == " ":
        board[choice - 1] = icon
    else:
        print()
        print("That space is taken!")

def is_victory(icon):
    if (board[0] == icon and board[1] == icon and board[2] == icon) or \
       (board[3] == icon and board[4] == icon and board[5] == icon) or \
       (board[6] == icon and board[7] == icon and board[8] == icon) or \
       (board[0] == icon and board[3] == icon and board[6] == icon) or \
       (board[1] == icon and board[4] == icon and board[7] == icon) or \
       (board[2] == icon and board[5] == icon and board[8] == icon) or \
       (board[0] == icon and board[4] == icon and board[8] == icon) or \
       (board[2] == icon and board[4] == icon and board[6] == icon):
        return True
    else:
        return False

def is_draw():
    if " " not in board:
        return True
    else:
        return False

while True:
    print_board()
    player_move("X")
    print_board()
    if is_victory("X"):
        print("X wins! Congratulations!")
        break
    elif is_draw():
        print("It's a draw!")
        break
    player_move("O")
    if is_victory("O"):
        print_board()
        print("O wins! Congratulations!")
        break
    elif is_draw():
        print("It's a draw!")
        break      
```

## 💠 Explanation:

⭐ **print_board()** function as the name says just helps in printing the current tic-tac-toe board.

⭐ **player_move()** function is the most important function in this tic-tac-toe game. This function takes the position as input from the user and fills that position in the board with the symbol of that player.

⭐ **is_victory()** function just checks if any of the two players have won or not.

⭐ **is_draw()** function checks if the game is drawn or not.

⭐ And then comes our main while loop which keeps the game going.

⭐ This program will stop only when either one player has won or the game is drawn.

## 💠 Demo:

```

```

