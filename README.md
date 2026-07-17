# Profile
# TIC-TAC-TOE

A classic two-player Tic Tac Toe game (X and O) built with Python, Tkinter for the GUI, and Pygame for sound effects.

## Features
- Two-player local gameplay (Player X vs Player O).
- Start screen to choose which player begins.
- Simple entry animation for moves.
- Win / draw detection with sound effects.
- Included sound assets for click, win, and draw.

## Files
- `game.py` — Main application. Implements the GUI, game logic, animations, and sound playback.
- `click.wav`, `win.wav`, `draw.wav` — Sound effects used by the game.
- `flowchart.png` — (optional) flow diagram of game logic / UI flow.

## Requirements
- Python 3.8+ recommended
- tkinter (usually included with standard Python distributions; on some Linux installs you may need to install `python3-tk`)
- pygame

## Installation (recommended)
Create and activate a virtual environment, then install dependencies:

```bash
# create & activate venv (Unix/macOS)
python3 -m venv .venv
source .venv/bin/activate

# Windows (PowerShell)
python -m venv .venv
.venv\Scripts\Activate.ps1
```

Then install pygame:

```bash
pip install pygame
```

On Debian/Ubuntu, if tkinter is missing:

```bash
sudo apt-get update
sudo apt-get install python3-tk
```

## Run the game
From the project root:

```bash
python game.py
```

The game window will open. Choose who starts (Player X or Player O), then click cells to play. Sounds will play for clicks, wins, and draws.

## How it works (brief)
- `TicTacToe` class (in `game.py`) builds a start screen, the 3x3 board, and manages state.
- Game flow:
  - Start screen → select starting player → board shown.
  - Players alternate clicking empty cells.
  - After each move the app checks for a win or draw.
  - On win/draw, shows a message box and resets to the start screen.
- Sound playback is handled via `pygame.mixer` (initialized at program start).

## Troubleshooting
- If you see an error initializing the audio mixer on headless servers, run without sound or ensure an audio device is available. On some systems you may need to set SDL_AUDIODRIVER or install additional packages.
- If tkinter windows do not appear, ensure your Python build includes tkinter (see installation above).

## Customization ideas
- Add AI to play against the computer (minimax).
- Add score keeping across rounds.
- Add a settings screen to mute sounds or change board size/appearance.
- Package as a standalone executable using PyInstaller.

## Contributing
Contributions are welcome. If you want to add features or fix issues:
1. Fork the repo.
2. Create a feature branch.
3. Open a pull request with a clear description of changes.

## License
If you’d like to make this repo public with a license, consider adding an `LICENSE` file (MIT is a common choice). This README does not include a license by default.

## Acknowledgements
- Built with Tkinter for GUI and Pygame for sound effects.
- Sound assets included in this repository.
