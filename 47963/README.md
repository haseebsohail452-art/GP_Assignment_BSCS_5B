                                                             Assignment #3
Name: Haseeb Sohail                                                                                                     SAP: 47963
                                                                  Game: Ludo Star
1. Game Overview
Ludo Star is a game based on maximum 4 players. This game allows 2 to 4 players to compete against each other over the internet. The 4 players will be randomly selected globally according to their requirements about the game. Each player contains 4 tokens and have to complete a round start from home and ending to home by protecting your own tokens from the other players. Player needs to roll a virtual dice to determine how many steps a token can move at a time.
This game provides features like online matchmaking, private room, chat functionality, offline game, real time synchronization. 
Main Features of the Game
1. Online Multiplayer gameplay
2. Player authentication and login
3. Real time dice rolling
4. Token movement on the board
5. Chat system
6. Winner determination and player statistics
3. High-Level Architecture
The architect of ludo star follows a client server model.
Client Side: The client application that runs on the player device is responsible for multiple things.
1.	Displaying the game board
2.	Showing token movement one place to another
3.	Receiving player input
4.	Displaying chat message for players communication with each other
5.	Communicationg with the server
Game Server: Prevents from cheating and maintain rule regulation.
1.	Matchmaking of players
2.	Game rules are correctly follow
3.	Dice validation
4.	Token Position update
5.	Winner determination

Database
The database stores:
1.	Player accounts
2.	Match history
3.	Player statistics
4.	Leaderboard information
Network Layer: Allows communication between the players.
4. Main Classes and Components
Player:
It will represent player in the game. This class have the movement of player and it’s information.
Responsibilities: 
1.	Store Player information
2.	Manage Tokens
3.	Track Game Progress
Token:
It represents the 4 tokens. These are the tokens with player play the game. 
Responsibilities: 
1.	Store token current position
2.	Handle Movements 
Dice Manager:
Controls the dice and generates a number.
Responsibilities: 
1.	Generate dice values
2.	Send result to player so the can move the token
Turn Manager:
Manages the players turn. If 2 players are playing then after one player completed his turn then 2nd player will play his turn.
Responsibilities: 
1.	Determine active player
2.	Switch turns after moves
Board Manager:
Manages the game board. Everything is working fine.
Responsibilities: 
1.	Track token location so the game will move to next part.
2.	Validate legal moves so no one can do cheating.
Game room:
Players meet each other for playing and also if it’s a team match then a player can join via code his teammate provides.
Responsibilities: 
1.	Store players information
2.	Maintain game state so everything works fine
Chat Manager:
Handles the communication between the players. So they can have fun by talking to each other while playing game.
Responsibilities: 
Sends and receives messages for players communication.
4. Design Decision:
The server is responsible for validating dice rolls, managing turns, and determining winners. This design prevents players from modifying game data and cheating. The client focuses mainly on displaying information and sending player actions to the server. Separating responsibilities into different classes improves maintainability, scalability, and code readability.

