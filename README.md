


https://github.com/alfredo1995/RandomBoard-Multiplayer/assets/71193893/96f954e3-30a4-4767-a9e6-54426db334b8

Requirements

    💡 A board game;

    💡 Board 5 x 5, 5 rows and 5 columns, 25 cells

    💡 Each cell with size of 1 x 1

    💡 Two players, each player represented by a pawn, one in white and the other in black;

    💡 The white pawn starts on the far right of the board, that is, on column 4;

    💡 The black pawn starts on the far left, i.e. on file 0;

    💡 The cell that each pawn must start in will be selected randomly within the specified column;

    💡 The objective is to reach the other side first, that is, white pawn on column 0 and black pawn on column 4;

    💡 Pedestrians cannot overlap or pass over each other;

    💡 The game is in turns, the player with the white pawn plays first and then the player with the black pawn;

    💡 Pedestrians can move to the right, left, forward or backward;

    💡 The player must draw lots to find out how many cells he can move, with a minimum of 0 and a maximum of 2;

    💡 When the first pawn arrives on the other side, a victory is added to the corresponding player and a new game begins;

    💡 5 matches will be played per challenge, the player who wins 3 matches wins the challenge;

    💡 There should be a menu screen, with the option to start the game and another to exit the game;

    💡 When clicking on match, a screen should appear for the player to enter a name and a button to enter the challenge;

    💡 The game HUD must have the name of the white pawn player in the right corner and the black pawn player in the left corner, both at the bottom;

    💡 Between the players' names there will be a button, which the player whose turn it is to play must click so that a number from 0 to 2 is drawn, this number will be the number of cells that the pawn can move;

    💡 In the central part of the HUD at the top there should be the number of matches that each player has won;

    💡 When a match is finished, a message should appear on the screen for those who won - "You won" - and a message for those who lost - "You lost";

    💡 At the end of the challenge, a message should appear - "Congratulations, You Won the Challenge" - for the player who won the challenge and a message - "Try Again" - for whoever lost;

Technical details

    💡 Multiplayer system: The game supports multiplayer matches between 2 players, with a central server that manages the game state and replicates information to clients.

    💡 GameState: The server maintains a GameState that represents the overall state of the game, including the position of the pieces on the board, the player's turn, and the score.

    💡 PlayerState: A PlayState was created to store important information about each player, such as name, color of pieces, and current state of the game.

    💡 Player management: The server updates the game state and replicates the information to all players

    💡 State replication: The server uses MultiCast to replicate PlayerState and GameState to all connected clients.

    💡 Game Events: Custom events used to communicate player actions between the client and server

