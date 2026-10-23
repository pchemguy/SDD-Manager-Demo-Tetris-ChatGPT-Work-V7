# Browser Tetris

## Purpose and users

Create a small, playable single-player Tetris game for desktop browser users. The player arranges falling tetrominoes, clears complete rows and earns points until no new piece can enter the board, then can restart immediately.

## Intended experience

- A 10-column by 20-row visible board with the seven standard tetrominoes and visually distinct piece colors.
- Keyboard movement left and right, rotation and soft drop, with automatic gravity.
- Collision checks against the board boundaries and settled cells; pieces settle after a failed downward movement.
- Complete rows clear together, remaining cells fall into the cleared space and the score updates.
- A visible score, concise controls, clear game-over feedback and a restart control.
- Pause and resume without advancing game time while paused or while the page is hidden.

Use independent random piece selection, simple collision-checked rotation and a fixed gravity interval. Favor understandable, consistent behavior and responsive controls over a large ruleset.

## Delivery constraints and quality

The proposed implementation uses TypeScript, the HTML Canvas API for the board and standard HTML for controls and status. It runs entirely in the browser as a static application, without a backend or account. The playable board must remain legible, and game controls must not consume keystrokes while the player interacts with an ordinary page control.

Separate game rules from browser input and rendering so collision, rotation, row clearing, scoring and game-over behavior can be checked deterministically. Verify the playable application in Chromium as the primary target and Playwright-managed Firefox as the secondary target, using isolated headless environments governed by [BROWSER_DEV_POLICY.md](../../BROWSER_DEV_POLICY.md).

## Scope boundaries

Multiplayer, online leaderboards, accounts and mobile touch controls are outside the intended scope.
