## Maze Drawing and Bomb Defusal Game

### Project Overview
This project is a game written in **Assembly language** using the **emu8086** emulator. The game challenges players to navigate through a maze and reach the final goal without triggering a bomb. It includes instructions, a counter for remaining moves, and success or failure messages based on the player's performance.

---

### Game Features
1. **Maze Drawing:**
   - The maze is represented using a 2D array where `1` represents walls, and `0` represents open paths. 
   - The maze is displayed row by row on the screen using character-based graphics.

2. **Game Instructions:**
   - The game displays the remaining number of moves using the `MOVES LEFT` message.
   - Instructions are shown at the start, and end-of-game notifications appear when the mission is completed or failed.

3. **End of Game Messages:**
   - If the player successfully completes the maze, a congratulatory message appears:  
     **"CONGRATS MISSION COMPLETE BOMB HAS BEEN DEFUSED."**
   - If the player runs out of moves before reaching the goal, a failure message is displayed:  
     **"MISSION FAILED BOMB HAS BEEN BLASTED."**

4. **Dynamic Maze Rendering:**
   - The maze is rendered using loops, with special characters for walls (`█`) and open paths (` `).

---

### Code Explanation
1. **Data Initialization:**
   - The maze is defined using arrays for each row (`maz1`, `maz2`, ..., `maz20`), with `1` representing walls and `0` representing open paths.
   - Text messages like success, failure, and remaining moves are stored in memory.

2. **Maze Printing:**
   - The code uses `lea si, mazX` to load the address of the current row of the maze.
   - A loop iterates through each element in the row, checking if it’s a wall or a path, and prints the appropriate character.

3. **Game State Management:**
   - Conditions compare paths (`0`) and walls (`1`) to determine valid moves for the player.
   - The number of remaining moves is decremented and displayed on the screen with the `MOVES LEFT` message.

4. **Game Completion:**
   - Conditional checks determine if the mission is complete or if the player has run out of moves.
