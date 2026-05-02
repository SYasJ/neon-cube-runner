# Neon Cube Runner 🌟

A fast-paced 3D tunnel racing game built with HTML5 Canvas and JavaScript. Dodge obstacles, collect power-ups, and survive as long as you can in this neon-lit cyberpunk world!
[Gameplay Screenshot 1](https://github.com/SYasJ/neon-cube-runner/blob/main/Game%20Play%20Screen.png)
*Visual: 3D tunnel with neon obstacles*
[Gameplay Screenshot 2](https://github.com/SYasJ/neon-cube-runner/blob/main/Game%20Play%20Action.png)
*Easy keyboard controls*

## 🎮 Features

- **Immersive 3D Tunnel** — Dynamic perspective-shifting tunnel with gradient lighting effects
- **Smooth Controls** — Responsive keyboard movement (Arrow keys or A/D), mouse/touch support
- **3-Life System** — Get multiple chances! Hearts display your remaining lives
- **Combo Multiplier** — Chain collectibles for massive score bonuses
- **Progressive Difficulty** — Speed and level increase as you survive longer
- **Persistent Leaderboard** — High scores saved in localStorage
- **Full Responsive** — Automatically adjusts to any screen size
- **Visual Polish** — Particle effects, glowing neon cubes, smooth animations

## 🚀 Quick Start

### Download & Play

1. **Download the file**
   ```bash
   # Clone or download index.html
   wget https://github.com/yourusername/neon-cube-runner/raw/main/index.html
   ```

2. **Open in browser**
   - Double-click `index.html`, or
   - Open with Chrome/Firefox/Safari/Edge
   - No installation needed — it's a standalone HTML file!

3. **Start playing**
   - Click **"▶ START GAME"** or press **SPACE**
   - Use **← →** or **A/D** to move left/right
   - Dodge red/orange obstacles
   - Collect yellow/green/purple cubes for points
   - Press **SPACE** to pause anytime
   
### Live Demo

[![Open in CodeSandbox](https://codesandbox.io/static/img/play-codesandbox.svg)](https://codesandbox.io/s/neon-cube-runner-template)

## 🎯 How to Play

### Controls

| Key | Action |
|-----|--------|
| **←** or **A** | Move Left |
| **→** or **D** | Move Right |
| **SPACE** | Pause/Resume |
| **SPACE** (Menu) | Start Game |

### Objective

- **Survive** as long as possible in the neon tunnel
- **Collect** glowing cubes for points (100 × combo multiplier)
- **Build combos** by collecting cubes quickly (120-frame timer)
- **Avoid** red and orange obstacles — lose a life on collision
- **Reach** higher levels for more challenge and speed

### Scoring

- **Collectible**: 100 × (combo + 1) points
- **Obstacle avoided**: 1 point per frame at end of screen
- **Combo bonus**: Chain collects quickly for ×2, ×3, ×4+ multipliers
- **Level bonus**: Higher levels = faster speed = more points

### Lives System

- Start with **3 lives** (♥♥♥)
- Lose 1 life per obstacle collision
- Respawn at center after losing a life
- Game over when all 3 lives are lost
- Check "Best Combo" and "Level" in final stats

## 📊 Game Mechanics

### Difficulty Progression

| Level | Speed | Note |
|-------|-------|------|
| 1 | 3.0 | Starting speed |
| 2 | 3.5 | +0.5 per level |
| 5 | 5.0 | Noticeably faster |
| 10 | 7.5 | Challenging |
| 15+ | 10.0+ | Expert mode |

- Level increases every **600 game frames** (~10 seconds at 60fps)
- Speed increases by **0.5** per level
- Obstacle spawn rate: `0.015 + speed × 0.005`
- Collectible spawn rate: `0.01`

### Visual Effects

- **3D Tunnel** — Radial gradient with purple/cyan/magenta lighting
- **Glowing Cubes** — Each collectible pulses and glows
- **Particle Explosions** — 20+ particles on life loss, 15+ on collection
- **Speed Bar** — Bottom HUD shows current speed percentage
- **Neon Shadows** — Dynamic glow effects on all game objects

## 💻 Technical Details

### Architecture

```
index.html (Single File Application)
├── HTML Structure
│   ├── Canvas (WebGL 2D context)
│   ├── UI Overlay (DOM elements)
│   └── Menu/Game Over screens
├── CSS Styling
│   ├── Full-viewport responsive design
│   ├── Gradient buttons with hover effects
│   └── Smooth transitions
└── JavaScript Game Engine
    ├── Game Loop (requestAnimationFrame)
    ├── Collision Detection (AABB)
    ├── Particle System
    └── Tunnel Renderer
```

### Browser Compatibility

- ✅ Chrome 90+
- ✅ Firefox 88+
- ✅ Safari 14+
- ✅ Edge 90+
- ✅ Mobile browsers (touch controls)

### Performance

- **60 FPS** target (vsync via requestAnimationFrame)
- **Optimized rendering** — object pooling for particles
- **No dependencies** — pure vanilla JS
- **<150 KB** total size (compressed)

## 📁 Project Structure

```
neon-cube-runner/
├── index.html              # Main game file (all-in-one)
├── README.md               # This file
└── FIXES.md                # Development changelog
```

## 🔧 Customization

### Colors & Theme

Edit the color constants in the JavaScript section:

```javascript
player.color = '#00ffff';        // Player color
obstacle colors: '#ff4444', ...  // Obstacle colors
collectible colors: '#ffff00', ... // Power-up colors
```

### Difficulty Tuning

```javascript
baseSpeed = 3;                          // Starting speed
speed increment = 0.5 per level          // Level progression
obstacle spawn = 0.015 + speed * 0.005   // Spawn frequency
```

### Adding Lives

```javascript
lives = 3;  // Change to 5, 10, etc.
```

## 🎨 Assets

All assets are procedurally generated:

- **No external images** — pure Canvas drawing
- **No audio** — lightweight and distraction-free (add your own!)
- **No fonts** — system fonts only

## 🔍 Development

### Local Development

1. Clone the repository
   ```bash
   git clone https://github.com/yourusername/neon-cube-runner.git
   cd neon-cube-runner
   ```

2. Open in browser
   ```bash
   open index.html  # macOS
   start index.html # Windows
   xdg-open index.html # Linux
   ```

3. Edit and refresh — no build step required!

### Adding Sound

Want to add audio? Insert this in the `<head>`:

```html
<audio id="bgm" src="music.mp3" loop></audio>
<audio id="sfx" src="beep.mp3"></audio>
```

Then play with: `document.getElementById('sfx').play()`

## 📝 License

MIT License — Feel free to use, modify, and distribute!

```
Copyright (c) 2026 Neon Cube Runner

Permission is hereby granted, free of charge, to any person obtaining a copy...
```

## 🤝 Contributing

Contributions welcome! Areas for improvement:

- [ ] Add sound effects and background music
- [ ] Mobile touch controls (virtual joystick)
- [ ] Power-up items (shield, slow-mo, magnet)
- [ ] Multiple player skins/colors
- [ ] Level editor
- [ ] Online leaderboard
- [ ] Replay system

**Submit PRs** or open **Issues** for bugs and feature requests!

## ⭐ Show Your Support

If you enjoy this game, please:

- ⭐ Star this repository
- 📢 Share with friends
- 💬 Leave feedback
- 🐛 Report bugs

## 📧 Contact

For questions, suggestions, or bug reports:

- GitHub Issues: [github.com/yourusername/neon-cube-runner/issues](https://github.com/yourusername/neon-cube-runner/issues)
- Twitter: [@yourhandle](https://twitter.com/yourhandle)

---

**Built with ❤️ and pure JavaScript**

[![JavaScript](https://img.shields.io/badge/JavaScript-ES6+-yellow.svg)](https://developer.mozilla.org/en-US/docs/Web/JavaScript)
[![HTML5](https://img.shields.io/badge/HTML5-Canvas-orange.svg)](https://developer.mozilla.org/en-US/docs/Web/API/Canvas_API)
[![License](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)
[![Version](https://img.shields.io/badge/Version-1.0.0-blue.svg)](.)
