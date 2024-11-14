**Requirements Specification: Slug Chase**

**Game Name:** Slug Chase  
**Team Members:** Kaden Williams, Brayden Teachout  
**Client:** Mrs. Kennedy  
**Date:** 11/14/2024

---

### **Game Overview**

* **Brief Description:** In *Slug Chase*, players control a slug as it slithers around the screen, consuming food items and leaving behind a slimy trail. As the slug eats, its slime trail grows, making the game increasingly challenging. Players must avoid colliding with the slug’s own trail or other obstacles.  
* **Main Goal:** The goal is to keep the slug moving, consume as much food as possible, and avoid collisions with the slime trail or obstacles, all while achieving the highest score possible.

---

### **Functional Requirements**

#### **Core Features**

1. **Slug Movement and Controls**  
   * **Directional Control:** Control the slug’s movement using arrow keys or WASD, similar to the classic *Snake* game.  
   * **Continuous Movement:** The slug continues moving in its current direction until redirected.  
   * **Boundary Option:** Decide if collisions with screen boundaries will end the game or allow screen-wrapping for added flexibility.  
2. **Food Collection**  
   * **Random Food Spawns:** Food appears randomly; players guide the slug to consume it.  
   * **Slime Growth:** Each food item lengthens the slime trail, increasing navigation difficulty.  
   * **Scoring:** Points are awarded for each food collected, with possible bonuses for speedier collection.  
3. **Slime Trail Mechanics**  
   * **Trail Persistence:** The slug’s trail grows with each food item eaten.  
   * **Collision Detection:** The game ends if the slug collides with its trail.  
   * **Trail Decay (Optional):** The slime trail can fade over time, providing an additional gameplay element.  
4. **Difficulty Progression**  
   * **Increasing Speed:** The slug’s speed may increase with food consumption.  
   * **Obstacle Introduction:** Higher levels introduce new obstacles for added challenge.  
   * **Complex Layouts:** Progressive levels may add tighter spaces and obstacles.  
5. **Power-Ups (Optional)**  
   * **Temporary Immunity:** Allows the slug to cross its own trail without penalty.  
   * **Shrink Trail:** Temporarily reduces the trail length.  
   * **Speed Boost:** Adds a burst of speed or slows down gameplay for easier navigation.  
6. **Game Over Conditions**  
   * **Self-Collision:** The game ends if the slug crosses its own slime trail.  
   * **Obstacle Collision:** Colliding with obstacles results in game over.  
   * **Boundary Collision:** Optionally, boundary collisions end the game unless wrap-around is enabled.  
7. **Score Tracking and Leaderboard (Optional)**  
   * **Real-Time Score Display:** Show the player’s current score on-screen.  
   * **High Score Leaderboard:** Records top scores for competitive play.  
8. **Visual and Sound Effects**  
   * **Slime Animation:** A semi-transparent trail grows thicker as the slug eats.  
   * **Sound Effects:** “Slurp” sounds for eating food and distinct sounds for collisions.  
   * **Background Music:** Immersive music complements the game’s theme.

---

### **Non-Functional Requirements**

#### **Usability**

* **Intuitive Controls:** Simple and intuitive control options (keyboard or touch screen).  
* **Clear Interface:** Display essential game information without overcrowding.  
* **Visual Feedback:** Quick, clear responses to player actions, such as effects when food is consumed.  
* **Onboarding and Help:** A brief tutorial introduces game mechanics and controls.

#### **Performance**

* **Smooth Gameplay:** Target 30-60 FPS for a smooth experience.  
* **Quick Load Times:** Aim for a load time of 2-3 seconds.  
* **Responsive Input:** Instant response to inputs for precise control.  
* **Resource Efficiency:** Optimize for minimal resource use, especially on mobile.

#### **Cross-Platform Compatibility**

* **Device Compatibility:** Playable on PC, mobile, and tablets with adaptable controls and screen scaling.  
* **Browser Compatibility (Optional):** Consider a web version using HTML5/JavaScript.

---

### **Design Requirements**

#### **Main Screen**

* **Start Button:** Prominent start button.  
* **Options:** Access settings, controls, and instructions.  
* **Leaderboard:** Optional high-score display.  
* **Theme:** Nature-inspired background, like a forest floor, to match the slug’s habitat.

#### **In-Game HUD**

* **Score Display:** Current score is clearly visible.  
* **Level Indicator:** Shows the level if the game has multiple stages.  
* **Pause/Exit:** Easy access to pause and return to the main menu.

#### **End Screen**

* **Score Summary:** Shows the player’s score with options to replay or return to the menu.  
* **Game Over Animation:** Simple animation or effect to signify game over.

#### **Game World and Visual Design**

* **Slug and Slime Trail:** An animated slug character and semi-transparent slime trail that grows as the game progresses.  
* **Food Design:** Small collectible items like berries or leaves.  
* **Obstacles and Levels:** Natural elements such as rocks and branches as obstacles in later levels.

#### **Audio Design**

* **Background Music:** Ambient nature sounds or light music to match the theme.  
* **Sound Effects:** Unique sounds for eating, collisions, and game over events.

---

### **Gameplay Mechanics Design**

1. **Slug Movement:**  
   * Smooth directional changes with gradual speed increases.  
2. **Slime Trail Growth:**  
   * Extends with each food item and has collision detection for self-contact.  
3. **Power-Ups (Optional):**  
   * **Temporary Effects:** Special abilities that briefly modify gameplay for a strategic advantage.

---

### **Data Requirements**

1. **Player Data**  
   * **Score:** Tracks food collected, resets on restart.  
   * **High Score:** Stores top score for future comparison.  
2. **Game Objects**  
   * **Slug Position and Movement:** Track position and direction in the game world.  
   * **Slime Trail:** Store trail segments and track its length.  
   * **Food Objects:** Randomly spawn food for the slug to collect.  
   * **Obstacles:** Position and type (if any) of obstacles in higher levels.  
   * **Power-Ups (Optional):** Randomly appearing items with effects on gameplay.  
3. **Game Settings**  
   * **Difficulty Level:** Adjusts speed and obstacle frequency.  
   * **Speed:** Controls the slug’s movement speed.  
   * **Grid Size/Resolution:** Defines game world boundaries.  
4. **UI and Audio Data**  
   * **Sound Settings:** Volume levels for background music and effects.  
   * **Visual Effects Settings:** Adjust trail opacity or other visuals.

---

### **Collaboration with Client**

#### **Feedback and Iteration**

* **Regular Playtesting:** Frequent sessions at the end of each sprint for the client to provide feedback.  
* **Direct Meetings:** Brief meetings for alignment on progress, questions, and next steps.

#### **Development Alignment**

* **Clear Sprint Goals:** Each sprint is planned with specific client-aligned goals.  
* **Prototypes:** Early mockups and prototypes for key features.  
* **Feedback Documentation:** Feedback logs for consistent, organized adjustments.

