# 🐍 Classic Snake Game

**Built with Amazon Q - Amazon Builder Developer Community T-Shirt Challenge**

A modern recreation of the classic Nokia Snake game with enhanced graphics, progressive difficulty, and exciting bonus features. This browser-based game combines nostalgic gameplay with contemporary web technologies.

![Game Preview](https://img.shields.io/badge/Game-Snake-brightgreen) ![HTML5](https://img.shields.io/badge/HTML5-Canvas-orange) ![JavaScript](https://img.shields.io/badge/JavaScript-ES6-yellow) ![CSS3](https://img.shields.io/badge/CSS3-Animations-blue)

## 🎮 Game Features

### Core Gameplay
- **Classic Snake Mechanics**: Control a growing snake to eat food and avoid collisions
- **Wrap-Around Edges**: Snake teleports to opposite side when hitting screen boundaries
- **Progressive Difficulty**: Game speed increases every 10 mice eaten
- **Level System**: Clear level progression with visual feedback

### Visual Enhancements
- **Realistic Snake Design**: 
  - Distinct head with directional eyes
  - Segmented body with gradient colors
  - Tapered tail for natural appearance
- **Detailed Mouse Graphics**: Brown mice with ears, tails, and eyes
- **Bonus Golden Mice**: Special blinking golden mice worth 100 points
- **Smooth Animations**: CSS animations and canvas rendering

### Advanced Features
- **Bonus System**: Golden mice appear randomly for 10 seconds
- **Speed Progression**: 7 difficulty levels with increasing challenge
- **Score Tracking**: Points system with level-based progression
- **Visual Feedback**: Level-up notifications and bonus alerts
- **Responsive Controls**: Arrow keys and WASD support

## 🕹️ How to Play

### Getting Started
1. Open `snake-game.html` in any modern web browser
2. Press any arrow key (↑↓←→) or WASD to start moving
3. Guide the snake to eat mice and grow longer
4. Avoid hitting your own body

### Controls
| Key | Action |
|-----|--------|
| ↑ / W | Move Up |
| ↓ / S | Move Down |
| ← / A | Move Left |
| → / D | Move Right |

### Scoring System
- **Regular Mouse**: 10 points
- **Golden Bonus Mouse**: 100 points
- **Level Up**: Every 10 regular mice eaten

### Game Mechanics
- **Wrap-Around**: Snake appears on opposite side when hitting edges
- **Self-Collision**: Game ends when snake hits its own body
- **Bonus Timer**: Golden mice disappear after 10 seconds
- **Speed Increase**: Game gets faster with each level

## 🎯 Game Objectives

### Primary Goals
- Eat as many mice as possible to grow the snake
- Achieve the highest score possible
- Progress through multiple difficulty levels
- Capture bonus golden mice for extra points

### Difficulty Progression
| Level | Speed (ms) | Mice Required | Description |
|-------|------------|---------------|-------------|
| 1 | 200 | 0-9 | Beginner - Slow and steady |
| 2 | 175 | 10-19 | Getting faster |
| 3 | 150 | 20-29 | Moderate challenge |
| 4 | 125 | 30-39 | Fast-paced action |
| 5 | 100 | 40-49 | Expert level |
| 6 | 75 | 50-59 | Master difficulty |
| 7+ | 50 | 60+ | Maximum challenge |

## 🛠️ Technical Implementation

### Technologies Used
- **HTML5 Canvas**: For smooth 2D graphics rendering
- **Vanilla JavaScript**: Game logic and mechanics
- **CSS3**: Styling, animations, and responsive design
- **Modern Web APIs**: Keyboard event handling

### Code Structure
```
snake-game.html
├── HTML Structure
│   ├── Game Canvas (400x400px)
│   ├── Score Display
│   ├── Level Indicator
│   └── Control Instructions
├── CSS Styling
│   ├── Retro Gaming Theme
│   ├── Glowing Effects
│   ├── Animation Keyframes
│   └── Responsive Layout
└── JavaScript Game Engine
    ├── Game State Management
    ├── Snake Movement Logic
    ├── Collision Detection
    ├── Food Generation
    ├── Bonus System
    ├── Level Progression
    └── Rendering Engine
```

### Key Functions
- `moveSnake()`: Handles snake movement and collision detection
- `drawGame()`: Renders all game elements on canvas
- `randomFood()`: Generates regular food positions
- `createBonusFood()`: Spawns golden bonus mice
- `gameLoop()`: Main game loop with timing control

## 🎨 Visual Design

### Color Scheme
- **Snake Head**: Bright Green (#00ff00)
- **Snake Body**: Medium Green (#00cc00)  
- **Snake Tail**: Dark Green (#008800)
- **Regular Mouse**: Brown (#8B4513)
- **Bonus Mouse**: Gold (#FFD700)
- **Background**: Black (#000000)
- **UI Elements**: Neon Green (#00ff00)

### Special Effects
- **Glowing Borders**: CSS box-shadow effects
- **Blinking Animation**: Bonus mice visibility toggle
- **Pulse Animation**: Level-up notifications
- **Gradient Background**: Purple gradient backdrop

## 🚀 Installation & Setup

### Prerequisites
- Modern web browser (Chrome, Firefox, Safari, Edge)
- No additional software required

### Quick Start
1. **Download**: Save `snake-game.html` to your computer
2. **Open**: Double-click the file or open with your browser
3. **Play**: Press any arrow key to start the game

### File Structure
```
project-folder/
└── snake-game.html (Complete game in single file)
```

## 🎪 Game Features Deep Dive

### Snake Mechanics
- **Starting Size**: 3 segments (head + 2 body parts)
- **Growth Pattern**: Adds one segment per regular mouse eaten
- **Movement**: Grid-based movement system (20px grid)
- **Direction Control**: Prevents immediate reverse direction

### Food System
- **Regular Mice**: Spawn randomly, worth 10 points
- **Bonus Mice**: 0.5% spawn chance per game loop
- **Collision Avoidance**: Food never spawns on snake body
- **Visual Distinction**: Different colors and animations

### Level Progression
- **Trigger**: Every 10 regular mice eaten
- **Speed Increase**: 25ms faster per level
- **Visual Feedback**: Animated level-up notifications
- **Maximum Speed**: Caps at 50ms for playability

## 🏆 High Score Tips

### Beginner Strategies
- Start slow and learn the controls
- Use edges for quick escapes via wrap-around
- Focus on regular mice before chasing bonuses
- Plan your path to avoid trapping yourself

### Advanced Techniques
- **Edge Dancing**: Use wrap-around for complex maneuvers
- **Bonus Hunting**: Risk assessment for golden mice
- **Speed Management**: Adapt strategy as game speeds up
- **Space Control**: Maintain open areas for movement

## 🐛 Troubleshooting

### Common Issues
- **Controls Not Working**: Ensure browser window has focus
- **Game Too Fast**: Practice on lower levels first
- **Visual Glitches**: Try refreshing the browser
- **Performance Issues**: Close other browser tabs

### Browser Compatibility
- ✅ Chrome 60+
- ✅ Firefox 55+
- ✅ Safari 12+
- ✅ Edge 79+

## 🔧 Customization Options

### Easy Modifications
- **Game Speed**: Adjust `gameSpeed` variable (line 47)
- **Grid Size**: Modify `gridSize` constant (line 35)
- **Colors**: Change color values in `drawGame()` function
- **Bonus Frequency**: Adjust spawn probability (line 265)

### Advanced Customizations
- Add sound effects
- Implement high score persistence
- Create different game modes
- Add power-ups and obstacles

## 📈 Future Enhancements

### Planned Features
- [ ] Sound effects and background music
- [ ] Local high score storage
- [ ] Multiple difficulty modes
- [ ] Power-up system
- [ ] Multiplayer support
- [ ] Mobile touch controls

### Community Contributions
- Bug reports and feature requests welcome
- Code improvements and optimizations
- Visual enhancements and themes
- Gameplay mechanic suggestions

## 🏅 Amazon Builder Challenge

This game was created as part of the **Amazon Builder Developer Community T-Shirt Challenge**, demonstrating:

- **Full-Stack Development**: Complete game implementation
- **Modern Web Technologies**: HTML5, CSS3, JavaScript ES6
- **User Experience Design**: Intuitive controls and feedback
- **Progressive Enhancement**: Layered feature complexity
- **Code Quality**: Clean, documented, maintainable code

### Challenge Requirements Met
✅ **Complete Game Implementation**: Fully functional Snake game  
✅ **Amazon Q Integration**: Built with Amazon Q assistance  
✅ **Technical Excellence**: Modern web standards compliance  
✅ **User Experience**: Engaging and intuitive gameplay  
✅ **Documentation**: Comprehensive README and code comments  

## 📄 License

This project is open source and available under the MIT License.

## 🤝 Acknowledgments

- **Amazon Q**: AI assistant that helped build this game
- **Amazon Builder Community**: Inspiration and challenge framework
- **Classic Nokia Snake**: Original game concept and mechanics
- **Web Development Community**: Best practices and techniques

---

**Built with ❤️ using Amazon Q Developer**

*Ready to play? Open the game and press any arrow key to start your Snake adventure!*
