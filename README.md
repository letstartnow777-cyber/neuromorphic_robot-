# NeuroReflex — Neuromorphic Disaster Zone Robot Simulation

> A Q-Learning based robot that learns navigation patterns similarly to reflex actions in humans.

---

## Problem Statement

Simulate a robot that learns navigation patterns similarly to reflex actions in humans — navigating a disaster zone with adaptive decision-making that evolves from random exploration into instant neuromorphic reflex responses.

---

## 🚀 Setup & Installation

This project requires **zero installation**. It runs entirely in the browser.

### Run Locally
```bash
# Step 1: Clone the repository
git clone https://github.com/YOUR_USERNAME/neuromorphic-robot.git

# Step 2: Navigate into the folder
cd neuromorphic-robot

# Step 3: Open the file in your browser
# On Windows:
start neuromorphic_robot.html

# On Mac:
open neuromorphic_robot.html

# On Linux:
xdg-open neuromorphic_robot.html
```

### OR — Direct Run
Just **double-click** `neuromorphic_robot.html` — it opens directly in Chrome, Firefox, or Edge with no setup needed.

### Requirements
| Requirement | Details |
|---|---|
| Browser | Chrome 80+, Firefox 75+, Edge 80+ |
| Internet | Not required (fully offline) |
| Dependencies | None — pure HTML/CSS/JS |
| Server | Not required |

---

## ✨ Features

| Feature | Description |
|---|---|
| Q-Learning Brain | Robot learns from rewards and punishments every episode |
| Reflex Mode | Switches from deliberate thinking to instant cached response when confident |
| Injury Memory | Painful wall collisions burned permanently into memory — never relearned |
| Live Heatmap | Green = safe learned path, Red/Orange = danger zones the robot fears |
| Reflex Arc Animation | Visualizes biological Sensor → Nerve → Motor → Move pipeline live |
| Success Rate Chart | Real-time learning progress graph across all episodes |
| Disaster Zone Map | Rubble walls, fire zones, flood zones, survivor rescue target |
| Adjustable Speed | 1x / 2x / 5x / 15x simulation speed control |
| Episode Tracker | Live epsilon, episode count, step count, success % in header |
| Robot Status Bars | Health, Battery, Confidence bars update in real time |

---

## 🛠️ Tech Stack

| Layer | Technology | Purpose |
|---|---|---|
| UI & Layout | HTML5 + CSS3 | Cyberpunk-themed responsive interface |
| Rendering | HTML5 Canvas API | Grid, robot, heatmap, chart, reflex arc |
| AI Engine | Vanilla JavaScript | Q-Learning algorithm, reflex logic |
| Animation | requestAnimationFrame | Smooth 60fps render loop |
| Styling | CSS Variables + Keyframes | Dynamic colors, scanline effect, glow |
| Fonts | Google Fonts (Share Tech Mono, Rajdhani) | Terminal aesthetic |
| Libraries | **None** | Fully self-contained, no npm, no frameworks |

### Key Algorithms
- **Q-Learning** (Reinforcement Learning) — core navigation learning
- **Epsilon-Greedy Strategy** — exploration vs exploitation balance
- **Hebbian Injury Memory** — permanent penalty boost on painful cells
- **Confidence Threshold Reflex** — Q-value gap detection for reflex switching

---

## 📁 Project Structure

```
neuromorphic-robot/
│
├── neuromorphic_robot.html     # Complete simulation — entire project in one file
│   ├── <style>                 # All CSS — layout, colors, animations
│   ├── <canvas id="simCanvas"> # Main grid simulation canvas
│   ├── <canvas id="chartCanvas">  # Success rate chart
│   ├── <canvas id="reflexArc"> # Reflex arc diagram
│   └── <script>                # Q-Learning engine + render loop
│
├── README.md                   # This file
│
└── screenshots/                # (optional)
    ├── early_learning.png      # Robot wandering randomly
    ├── reflex_mode.png         # Robot in reflex mode with heatmap
    └── success_chart.png       # Success rate climbing to 100%
```

### Inside the Script — Module Breakdown
```
CONFIG          → Grid size, learning params (α, γ, ε)
MAP             → Hardcoded 10×10 disaster zone layout
Q-TABLE         → getQ(), bestAct(), isReflex()
ROBOT STEP      → robotStep() — one move per tick
EPISODE LOGIC   → endEp() — reset, decay epsilon, log stats
DRAW            → draw() — renders grid, heatmap, robot each frame
REFLEX ARC      → drawArc() — animates the 4-node nerve diagram
CHART           → drawChart() — plots rolling success rate
CONTROLS        → toggleSim(), resetSim(), cycleSpeed()
RENDER LOOP     → requestAnimationFrame — ties everything together
```

---

## How It Works

### Q-Learning Formula
```
Q[state][action] += α × (reward + γ × maxFutureQ − Q[state][action])
```

| Parameter | Value | Role |
|---|---|---|
| α (Alpha) | 0.5 | Learning rate |
| γ (Gamma) | 0.95 | Discount — goal reward ripples backward |
| ε (Epsilon) | 1.0 → 0.05 | Exploration decay per episode |

### Reward System
| Event | Reward |
|---|---|
| Reach survivor | +100 |
| Hit wall | -15 |
| Step in fire | -10 |
| Step in flood | -5 |
| Normal step | -1 |

### Learning Progression
```
Episodes 1–10   → Random wandering, 0% success
Episodes 10–25  → First goal hits, reflex mode appears
Episodes 25–50  → Success rate 30–60%
Episodes 50+    → Consistent 80–100%, mostly reflex mode
```

---

## Controls

| Control | Action |
|---|---|
| START / PAUSE | Begin or pause the simulation |
| RESET | Clear Q-table, start fresh |
| SPEED | Cycle 1x / 2x / 5x / 15x |
| HEATMAP | Toggle safe/danger overlay |
| HAZARDS | Toggle fire and flood rendering |

---

## Concepts Demonstrated

- Reinforcement Learning (Q-Learning)
- Neuromorphic Computing
- Biological Reflex Arc Simulation
- Hebbian-style Injury Memory
- Epsilon-Greedy Exploration Strategy
- Real-time Learning Visualization

---

## Submission Info

- **Event:** Hackathon — Problem Statement 2
- **Track:** CSE / AI
- **Type:** Single HTML file, runs fully offline

---

## License

MIT License — Free to use, modify, and distribute for academic purposes.
