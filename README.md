
# 🎯 Galería de Tiro

<p>
  <img alt="Unreal Engine" src="https://img.shields.io/badge/Unreal%20Engine-5.5-0e1128?logo=unrealengine&logoColor=white">
  <img alt="Platform" src="https://img.shields.io/badge/Platform-PC-lightgrey">
  <img alt="Status" src="https://img.shields.io/badge/Status-Completed-brightgreen">
</p>

A first-person shooting gallery built in **Unreal Engine 5.5**: walk up to a firing line and shoot colored targets as they appear, entirely built with Unreal's Blueprint visual scripting on top of the engine's First Person template.

## 📋 Table of Contents

- [Gameplay](#-gameplay)
- [Features](#-features)
- [Tech Stack](#-tech-stack)
- [Project Structure](#-project-structure)
- [Getting Started](#-getting-started)
- [Controls](#-controls)
- [Author](#-author)
- [Status & License](#-status--license)

---

## 🎮 Gameplay

- **First-person shooting** — aim and fire from a first-person perspective, built on Unreal's standard FP character and projectile system.
- **Colored targets** (`BP_Diana`) — three distinct target types (red, yellow, blue), each with its own mesh and material, placed around the range to shoot at.
- **Auto-fire support** — alongside a standard single-shot trigger, a dedicated auto-shoot input action lets the weapon fire continuously while held.
- **Custom game flow** — a dedicated Game Mode and Game Manager Blueprint (`BP_FirstPersonGameMode`, `BP_Gamemanager`) drive the shooting-gallery logic on top of the base template.
- **Pickup weapon** — an additional rifle pickup is available on the range, extending the starting pistol loadout.

## ✨ Features

- Custom target Blueprint (`BP_Diana`) with color-coded static meshes and materials (`SM_Target_Red/Yellow/Blue`, `M_red/Yellow/Blue`)
- Extended input scheme beyond the base template: dedicated `IA_Autoshoot` input action alongside `IA_Shoot`, `IA_Move`, `IA_Look`, and `IA_Jump`, mapped through Enhanced Input contexts (`IMC_Default`, `IMC_Weapons`)
- Mobile control support included via the template's `MobileControls` widget/input setup
- Level built on Unreal's First Person template map, decorated with Level Prototyping assets (grid materials, primitive meshes) for quick range layout

## 🛠️ Tech Stack

| Category | Technology |
|---|---|
| Engine | Unreal Engine **5.5** |
| Scripting | Blueprint visual scripting (no custom C++ module) |
| Input | Enhanced Input System |
| Base Template | Unreal's First Person template (character, weapon, projectile) |
| Plugins | Modeling Tools Editor Mode |

## 📁 Project Structure

```
galeriadetiro/
├── AA1_Iker_Franzoni.uproject      # Unreal project file (Engine 5.5)
├── Config/                          # Project configuration (input, engine, editor)
└── Content/
    ├── FirstPerson/
    │   ├── Blueprints/
    │   │   ├── BP_Diana.uasset             # Shooting-range target (custom)
    │   │   ├── BP_Gamemanager.uasset        # Custom game/round logic
    │   │   ├── BP_FirstPersonGameMode.uasset
    │   │   ├── BP_FirstPersonCharacter.uasset
    │   │   ├── BP_FirstPersonProjectile.uasset
    │   │   ├── BP_Weapon_Component.uasset
    │   │   ├── BP_Pickup_Rifle.uasset
    │   │   └── Linea.uasset
    │   ├── Input/                    # Enhanced Input actions & mapping contexts
    │   └── Maps/FirstPersonMap.umap    # Main playable level
    ├── FPWeapon/                       # Pistol mesh, materials, textures, fire SFX
    ├── Models/                          # Target meshes & color materials (red/yellow/blue/white)
    ├── LevelPrototyping/                  # Grid materials & primitives used for range layout
    └── StarterContent/ · FirstPersonArms/  # Unreal template starter assets
```

## 🚀 Getting Started

### Prerequisites

- **Unreal Engine 5.5** (via Epic Games Launcher or source build)

### Setup

```bash
git clone https://github.com/ikeerfranzz/galeriadetiro.git
```

1. Double-click `AA1_Iker_Franzoni.uproject` (or open it from Epic Games Launcher / Unreal Editor)
2. Let the editor compile shaders and load the project
3. Open `Content/FirstPerson/Maps/FirstPersonMap`
4. Press **Play** in the editor

## 🕹️ Controls

| Input | Action |
|---|---|
| Mouse | Look |
| `W` `A` `S` `D` | Move |
| `Space` | Jump |
| Left Mouse Button | Shoot |
| Hold auto-shoot input | Continuous fire |

## 👨‍💻 Author

**Iker Franzoni** ([@ikeerfranzz](https://github.com/ikeerfranzz)) — sole developer of this project, built as an individual Unreal Engine course exercise.

## 📄 Status & License

This project is **complete**. It was built as a course exercise and is shared here as a portfolio piece; no open-source license is granted. Please reach out before reusing any part of this code or its assets.
