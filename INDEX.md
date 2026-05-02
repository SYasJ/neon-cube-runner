# 🎮 Neon Cube Runner - Complete Project

## 📁 Project Files

- **index.html** (11KB) - Main game file (all-in-one HTML/CSS/JS)
- **README.md** (1.8KB) - Full documentation
- **QUICKSTART.md** (1.0KB) - Quick reference guide
- **DEMO.md** (6.7KB) - Demo guide with screenshots

## 🎯 Quick Start

1. Open `index.html` in your web browser
2. Click **"▶ START GAME"**
3. Use mouse or arrow keys to steer
4. Avoid obstacles, collect orbs, build combos!

## 🌟 Key Features

- 🎮 **3D Neon Cubes** - Realistic depth shading and glow effects
- 🌀 **Dynamic Tunnel** - Scrolling 3D tunnel with perspective
- ✨ **Particle Effects** - Explosions on collection/crash
- 🌌 **Parallax Stars** - Multi-layered starfield background
- 📈 **Combo System** - Chain orbs for massive score multipliers
- 🏆 **Local High Score** - Automatically saved
- ⚡ **60 FPS** - Smooth performance
- 🔌 **Zero Dependencies** - Pure vanilla JavaScript

## 🎮 Controls

| Control | Action |
|---------|--------|
| Mouse | Move cursor to steer |
| ← → Arrows | Move left/right |
| A / D | Move left/right |
| Spacebar | Pause/Resume |

## 🎨 Visual Design

**Colors:**
- Background: Deep space (#0f0f23)
- Player: Cyan (#00ffff)
- Glow: Magenta (#ff00ff)
- Obstacles: Red/Orange (#ff4444, #ff6600)
- Orbs: Yellow, Green, Purple, Cyan

**Effects:**
- Neon glow (shadow blur)
- 3D rotation
- Depth shading
- Pulsing animations
- Particle explosions

## 🏗️ Architecture

**Game Loop:** update() → render() → requestAnimationFrame()  
**Systems:** Input, Physics, Spawn, Particle, UI, Save

**Rendering Order (Back → Front):**
1. Background gradient
2. Parallax star layers (×5)
3. Tunnel segments (20)
4. Collectibles (dynamic)
5. Obstacles (dynamic)
6. Particles (dynamic)
7. Player cube
8. UI overlay

## 🔄 Progression

- Every 10 seconds: **Speed += 0.5**, **Level += 1**
- Base speed: 3.0
- Max tested: ~8.0
- Combo timer: 2 seconds

## 📊 Technical Specs

- **File Size:** ~11KB
- **Lines of Code:** ~273
- **Dependencies:** Zero (vanilla JS)
- **Performance:** 60 FPS target
- **Browser Support:** Chrome, Firefox, Safari, Edge
- **Mobile:** Touch controls supported

## 🎬 What to Experience

### Menu Screen
Neon title with glowing cyan/magenta text, start button with hover effects, starfield background.

### Gameplay
Cyan player cube in center, scrolling 3D tunnel walls, red obstacles approaching, colorful orbs floating by with pulsing animations, yellow particle explosions on collection.

### Combo State
Maximum excitement! Rapid-fire particle explosions, scaled-up combo display showing "COMBO x5+!", yellow glow everywhere, orbs flying in all directions.

### Game Over
Bold red "GAME OVER" with glow effect, final score display, best combo and level stats, green restart button.

## 🌟 Why It's Addictive

✅ **Instant Gratification** - Every orb feels rewarding  
✅ **Visual Satisfaction** - Glows, particles, scaling text  
✅ **Combo Rush** - Risk/reward keeps you engaged  
✅ **Progressive Challenge** - Harder but never impossible  
✅ **Neon Aesthetic** - Eye-catching colors pop  
✅ **Smooth Controls** - Responsive mouse/keyboard  
✅ **Endless Replay** - No two runs the same  

## 💡 Tips for High Scores

1. Master mouse control - More precise than keyboard
2. Focus on combos - Prioritize orb collection
3. Anticipate obstacles - Look ahead to plan moves
4. Stay centered - Maximize maneuvering room
5. Pattern recognition - Obstacles become predictable
6. Risk management - Skip orbs if collision risk is high

## 🚀 Getting Started

**Option 1: Direct Open**
- Double-click `index.html` in Finder/Explorer
- Or right-click → Open With → Web Browser

**Option 2: Python Server**
```bash
cd /path/to/project
python3 -m http.server 8000
```
Visit: http://localhost:8000

**Option 3: Node Server**
```bash
cd /path/to/project
npx serve
```
Visit: http://localhost:3000

## 🤝 Contributing

Ideas for enhancements:
- 🎵 Sound effects & background music
- ⚡ Power-ups (shield, slow-motion, magnet)
- 🎮 Different game modes (time trial, challenge)
- 🎨 Skins & themes
- 📱 Enhanced mobile controls
- 🏆 Online leaderboards
- 🏅 Achievement system
- 🌊 Obstacle pattern modes

## 📄 License

MIT License - Free for personal & commercial use!

## 💝 Final Thoughts

This project demonstrates:
- Clean, efficient code structure
- Creative visual design within constraints
- Engaging core gameplay loop
- Smooth 60 FPS performance
- Zero external dependencies

**Enjoy the game! May your combos be long and your scores high! 🎮✨**

---

**Built with ❤️ using HTML5 Canvas & Vanilla JavaScript**
