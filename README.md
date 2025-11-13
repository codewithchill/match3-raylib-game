# **Raylib ASCII Match-3**

- **Project**: A small 2D match-3 game written with `raylib` in C.
- **Source**: `main.c`
- **Assets**: `assets/` (background image, font, music, and sound effects)

## **Description:**

- **Raylib ASCII Match-3** is a compact demo game that renders tiles as ASCII characters and implements basic match-3 mechanics: swap adjacent tiles, match three or more in a row/column, tiles fall and refill, score popups, and a simple score animation.

## **Files of interest:**

- `main.c`: game logic, rendering, input and audio calls.
- `assets/`: contains `bg-img.jpg`, `astroz.ttf`, `music.mp3`, `match-sound.mp3` (all required at runtime).

## **Build (Windows / MSYS2) - example:**

- Install MSYS2 and the UCRT toolchain, then install `raylib` and `gcc` (or use your preferred raylib setup).
- From a MSYS2 UCRT64 shell (or other environment where `raylib` is available), run:

```bash
gcc main.c -o game -LC:/msys64/ucrt64/lib -lraylib -lopengl32 -lgdi32 -lwinmm
```

- If you use a different toolchain or library path, update `-L` and library flags accordingly.

## **Run:**

- From the folder containing the `game` executable and the `assets/` directory, run:

```bash
./game    # or .\game.exe on Windows PowerShell
```

## **Controls:**

- Left mouse button: select a tile. Click an adjacent tile to swap. Matches of 3 or more will be cleared automatically.

## **Gameplay / Mechanics:**

- Board size: 8x8 tiles (see `BOARD_SIZE` in `main.c`).
- Tile types: 5 ASCII characters (see `tile_chars[]` in `main.c`).
- Matching: detects horizontal and vertical 3+ matches, awards score and spawns score popups, then resolves tile falls and refills the board.

## **Audio / Fonts:**

- The game loads `assets/astroz.ttf` for the score font and plays `assets/music.mp3` and `assets/match-sound.mp3`. Ensure these files exist in `assets/`.

## **Notes & Tips:**

- Run the game from the project root so relative asset paths (e.g., `assets/astroz.ttf`) resolve correctly.
- If you see issues with audio or fonts, verify your `raylib` audio backend and that `InitAudioDevice()` succeeds.

Enjoy experimenting with the match-3 mechanics and raylib rendering!

---
