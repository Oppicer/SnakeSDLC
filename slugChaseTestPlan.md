# **Slug Chase Test Plan**

## **Part 1: Unit Testing the Game Mechanics**

### Description:
Unit testing ensures individual game components like movement, collision detection, and item collection work as expected.

### Actions:
- **Mechanics to Test**:
  - **Movement**: Can the slug move left, right, up, or down? Does the position update correctly?
  - **Trail Mechanics**: Does the slug leave a proper trail when it moves?
  - **Collision Detection**: Does the slug properly detect collisions with its trail or the boundaries of the play area?
  - **Item Collection**: Is the "poop" item collected when the slug intersects with it?

### Example Test Cases:

| **Test Case**                | **Test Data**           | **Expected Outcome**                                                                 |
|-------------------------------|-------------------------|-------------------------------------------------------------------------------------|
| Slug movement                 | Key presses: W, A, S, D | Slug moves up, left, down, and right respectively.                                 |
| Collision with trail          | Slug touches its trail  | Game ends with a "Game Over" screen.                                               |
| Collecting an item            | Slug intersects item    | Item disappears, and the trail extends.                                            |
| Boundary collision            | Slug moves off-screen   | Slug wraps around to the opposite side of the screen.                              |

---

## **Part 2: Logic Testing the Game Rules and Calculations**

### Description:
Logic tests verify the correctness of scoring, trail extension, and item respawn.

### Actions:
- **Mechanics to Test**:
  - **Score Calculation**: Does the score increase by the correct amount when an item is collected?
  - **Trail Growth**: Does the trail extend correctly when an item is collected?
  - **Item Respawn**: Is a new "poop" item respawned at a random valid location?

### Example Test Cases:

| **Test Case**                | **Test Data**             | **Expected Outcome**                                             |
|-------------------------------|---------------------------|-------------------------------------------------------------------|
| Score increment               | Item collected           | Score increases by +1 for each collected item.                   |
| Trail extension               | Item collected           | Trail extends by one segment for each collected item.            |
| Item respawn                  | Item collected           | New item spawns at a random, unoccupied location.                |

---

## **Part 3: Boundary Testing**

### Description:
Boundary testing examines extreme scenarios, such as maximum score or maximum trail length.

### Actions:
- **Mechanics to Test**:
  - **Maximum Score**: What happens when the score reaches its upper limit?
  - **Trail Length**: Does the game handle long trails without performance issues?
  - **Item Placement**: Does the game handle situations where no space is available for a new item?

### Example Test Cases:

| **Test Case**                | **Test Data**               | **Expected Outcome**                                             |
|-------------------------------|-----------------------------|-------------------------------------------------------------------|
| Maximum score                 | Score = 9999               | Score remains capped at 9999, decorated in a gold frame.         |
| Maximum trail length          | Entire play area occupied  | Game ends as no valid moves are possible.                        |
| Item respawn limit            | No space for items         | Game ends with a "No Space Available" message.                   |

---

## **Part 4: Integration Testing**

### Description:
Integration testing checks that different game components, such as movement, scoring, and collision, work together seamlessly.

### Actions:
- **Mechanics to Test**:
  - **Gameplay and Scoring**: Does collecting items correctly update the score and extend the trail?
  - **Movement and Collision**: Does slug movement interact correctly with the trail, items, and boundaries?

### Example Test Cases:

| **Test Case**                | **Test Data**             | **Expected Outcome**                                             |
|-------------------------------|---------------------------|-------------------------------------------------------------------|
| Scoring after collection      | Item collected           | Score updates and trail grows simultaneously.                    |
| Movement and boundary wrap    | Slug moves off edge       | Slug reappears on the opposite edge of the screen.               |
| Collision with trail          | Slug intersects trail     | Game ends and displays a "Game Over" screen.                     |

---

## **Part 5: Handling Bad Input and Run-Time Errors**

### Description:
These tests ensure that invalid inputs or unexpected game states are handled gracefully without crashing.

### Actions:
- **Mechanics to Test**:
  - **Invalid Input**: Does the game ignore unassigned key presses?
  - **Unexpected States**: Does the game handle corrupted save data or invalid item placement?

### Example Test Cases:

| **Test Case**                | **Test Data**             | **Expected Outcome**                                             |
|-------------------------------|---------------------------|-------------------------------------------------------------------|
| Invalid key presses           | Press Q or Z             | Game ignores input without crashing.                             |
| Corrupted save file           | Invalid save data        | Game notifies the player and allows them to start a new game.    |
| Infinite loop prevention      | Slug occupies all space  | Game detects the state and ends with a message.                  |

---

## **Part 6: Summary Test Table**

| **Test Case**                | **Test Data**               | **Expected Outcome**                                             |
|-------------------------------|-----------------------------|-------------------------------------------------------------------|
| Movement                     | Keys W, A, S, D            | Slug moves in the correct direction.                             |
| Collision with trail          | Slug intersects trail      | Game ends with "Game Over."                                      |
| Collecting items              | Slug touches item          | Score +1, trail grows, and new item spawns.                      |
| Maximum score                 | Score reaches 9999         | Score caps at 9999 with visual indicator.                        |
| Invalid input                 | Press Q or Z               | Input ignored without affecting gameplay.                        |
| Integration of scoring        | Collecting item            | Score updates and trail grows simultaneously.                    |
| Boundary wrap                 | Slug moves off-screen      | Slug reappears on the opposite side.                             |

---
