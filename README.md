# 🏍️ NEON RASH: PROTOCOL 3D

> _A high-velocity, low-latency combat racing simulation rendered in the void of WebGL._

![Gameplay Screenshot](assets/images/Screenshot%202025-12-11%20at%2012.26.19%E2%80%AFAM.png)

## 💾 System Overview

**NEON RASH** is a browser-based, multiplayer combat racer inspired by the classics of the 16-bit era, upgraded with a cyberpunk wireframe aesthetic. Completely vibe coded in vanilla JavaScript using **Three.js** for the render pipeline and **PeerJS** for decentralized P2P networking.

This is not just a game; it's a test of reflexes, packet loss, and raw JavaScript performance.

## 🛠️ Tech Stack

- **Render Engine**: [Three.js (r160)](https://threejs.org/) - Utilizing `WebGLRenderer` with `PCFSoftShadowMap`.
- **Post-Processing**: `EffectComposer` pipeline featuring `UnrealBloomPass` for maximum neon saturation.
- **Networking**: [PeerJS](https://peerjs.com/) (WebRTC) - Implementing a Star Topology (Host-Client) for real-time state synchronization.
- **Physics**: Custom deterministic arcade physics with AABB collision detection and vector-based movement.
- **Language**: ECMAScript 2020+ (Modules).

## ⚡ Features

### 🌐 Multiplayer Netcode

- **Room-Based Matchmaking**: Generate unique 4-character hex codes to create private lobbies.
- **State Synchronization**: Real-time broadcasting of player coordinates (`x`, `z`), velocity, and combat states.
- **Latency Handling**: Client-side interpolation for smooth remote player movement.

### ⚔️ Combat & Gameplay

- **Lateral Impulse Mechanic**: Press `SPACE` to execute a kinetic kick, applying lateral velocity to opponents.
- **Traffic Hazards**: AI-controlled neon vehicles with randomized lane logic.
- **Procedural Track**: Infinite scrolling road segments with dynamic curvature generation.
- **Damage Model**: 3-hit health system with visual feedback and camera shake trauma.

### 📊 Telemetry & UI

- **F1-Style Timer**: High-contrast, 60-second countdown timer.
- **Live Leaderboard**: Real-time sorting based on **Hits** (primary) and **Distance** (secondary).
- **Status Tracking**: Dynamic badges for player states:
  - `RACING` (Green)
  - `CRASHED` (Red)
  - `FINISHED` (Yellow)

## 🎮 Controls

| Key                  | Action     | Description                       |
| :------------------- | :--------- | :-------------------------------- |
| **Arrow Up**         | Accelerate | Increase forward velocity vector. |
| **Arrow Down**       | Brake      | Apply friction to reduce speed.   |
| **Arrow Left/Right** | Steer      | Lateral translation across lanes. |
| **Space**            | Kick       | Execute combat maneuver.          |
| **R**                | Restart    | Reboot game state (Host only).    |

## 📸 Gallery

![Lobby Screen](assets/images/Screenshot%202025-12-11%20at%2012.27.01%E2%80%AFAM.png)
_The connection interface._

![Combat](assets/images/Screenshot%202025-12-11%20at%2012.27.15%E2%80%AFAM.png)
_Mid-race combat maneuver._

---
