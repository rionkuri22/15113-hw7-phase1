# 🔥💧 Fireboy & Watergirl

> **Course Project:** 15-113 | Carnegie Mellon University (CMU)  
> **Challenge Format:** 45-Minute In-Class Coding Challenge + Code Handoff  
> **Author:** Rion Kurihara  

---

## 📌 Project Overview

This project was built as part of an in-class exercise at **Carnegie Mellon University**. 

We were to recreate the classic two-player puzzle-platformer **Fireboy & Watergirl** as a way to practice **rapid prototyping** under strict time constraints (~45 minutes), and preparing code for an effective handoff so a peer developer could seamlessly read, understand, and build upon another person's codebase.

---

## 🎮 Game Rules & How to Play

### 🎯 Objective
Both characters must navigate elemental hazards, solve co-op puzzles, and reach their designated exit doors (**F** for Fireboy, **W** for Watergirl) at the top of the temple.

### 🕹️ Controls

| Action | Fireboy (Red) | Watergirl (Blue) |
| :--- | :--- | :--- |
| **Move Left** | `Left Arrow` | `A` |
| **Move Right** | `Right Arrow` | `D` |
| **Jump** | `Up Arrow` | `W` |

### 🏆 Win & Loss Conditions
* **Victory:** Both characters successfully reach their respective doors alive.
* **Game Over:** If either character touches an opposing element or green ooze, they die instantly and the level fails.
* **Rank System:** Final grade (**A / B / C**) calculated based on completion speed and total gems collected.

---

## ✨ Key Features & Mechanics

### 1. 🌋 Elemental Immunities & Hazards
* **🔥 Fireboy:** Can walk safely through lava pools (`#ff3b3b`), but dies instantly upon touching water.
* **💧 Watergirl:** Can walk safely through water pools (`#3b82f6`), but dies instantly upon touching lava.
* **☣️ Toxic Green Ooze:** Deadly pit (`#00ff2a`) that kills both characters on contact.

### 2. ⚙️ Interactive Co-op Puzzle Mechanisms
* **Buttons:** Weight-sensitive pads that stay activated only while a player stands on them.
* **Levers:** Interactive switches that toggle and stay locked once flipped by a player.
* **Gates & Lifts:** Dynamic map obstacles connected to buttons and levers via `linkId`.

### 3. 💎 Collectible Gems
* Red gems can only be collected by Fireboy; Blue gems can only be collected by Watergirl. Collecting all gems is required to earn an **A-rank**.

---

## 🛠️ Code Architecture

```
15113-hw7/
├── index.html                   # HTML structure, Canvas element, HUD overlay & script imports
├── style.css                    # Game container, screen overlays & typography styling
└── js/                          # Modularized game engine logic
    ├── input.js                 # Key event listeners (WASD & Arrows) & input state tracking
    ├── physics.js               # AABB bounding box collision resolution & gravity dynamics
    ├── level.js                 # Level dataset (walls, pools, doors) & canvas level rendering
    ├── entities.js              # OOP class hierarchy (Player, Pool, Door, Button, Lever, Gate, Lift, Gem)
    └── main.js                  # Central controller (60 FPS loop, state machine, timer & win/loss logic)
```

---

## 🚀 How to Run

### Prerequisites
Make sure Python 3 is installed on your system to run a local web server.

### Launching the Game
1. Open a terminal in the project root directory:
   ```bash
   cd /Users/rion/Desktop/Github/15113-hw7
   ```

2. Start a local HTTP server:
   ```bash
   python3 -m http.server 8000
   ```

3. Visit the game in your web browser:
   ```text
   http://localhost:8000
   ```

---

## 📝 Remaining Handoff Tasks & Backlog

Because this prototype was developed under a 45-minute sprint, the following items remain open for the next contributor:

* [ ] Fix alignment/positioning of floating map elements.
* [ ] Adjust platform heights to match maximum jump trajectory.
* [ ] Relocate instructional text overlay to a cleaner location.
* [ ] Ensure all platform paths seamlessly connect and lead to the exit doors.
