# ♟️ Chess Bot

An interactive **Chess vs Computer** game developed in a Jupyter Notebook using **Python, HTML, CSS, and JavaScript**.

The project provides a browser-based chess interface with legal move validation, special chess rules, a chess clock, and a computer-controlled opponent.

---

## 🎯 Project Overview

This project implements a playable chess game where:

- The player controls the **White pieces**
- The computer controls the **Black pieces**
- Players can select pieces and make legal moves on an interactive chessboard
- The computer automatically responds with a move
- Chess rules such as check, checkmate, castling, en passant, and promotion are handled by the game logic

The complete interface is rendered inside a Jupyter Notebook using HTML and JavaScript.

---

## ✨ Features

### ♟️ Interactive Chessboard

- 8 × 8 interactive chessboard
- Click-based piece selection and movement
- Visual highlighting of:
  - Selected pieces
  - Legal moves
  - Capture moves

### 🤖 Computer Opponent

The computer automatically generates legal moves and scores them based on:

- Capturing valuable pieces
- Giving check
- Castling
- A small random component to vary move selection

The computer then selects the highest-scoring available move.

### ♜ Chess Rules

The project supports several important chess rules:

- Legal piece movement
- Piece capturing
- Check detection
- Checkmate detection
- Stalemate detection
- Castling
- En passant
- Pawn promotion

### ⏱️ Chess Clock

The game includes a **10-minute clock for each player**.

- White clock
- Computer clock
- Automatic countdown based on whose turn it is
- Game ends when a player's time reaches zero

### 👑 Pawn Promotion

When a pawn reaches the opposite end of the board, the player can choose:

- Queen
- Rook
- Bishop
- Knight

The computer automatically promotes to a queen.

### 🔄 Restart Game

A restart button is provided to reset:

- Board position
- Turn
- Castling rights
- En passant state
- Promotion state
- Chess clocks
- Game status

---

## 🛠️ Technologies Used

- **Python** – Jupyter Notebook integration
- **HTML** – Game interface and chessboard structure
- **CSS** – Chessboard and UI styling
- **JavaScript** – Game logic, move validation, computer moves, chess rules, and clock functionality
- **Jupyter Notebook** – Development and execution environment

---

## 🧠 Game Logic

The chess engine maintains the current board state and determines legal moves for each piece.

The project includes functions for:

- Generating pseudo-legal moves
- Checking whether a square is attacked
- Detecting check
- Generating legal moves
- Simulating moves
- Handling castling
- Handling en passant
- Handling promotion
- Detecting checkmate and stalemate

Before making a move, the game verifies that the move does not leave the player's king in check.

---

## 🤖 Computer Move Selection

The computer first generates all legal moves available to Black.

Each move receives a score based on several factors:

| Factor | Description |
|---|---|
| Capture | Gives a bonus based on the value of the captured piece |
| Check | Gives an additional bonus when the move puts the opponent in check |
| Castling | Gives a bonus for castling |
| Randomness | Adds a small random value to introduce variation |

Piece values used by the computer are:

| Piece | Value |
|---|---:|
| Pawn | 1 |
| Knight | 3 |
| Bishop | 3 |
| Rook | 5 |
| Queen | 9 |
| King | 100 |

The computer selects the highest-scoring legal move.

---

## 📁 Project Structure

```text
Chess-bot/
│
├── Chess.ipynb
└── README.md
