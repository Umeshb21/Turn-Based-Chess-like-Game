# Umesh_21BCE7320

---

# Turn-Based Chess-like Game

## Table of Contents
- [Introduction](#introduction)
- [Features](#features)
- [Gameplay](#gameplay)
- [Installation](#installation)
- [Usage](#usage)
- [Technical Details](#technical-details)

## Introduction
This project is a web-based turn-based chess-like game where two players compete on a 5x5 grid. Each player controls a set of characters with unique movement capabilities. The objective is to eliminate all of the opponent's characters.

## Features
- **Real-time gameplay** using WebSockets.
- **Three unique character types** with different movement and combat rules:
  - **Pawn**: Moves one block in any direction.
  - **Hero1**: Moves two blocks straight in any direction and can eliminate opponents in its path.
  - **Hero2**: Moves two blocks diagonally in any direction and can eliminate opponents in its path.
- **Responsive web client** that displays the game board, character positions, and valid moves.
- **Turn-based gameplay** with alternating player turns.
- **Game over condition** when all characters of one player are eliminated.

## Gameplay

### Characters and Movement
- **Pawn**:
  - Moves one block in any direction (Left, Right, Forward, or Backward).
  - Move commands: `L` (Left), `R` (Right), `F` (Forward), `B` (Backward)
- **Hero1**:
  - Moves two blocks straight in any direction.
  - Kills any opponent's character in its path.
  - Move commands: `L` (Left), `R` (Right), `F` (Forward), `B` (Backward)
- **Hero2**:
  - Moves two blocks diagonally in any direction.
  - Kills any opponent's character in its path.
  - Move commands: `FL` (Forward-Left), `FR` (Forward-Right), `BL` (Backward-Left), `BR` (Backward-Right)

### Move Command Format
- For Pawn and Hero1: `<character_name>:<move>` (e.g., `P1:L`, `H1:F`)
- For Hero2: `<character_name>:<move>` (e.g., `H2:FL`, `H2:BR`)

### Winning the Game
- The game ends when one player eliminates all of their opponent's characters.

## Installation
1. **Clone the repository:**
   ```bash
   git clone https://github.com/Umeshb21/Umesh_21BCE7320.git
   cd Umesh_21BCE7320
   ```

2. **Install dependencies for the server:**
   ```bash
   npm install
   ```

3. **Start the WebSocket server:**
   ```bash
   node server.js
   ```

4. **Open the web client:**
   - Open `index.html` in a web browser.

## Usage

1. **Start the server:**
   ```bash
   node server.js
   ```

2. **Launch the game:**
   - Open `index.html` in two different web browsers or browser tabs.

3. **Initialize the game:**
   - Enter your player ID (`A` or `B`) and configure your characters.

4. **Play the game:**
   - Select a character by clicking on it, then use the buttons to move it.

5. **Winning the game:**
   - The game ends when one player eliminates all of the opponent's characters.

## Technical Details
- **Server:** Node.js with WebSocket for real-time communication.
- **Client:** HTML, CSS, and JavaScript for the web interface.
- **Game Logic:** Includes character movement, attack mechanics, and win condition checks.
- **Communication:** WebSocket events for game initialization, player moves, game state updates, and invalid move notifications.
