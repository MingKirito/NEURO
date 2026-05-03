# 🧠 NEURO — A Machine Learning Education RPG

**NEURO** is a 2D top-down RPG built in **Godot 4.5** as a Final Year Project. The game teaches players core machine learning concepts — training, attribute tuning, and automation — through hands-on gameplay mechanics across 4 chapters, culminating in a boss fight.

---

Assets used are sourced from free asset websites and are used for educational, non-commercial purposes only.

## 🎮 Gameplay Overview

Rather than reading about machine learning, players *experience* it:

| Chapter | ML Concept Taught | What You Do |
|---------|------------------|-------------|
| **Chapter 1 — Training** | Model training / parameter tuning | Adjust sliders (shape, feel, speed) to train a slime model until it converges |
| **Chapter 2 — Attributes** | Feature weighting | Allocate stat points across Damage, Speed, and Pierce before combat |
| **Chapter 3 — Automation** | Inference / automated decision-making | Configure a danger threshold and response style (Flow / Burst / Switch) for auto-combat |
| **Chapter 4 — Boss** | Final evaluation | Face the boss using everything you've configured |

### Controls

| Key | Action |
|-----|--------|
| `W A S D` | Move |
| `Space` | Attack (manual combat mode) |
| `Tab` / UI button | Open Automation Menu |

---

## 📁 Project Structure

```
NEURO/
├── project.godot              # Godot project config
├── scenes/
│   ├── Chapter1/              # Intro, Training Scene, Training Ground
│   ├── Chapter2/              # Attribute combat levels
│   ├── Chapter3/              # Automation combat levels
│   ├── Chapter4/              # Boss fight
│   ├── player.tscn            # Player character
│   ├── Boss.tscn / orc.tscn / slime.tscn   # Enemies
│   └── MainMenu.tscn
├── scripts/
│   ├── player.gd              # Player movement, combat, auto-fire logic
│   ├── player_stats.gd        # Stat system (damage, speed, pierce, thresholds)
│   ├── automation_menu.gd     # Chapter 3 automation UI & response styles
│   ├── training_scene.gd      # Chapter 1 slider-based training mechanic
│   ├── GameManager.gd         # Save/load, scene management, music routing
│   └── ...
├── dialogue/                  # Story & hint dialogue files (.dialogue)
├── arts/                      # Sprites, fonts, images
├── music/                     # Background music tracks
└── addons/
    └── dialogue_manager/      # Dialogue plugin
```

---

## 🚀 How to Play

### Option A — Download & Play (Recommended)
Download the game directly from itch.io — no Godot installation needed:

👉 **[https://mingkirito.itch.io/neuro](https://mingkirito.itch.io/neuro)**

### Option B — Run from Source
1. Download and install **[Godot 4.5](https://godotengine.org/download)**
2. Clone or download this repository
3. Open Godot → click **Import** → select the `project.godot` file
4. Press **F5** or click the ▶ Play button to run

> No additional plugins or installs needed — everything is bundled in the `addons/` folder.

---

## 🤖 ML Mechanics In Detail

### Chapter 1 — Training a Model
Players adjust three sliders representing model parameters (Shape, Feel, Speed). A slime enemy visually responds — changing colour from black → white as parameters converge toward target values. This simulates the feedback loop of training a model toward an optimal configuration.

### Chapter 2 — Attribute Allocation
Players distribute a limited pool of stat points across three features before entering combat. This mirrors feature weighting — choosing which inputs matter most for a given task.

### Chapter 3 — Neural Automation
Players configure two settings on an **Automation Panel**:
- **Danger Threshold (Bias)** — how close an enemy must be before the system activates (0.0 to 1.0)
- **Response Style** — the firing behaviour once activated:
  - `FLOW` — continuous scaled damage based on threat proximity
  - `BURST` — high-damage triple shot when threat exceeds threshold sharply
  - `SWITCH` — consistent output regardless of excess threat

The player character then fires *automatically* based on real-time threat calculations — simulating how a trained model makes inference decisions.

---

## 🗑️ Files to Exclude / Clean Up Before Pushing

Add a `.gitignore` with the following to keep your repo clean:

```gitignore
# Godot temp/cache files
*.tmp
.godot/
*.uid

# Exported builds (optional — remove if you want to include the .exe)
*.exe
*.pck
*.apk

# OS files
.DS_Store
Thumbs.db
```

> There are several `.tmp` files (e.g. `Chapter3-1.tscn24285809619.tmp`) left over from Godot's editor — these are safe to delete and shouldn't be committed.

---

## 🛠️ Built With

- **[Godot Engine 4.5](https://godotengine.org/)** — Game engine
- **GDScript** — Scripting language
- **[Dialogue Manager](https://github.com/nathanhoad/godot_dialogue_manager)** — Dialogue plugin by Nathan Hoad
- Original art assets, sprites, and music included in the project

---

## 👤 Author

**Shong Ming Xuan** — TP074250  
APD3F2505CS — Artificial Intelligence  
Asia Pacific University (APU)
