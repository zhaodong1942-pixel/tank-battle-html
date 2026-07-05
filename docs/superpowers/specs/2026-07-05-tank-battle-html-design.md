# HTML Tank Battle Design

## Goal

Build a small browser-playable tank battle game and publish it as a public GitHub repository named `tank-battle-html`.

## Assumptions

- The game should run by opening `index.html` directly, with no build step and no external dependencies.
- The first version should be compact and playable rather than a full clone of Battle City.
- The repository should be public unless the user later requests otherwise.

## Game Scope

- Player controls a tank with arrow keys or WASD.
- Space fires a bullet in the current facing direction.
- Enemy tanks move automatically, change direction when blocked, and fire occasionally.
- Brick walls block movement and are destroyed by bullets.
- Steel walls block movement and bullets without being destroyed.
- The player wins after all enemies are destroyed.
- The player loses when lives reach zero.
- A restart button starts a fresh game.

## Interface

The page contains a compact header with title, score, lives, enemy count, game status, and a restart button. The main area is a Canvas board with a dark arcade look and clear tank, wall, and bullet shapes.

## Architecture

The implementation uses one `index.html` file containing HTML, CSS, and JavaScript. The JavaScript keeps the game state in plain objects and arrays: map tiles, tanks, bullets, input state, score, and status. A single animation loop updates movement, collisions, enemy behavior, bullets, win/loss checks, and rendering.

## Verification

- Open the page locally and confirm the game renders.
- Confirm controls move the player and fire bullets.
- Confirm enemies can be destroyed, bricks can be destroyed, steel remains, and win/loss status appears.
- Commit the project and push it to a new public GitHub repository.
