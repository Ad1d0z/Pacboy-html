# Pacboy (HTML)

A self-contained HTML/JavaScript port of [Pacboy](https://github.com/Ad1d0z/Pacboy),
the Pac-Man-style maze game originally built with Python + Pygame.

Everything lives in a single file — `pacboy.html`. No dependencies, no assets,
no build step: sound is synthesized with WebAudio and high scores persist in
the browser's `localStorage`. Just open it in a browser and play.

## Play

Open `pacboy.html` in any modern browser, or embed it in an HTML presentation:

```html
<iframe src="pacboy.html" width="600" height="690" style="border:0"></iframe>
```

Click the game once so it has keyboard focus (this also unlocks the sound).
While focused, the game swallows arrow-key presses so it won't advance your
slides mid-game.

## Controls

Keyboard:

- **Enter name:** type on the start screen, then **Enter**
- **Choose difficulty:** Up/Down (or W/S) to pick **Easy / Medium / Hard**, **Enter** to start;
  **Backspace** goes back to edit your name
- **Move:** Arrow keys or **W A S D**
- **Pause:** **P** or **Esc** (or the button in the top-right corner)
- **Play again** (after game over): **R**

Touch (phones/tablets):

- **Tap** to skip the intro; on the name screen a tap summons the on-screen
  keyboard (Go/Enter continues)
- **Tap a difficulty** to select it, tap it again to start; **"< BACK"**
  returns to name entry
- **Swipe** anywhere to steer — one continuous drag can steer through
  several turns
- **Tap the pause button** (top-right corner) to pause; tap anywhere to resume
- **Tap** the game-over screen to play again

## Gameplay

- Clear every coin to advance — an endless, escalating run of fresh mazes with
  faster enemy spawns each level. Score and lives carry over. There are ten
  maze layouts, each with its own wall colour theme, picked at random per level.
- Enemies come in four personalities (max **5** active): a **chaser** (red),
  an **ambusher** (pink) that cuts ahead of you, a **shy** one (orange) that
  retreats when you get close, and a **roamer** (cyan).
- **Teleporters** on the left and right edges warp you across the maze.
- **Cherries** near the corners (plus one by the ghost house on Easy) turn
  enemies blue and edible for a few seconds; eating ghosts in a row scores
  **200 → 400 → 800 → 1600**.
- +10 per coin, +50 per cherry. Your best runs are kept in a local
  high-score table.
