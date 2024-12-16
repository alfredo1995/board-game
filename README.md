


https://github.com/user-attachments/assets/05e10503-99c5-452d-a45b-23c3e2cf2973


 
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

    💡 Steam Multiplayer: Responsible for connecting the game to the Steam platform, using the official Steam plugin.
         Steam Session: Implements the functionality of multiplayer sessions with Steam support, allowing players to:
         Steam Plugin: Ensures integration with Steam APIs for authentication, friend management, and other features.
         Server Browsing: Displays a list of available servers, with information about capacity, ping, and match status, to facilitate matchmaking.

        


