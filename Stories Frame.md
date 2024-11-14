### **User Story 1: Player Starts the Game**

**As a player,**  
I want to start a new game by pressing a "Start" button,  
So that I can begin playing and enjoy the game.

**Acceptance Criteria:**

* The player must be able to click a visible "Start Game" button.  
* Upon clicking, the game must transition from the main menu to the gameplay screen without delay.

---

### **User Story 2: Player Controls the Slug**

**As a player,**  
I want to control the movement of the slug using arrow keys,  
So that I can navigate it through the game environment effectively.

**Acceptance Criteria:**

* The slug's direction should change in response to arrow key inputs, allowing movement up, down, left, and right.  
* If the slug collides with the wall or itself, the game should end, displaying a "Game Over" message.

---

### **User Story 3: Slug Eats Food and Grows**

**As a player,**  
I want the slug to grow longer each time it eats food,  
So that the gameplay becomes more challenging as it takes up more space on the screen.

**Acceptance Criteria:**

* The slug's length should increase by one unit every time it reaches and "eats" a piece of food.  
* A new piece of food should randomly appear on the game grid immediately after the slug eats one.

---

### **User Story 4: Slug Leaves Slime Trail**

**As a player,**  
I want the slug to leave a visible slime trail that increases as it eats more,  
So that the game has an interesting visual effect and I can track my progress.

**Acceptance Criteria:**

* A slime trail should appear behind the slug as it moves, starting small and expanding as the slug eats food.  
* The slime trail should fade gradually to avoid cluttering the screen and reduce as the slug grows longer.

---

### **User Story 5: Player Tracks Score**

**As a player,**  
I want to see my score increase each time the slug eats food,  
So that I can track my progress and aim for a high score.

**Acceptance Criteria:**

* The score should increase by a set amount (e.g., \+10 points) every time the slug eats a piece of food.  
* The current score should be visible at all times on the gameplay screen and should reset to zero when a new game begins.

