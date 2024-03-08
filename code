board = [[' ' for i in range(3)] for j in range(3)]
current_player = 'X'

print("Хрестики-нулики")

for i in range(9):
    print('\n'.join([' | '.join(row) for row in board]))
    print("\nгравець", current_player, "ходить.")

    row = int(input("Введіть рядок (0, 1 або 2): "))
    column = int(input("Введіть стовпець (0, 1 або 2): "))

    if board[row][column] != ' ':
        print("Помилка. Спробуйте ще раз.")

    board[row][column] = current_player

    if (board[0][0] == board[1][1] == board[2][2] == current_player or
            board[0][2] == board[1][1] == board[2][0] == current_player or
            any(all(board[i][j] == current_player for j in range(3)) for i in range(3)) or
            any(all(board[i][j] == current_player for i in range(3)) for j in range(3))):
        print('\n'.join([' | '.join(row) for row in board]))
        print("Гравець", current_player, "переміг!")
        break

    current_player = 'O' if current_player == 'X' else 'X'

else:
    print('\n'.join([' | '.join(row) for row in board]))
    print("Нічия!")
