HTML Structure (What’s in the Page?)
🧩 1. <canvas id="gameCanvas">
This is the main game screen.

Everything that moves (player, enemies, background) will be drawn here using JavaScript.

It’s like the game’s "stage" or playing field.

html
Copy
Edit
<canvas id="gameCanvas" width="1000" height="600"></canvas>
🧑‍💻 2. <div class="ui"> – Player Status
Shows live game information (top-left of the screen):

❤️ Health

⚡ Mana (magic energy)

🏆 Score

🎯 Level

💰 Gold

This lets the player keep track of their current condition.

html
Copy
Edit
<div class="ui">
  <div>❤️ Health: <span id="health">100</span></div>
  ...
</div>
🛡️ 3. <div class="inventory"> – Items Player Has
Shows player’s equipment and items (top-right):

🗡️ Weapon (like sword or bow)

🛡️ Shield

🧪 Potions (health recovery)

html
Copy
Edit
<div class="inventory">
  <div>🗡️ Weapon: <span id="weapon">Sword</span></div>
  ...
</div>
🎮 4. <div class="controls"> – Game Controls
Explains how to play the game (bottom-left):

W / A / S / D or Arrow Keys – Move

Spacebar – Attack

Q – Use potion

E – Use magic

R – Restart the game

html
Copy
Edit
<div class="controls">
  <div>WASD/Arrow Keys: Move</div>
  ...
</div>
🆙 5. <div class="level-indicator" id="levelIndicator">
Used to show current level in big text like:
"LEVEL 2"

Hidden by default (display: none)

It’s shown temporarily when player levels up.

💀 6. <div class="game-over" id="gameOver">
Appears when the player loses (health becomes 0).

Shows:

“Game Over” message

Final Score

Level Reached

A button to “Play Again”

html
Copy
Edit
<div class="game-over" id="gameOver">
  <h2>Game Over!</h2>
  <p>Final Score: <span id="finalScore">0</span></p>
  ...
</div>
When the player clicks “Play Again”, the game restarts using:

js
Copy
Edit
onclick="restartGame()"
🎨 CSS Styling (Inside <style> tag)
✅ What It Does:
Sets background colors and gradients (sky, grass, soil)

Uses white, clean font (Courier New)

Adds shadows and borders for a polished look

Positions elements like health bar, inventory, etc. around the canvas

Hides certain elements until needed (display: none)

