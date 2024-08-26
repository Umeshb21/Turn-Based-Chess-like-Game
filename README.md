# Umesh_21BCE7320

Chess-Like Game 

Overview  

This project is a chess-like game played on a 5x5 grid between two players. Each player controls a team of five characters with specific movement rules: 

Pawn: Moves one block in any direction (Left, Right, Forward, Backward).

Hero1: Moves two blocks straight in any direction and kills any opponent's character in its path.

Hero2: Moves two blocks diagonally in any direction and kills any opponent's character in its path.

The game is implemented with a WebSocket server for real-time communication and a web-based client for user interaction.

Setup Instructions:

Server:

1.Install Dependencies:

Make sure you have Node.js installed. Navigate to the server directory and run:

npm install ws

2.Run the Server:

Start the server by running:

node server.js

The server will listen on port 8080.

Client:

1.Prepare the Client Files:

Ensure you have the index.html file ready in your project directory.

2.Open the Client

Open index.html in your web browser. You can simply double-click the file to open it in your default browser or use a local server if you prefer.

Usage:

1.Start the Server:

Run the server using the command mentioned in the setup instructions.

2.Open the Client:

Open index.html in two separate browser windows or tabs. Enter A or B as your player ID when prompted.

3.Deploy Characters:

When prompted in the browser, enter your characters in a comma-separated format (e.g., P1,H1,P2,P3,H2).

4.Play the Game:

Select a character by clicking on it in the grid.
Choose a move by clicking one of the move buttons.
The game alternates turns between players and updates the grid and move history in real-time.
