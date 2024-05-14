


https://github.com/alfredo1995/RandomBoard-Multiplayer/assets/71193893/96f954e3-30a4-4767-a9e6-54426db334b8

Meeting the Requirements
  
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

Project Architecture

![arquitetura-server-multiplayer-replicate-multicast](https://github.com/alfredo1995/multiplayer-server-replicate-multicast/assets/71193893/fd35c3f0-269d-4c0b-9d07-5dfbf45a5bde)

Technical details

    💡 GameMode: Defined as general game rules and behavior.
        Level: Responsible for creating the game's visual and sound scene
        PlayerControler: Responsible for the commands that the game character can understand and execute.

    💡 GameState: Storing and managing global game information that all players need access to during the match.
        Server: Managing the game rules, updating the state of the virtual world according to the players' actions.
        MultiCast: Allows the server to send a single message to multiple players simultaneously
        RepNotify : Synchronize the state of duplicated random variables between the server and clients

    💡 Widget: Creates the user interface (UI) elements that players interact with during gameplay.
        Logic: Build the scene, move the pieces, check the game conditions, call animations and other functions.

    💡 PlayState: Centralizes the data that needs to be shared and synchronized between the server and all connected clients.
        Request: Fulfill data requests related to player information for this multiplayer game.
        Replicate: Synchronizes data between the server and clients, ensuring all players have insight into each other's actions.


