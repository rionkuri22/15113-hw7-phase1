# 🔥💧 Fireboy & Watergirl — Speed Coding Challenge

> **Course Project:** 15-113 | Carnegie Mellon University (CMU)  
> **Challenge Format:** 45-Minute In-class Coding Challenge + Code Handoff  

---

## 📌 Project Overview & Context

This project was built as part of an in-class exercise at **Carnegie Mellon University**. 

We were to recreate the classic two-player puzzle-platformer **Fireboy & Watergirl** as a way to practice **rapid prototyping** under strict time constraints (~45 minutes), and preparing code for an effective handoff so a peer developer could seamlessly read, understand, and build upon another person's codebase.

---

## 🚀 How to Run & Test the Game

1. **Open a terminal** in the project root directory:
   ```bash
   cd /Users/rion/Desktop/Github/15113-hw7
   ```

2. **Start a local HTTP server** using Python:
   ```bash
   python3 -m http.server 8000
   ```

3. **Open your browser** and navigate to:
   ```text
   http://localhost:8000
   ```

---

## 🎮 Game Vision & Mechanics

### Core Concept
A two-player maze game. Each character has distinct elemental traits and must work together to complete the level.

* **🔥 Fireboy:** Immune to lava/fire pools, but dies instantly upon touching water.
* **💧 Watergirl:** Immune to water/ice pools, but dies instantly upon touching lava.
* **☣️ Toxic Green Ooze:** Deadly to both characters upon contact.

### 🕹️ Controls

| Character | Left | Right | Jump |
| :--- | :--- | :--- | :--- |
| **Fireboy** | `Left Arrow` | `Right Arrow` | `Up Arrow` |
| **Watergirl** | `A` | `D` | `W` |

### 🎯 Win & Loss Conditions
* **Goal:** Both characters must navigate hazards, solve puzzles, and reach their designated exit doors (**F** for Fireboy, **W** for Watergirl).
* **Failure:** If either character dies, the level immediately fails and must be restarted.
* **Scoring Factors:**
  * Survival of both characters.
  * Number of gems collected (Red gems for Fireboy, Blue gems for Watergirl).
  * Completion speed (tracked by timer at the top center).

---

## 🧩 Key Features & Puzzle Elements

* **Levers & Buttons:** Require co-op coordination. Buttons must be held down continuously to keep doors open, whereas levers stay locked in place once flipped.
* **Moving Platforms & Pulleys:** Platforms configured so one player's weight lowers or raises paths for their partner.
* **Elemental Gems:** Optional collectibles scattered across the map needed to achieve an **A-rank**.

---

## 📝 Remaining Handoff Tasks & Backlog

Because this prototype was developed under a 45-minute sprint, the following items remain open for the next contributor:

* [ ] Fix alignment/positioning of floating map elements.
* [ ] Adjust platform heights to match maximum jump trajectory.
* [ ] Relocate instructional text overlay to a cleaner location.
* [ ] Ensure all platform paths seamlessly connect and lead to the exit doors.
