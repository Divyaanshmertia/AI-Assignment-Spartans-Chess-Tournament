# Spartans Chess Tournament

A modified 4x8 chess game implementation with AI players. This project implements a unique variant of chess played on a 4x8 board with a subset of traditional chess pieces.

## Game Overview

This chess variant is played on a 4x8 board with the following pieces:
- Pawns (♟/♙)
- Knights (♞/♘)
- Bishops (♝/♗)
- Kings (♚/♔)

The game follows modified chess rules and includes features like:
- Bullet chess format (1-minute time control)
- Point-based scoring system
- AI player implementations
- Checkmate and stalemate detection

## Project Structure

- `board.py`: Core game engine implementation with move generation and validation
- `ai_player.py`: Base class for AI player implementations
- `game_runner.py`: Game execution and visualization
- `config.py`: Game constants and configuration

### Key Components

#### Game Engine (`board.py`)
- Move validation and generation
- Check/checkmate detection
- Board state management
- Position history tracking

#### AI Player Interface (`ai_player.py`)
Base class for AI implementations with required methods:
- `get_best_move()`: Calculate and return the best move
- `evaluate_board()`: Heuristic evaluation of board positions

#### Game Runner (`game_runner.py`)
- Game visualization with Unicode chess pieces
- Time management for bullet chess games
- Score tracking and game statistics
- Move logging and display

#### Configuration (`config.py`)
- Board dimensions (4x8)
- Piece definitions and values
- Position evaluation tables
- Unicode symbols for pieces

## Piece Values
```
Pawn: 20 points
Knight: 70 points
Bishop: 70 points
King: 300 points
```

## Scoring System
Points are awarded for:
- Capturing pieces (piece value)
- Giving check (+2 points)
- Checkmate (+300 points)

## Running the Game

To start a game between two AI players:

```python
python game_runner.py
```

The default configuration runs a 60-second bullet game between StandardPlayer and AggressivePlayer.

## AI Development

To create a new AI player:
1. Create a new class inheriting from `AIPlayer`
2. Implement `get_best_move()` and `evaluate_board()`
3. Set appropriate search depth

Example:
```python
class MyAIPlayer(AIPlayer):
    def __init__(self, board):
        super().__init__(board)
        self.depth = 1  # Set search depth

    def get_best_move(self):
        # Implement move selection logic
        pass

    def evaluate_board(self):
        # Implement board evaluation
        pass
```




## Contributing

We welcome contributions to improve the Spartans Chess Tournament! If you find any issues or have suggestions for improvements, please follow these steps to create an issue on GitHub:

1. Go to the [Issues page](https://github.com/Divyaanshmertia/AI-Assignment-Spartans-Chess-Tournament/issues)
2. Click on "New Issue"
3. Choose the appropriate issue template (if available) or create a blank issue
4. Provide the following information:
   - **Title**: A clear, concise description of the issue
   - **Description**: Detailed information about the issue, including:
     - What you were trying to do
     - What you expected to happen
     - What actually happened
     - Steps to reproduce the issue
   - **Environment** (if applicable):
     - Python version
     - Operating System
     - Any relevant dependencies
   - **Screenshots** (if applicable): Include any relevant visual evidence
   - **Additional Context**: Any other information that might be helpful

5. Submit the issue

### Best Practices for Issue Creation
- Search existing issues to avoid duplicates
- Use a clear and descriptive title
- Provide as much relevant information as possible
- Be specific about the problem
- Format code snippets using markdown code blocks
- Be respectful and follow the project's code of conduct

### Pull Requests
If you'd like to contribute code:
1. Fork the repository
2. Create a new branch for your feature
3. Make your changes
4. Submit a pull request with a clear description of the changes

For major changes, please open an issue first to discuss what you would like to change.
