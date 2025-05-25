
---

# 🤖 Beep Boop Bot (B3)

![Beep Boop Bot logo](optional-logo.png)
**Beep Boop Bot** is a mobile-friendly, single-page educational game that teaches **fundamentals of coding and logical thinking** through interactive gameplay designed for **middle schoolers**.

🎮 **Play Now**: [beepboopbot.surge.sh](http://beepboopbot.surge.sh)

---

## 🚀 Hackathon Theme Alignment

**Challenge Track**: STEM + Coding for Kids
**Target Audience**: Middle school students
**Learning Outcome**: Teaches sequencing, conditionals, and logic through a gamified robot navigation puzzle.

---

## 📚 Storyline

> “B3, the curious robot, is trapped on a mysterious spaceship. Use your coding skills to queue commands, jump obstacles, and help B3 escape safely!”

---

## 🧠 Learning Objectives

* Logical reasoning via sequential command execution
* Basic coding concepts (forward motion, loops, conditional thinking)
* Debugging and trial-error testing
* Visual spatial problem-solving

---

## 🧩 Gameplay Mechanics

* Grid-based 5x5 puzzle board
* Robot (B3) executes user-defined command queue
* Commands include:

  * `Move Forward`
  * `Rotate Left`
  * `Rotate Right`
  * `Jump` (over obstacles)
* Cannot move off-grid
* GO / STOP / CLEAR controls
* Level selector with increasing difficulty

---

## 🧱 MVP Features

* Mobile-first responsive layout
* Level system with multiple boards
* Two-panel UI (Command Input + Game Area)
* Queue-based command execution
* B3 returns to start on failure or Stop
* Pop-up feedback for win/loss
* Instructions page and backstory

---

## ⚛️ Tech Stack

* **React.js**
* **Redux**
* **GreenSock (GSAP)** for animations
* **HTML/CSS** (Flex/Grid)
* **Deployed via** Surge

---

## 🔁 React Component Structure

* `App`
* `Nav` (Level selector)
* `CommandPane` (Add, remove, clear commands)
* `CommandQueue` (Current command list)
* `GoStopButton` (Run/Stop/Retry)
* `Board` (5x5 interactive grid)
* `About` (Instructions + Story)

---

## 🕹️ User Stories

* View instructions/backstory at any time
* Choose and switch levels
* Add/remove commands before running
* Click 'Go' to execute queue
* See feedback on win/loss
* Retry failed attempts
* Clear queue anytime
* Only editable when robot is idle

---

## 🧠 Data Models

### B3 Robot State:

```js
robot = {
  direction: 0 | 90 | 180 | 270, // North, East, South, West
  positionX: 0-4,
  positionY: 0-4,
  isOnBox: Boolean
}
```

### Game Board:

```js
[
  [0,0,2,0,0],
  [0,0,0,0,0],
  [0,2,0,0,0],
  [0,0,0,0,0],
  [0,0,0,2,1] // 1 = Exit, 2 = Box
]
```

### Levels:

Levels are stored in an object:

```js
levels = {
  1: [...],
  2: [...],
  // ...
}
```

---

## 🎮 Redux Actions

| Action          | Description                  |
| --------------- | ---------------------------- |
| `GO_BUTTON`     | Start executing commands     |
| `STOP_BUTTON`   | Reset B3 to start            |
| `MOVE_FORWARD`  | Move 1 step forward          |
| `TURN_LEFT`     | Rotate 90° counter-clockwise |
| `TURN_RIGHT`    | Rotate 90° clockwise         |
| `JUMP_UP`       | Jump onto a box              |
| `QUEUE_ACTION`  | Add to queue                 |
| `CLEAR_QUEUE`   | Remove all queued commands   |
| `REMOVE_ACTION` | Delete one command           |
| `LEVEL_WON`     | Set game state to "won"      |
| `HAS_FINISHED`  | Mark end of queue execution  |




---

## 🌈 Future Features

* Loops & Conditional Logic (intro to real programming)
* Custom level builder for teachers
* Sound effects and robot personality!

