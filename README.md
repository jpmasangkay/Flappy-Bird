# 🐦 FLAPPY BIRD

### Unity Arcade Game

**Tap. Soar. Survive.**

A Unity recreation of the iconic Flappy Bird arcade game — simple to learn, impossible to master. Navigate your bird through an endless gauntlet of pipes by timing every tap perfectly. One wrong move and it's game over.

[![Unity](https://img.shields.io/badge/Unity-000000?style=for-the-badge&logo=unity&logoColor=white)](https://unity.com)
[![C#](https://img.shields.io/badge/C%23-239120?style=for-the-badge&logo=csharp&logoColor=white)](https://learn.microsoft.com/en-us/dotnet/csharp/)

---

## ✨ Features

### 🎯 Core Gameplay

- Classic **tap-to-flap** mechanic — one input, total control
- **Endless scrolling** pipe obstacles with randomized gap positions
- Unforgiving difficulty — a single collision ends your run instantly
- A **score system** that tracks every pipe you clear

### 🐤 Player

- Physics-driven bird movement powered by Unity's **Rigidbody2D**
- Smooth gravity arc and responsive flap impulse for tight, satisfying control
- Animated bird sprite that reacts to rise and fall

### 🌵 Obstacles & World

- Continuously spawning **pipe pairs** that scroll from right to left
- Randomized vertical gap placement keeps every run fresh and unpredictable
- Looping background and ground for a seamless infinite world

### 💥 Collision & Game States

- Pixel-accurate collision detection using Unity's **2D physics engine**
- Instant game-over on pipe or ground contact
- **Restart flow** that resets the scene cleanly for another attempt

### 🔊 Audio

- Sound effects for flapping, scoring, and collision
- Light background audio to complement the fast-paced, bite-sized gameplay

---

## 🛠️ Tech Stack

| Technology | Purpose |
|-----------|---------|
| **Unity** | Game engine — rendering, physics, input, and scene management |
| **C#** | All gameplay logic, bird controller, pipe spawning, and scoring |
| **Unity Physics 2D** | Rigidbody movement, gravity simulation, and collision detection |
| **Unity Asset Pipeline** | Sprite management, animations, and audio playback |

---

## 🚀 Getting Started

### Play Immediately (Pre-built)

A pre-built Windows executable is included in the repository — no Unity installation required.

1. Clone or download the repository
2. Run **`Test.exe`** directly
3. Tap / click / press **Space** to start flapping

```bash
# Clone the repository
git clone https://github.com/jpmasangkay/Flappy-Bird.git
cd Flappy-Bird
```

Then simply double-click **`Test.exe`** to launch the game.

### Opening in Unity (Source)

> **Note:** This repository contains the built game output. To view or modify the source project, the Unity project source files would be needed separately.

1. Open **Unity Hub**
2. Click **Open** → **Add project from disk**
3. Select the project folder
4. Unity will import all assets and compile scripts automatically
5. Once loaded, open the main scene from the `Assets/` folder and press **▶ Play**

---

## 📁 Project Structure

```
Flappy-Bird/
├── Test.exe                              # Game executable — run this to play
├── UnityPlayer.dll                       # Unity runtime library
├── UnityCrashHandler64.exe               # Unity crash reporting handler
├── Test_Data/                            # Game data, assets, and managed scripts
│   ├── Managed/                          # Compiled C# assemblies
│   ├── Resources/                        # Packed game resources
│   └── StreamingAssets/                  # Runtime-loaded assets
├── MonoBleedingEdge/                     # Mono runtime for .NET scripting backend
├── Test_BurstDebugInformation_DoNotShip/ # Burst compiler debug symbols (dev only)
└── .gitattributes
```

---

## 🧠 How It Works

Flappy Bird is built on Unity's **component-based architecture**, with each system handled by focused C# MonoBehaviour scripts:

1. **Bird Controller** — Applies a constant downward gravity force via Unity's `Rigidbody2D`. Each tap triggers an upward velocity impulse, producing the characteristic flap arc. Collision with any obstacle or the ground immediately triggers the game-over state.

2. **Pipe Spawner** — A spawner script instantiates pipe prefab pairs at a fixed horizontal interval. Each pair is placed at a random vertical offset within a defined range, then moves left at a constant scroll speed before being destroyed off-screen.

3. **Scoring System** — A trigger collider positioned between each pipe gap detects when the bird passes through cleanly. Every successful pass increments the score and updates the on-screen HUD.

4. **Game Manager** — Coordinates global state between the active gameplay, game-over, and restart phases. On game over, it freezes relevant game objects and surfaces the restart UI. On restart, it reloads the scene to reset all state cleanly.

5. **Infinite Scrolling World** — The background and ground use tiling or repositioning logic to loop seamlessly, creating the illusion of an endless environment without performance overhead.

---

## 🎮 How to Play

1. **Launch** `Test.exe` or press **Play** in the Unity Editor
2. **Tap / click / press Space** to make the bird flap and gain altitude
3. **Navigate through the gaps** between the pipe pairs
4. **Don't touch the pipes or the ground** — one hit ends the run
5. **Beat your high score** — see how many pipes you can clear in a single run

---
