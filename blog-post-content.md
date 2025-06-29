# 🐍 Building a Classic Snake Game with Amazon Q CLI

*How AI-powered development transformed a nostalgic idea into a fully-featured browser game*

## Introduction

As part of the **Amazon Builder Developer Community T-Shirt Challenge**, I built a complete Snake game using Amazon Q CLI. This post covers effective AI prompting techniques and how Amazon Q handled classic programming challenges.

## 🎮 Why I Chose Snake Game

My first mobile phone was a Nokia with the built-in Snake game. Despite simple graphics, it was addictive and nostalgic. Snake offered the perfect balance for demonstrating development skills: core mechanics (movement, collision detection), advanced features (progressive difficulty, bonus systems), and technical challenges (canvas rendering, game loops).

## 🤖 Effective Prompting Techniques

### 1. Iterative Feature Building
Instead of requesting everything at once, I broke down features logically:
```
Initial: "Create basic Snake game with arrow controls"
Enhancement: "Add wrap-around edges instead of wall collision"
Polish: "Add bonus golden mice that blink and give 100 points"
```

### 2. Specific Visual Requirements
**Instead of**: "Make the snake look better"  
**I used**: "Make snake head with directional eyes, start with size 3, make tail smaller and darker"

### 3. Problem-Solution Context
When encountering issues, I provided clear context about the problem and desired solution, which helped Amazon Q understand both the technical issue and expected behavior.

## 🧠 How AI Handled Programming Challenges

### Collision Detection
```javascript
// Self-collision detection
for (let segment of snake) {
    if (head.x === segment.x && head.y === segment.y) {
        gameOver();
        return;
    }
}

// Food collision with growth logic
if (head.x === food.x && head.y === food.y) {
    score += 10;
    randomFood();
} else {
    snake.pop(); // Remove tail if no food eaten
}
```

### Wrap-Around Logic
```javascript
// Handle wrap-around at edges
if (head.x < 0) {
    head.x = tileCount - 1; // Wrap to right side
} else if (head.x >= tileCount) {
    head.x = 0; // Wrap to left side
}
```

### Dynamic Speed Adjustment
```javascript
// Increase speed every 10 mice
if (miceEaten % 10 === 0) {
    level++;
    gameSpeed = Math.max(50, gameSpeed - 25);
    clearInterval(gameInterval);
    gameInterval = setInterval(gameLoop, gameSpeed);
}
```

## ⚡ Development Automation Benefits

Amazon Q CLI significantly accelerated development:
- **Instant Code Generation**: Complete HTML/CSS/JavaScript structure in seconds
- **Automatic Bug Fixes**: Identified root causes and implemented solutions
- **Feature Integration**: Seamlessly added bonus mouse system without breaking existing code
- **Documentation**: Generated comprehensive README automatically

## 💻 Interesting AI-Generated Solutions

### Directional Snake Eyes
```javascript
// Eyes change direction based on movement
if (dx === 1) { // Moving right
    ctx.fillRect(x + 12, y + 4, 3, 3);
    ctx.fillRect(x + 12, y + 12, 3, 3);
} else if (dx === -1) { // Moving left
    ctx.fillRect(x + 3, y + 4, 3, 3);
    ctx.fillRect(x + 3, y + 12, 3, 3);
}
```

### Blinking Bonus Mouse
```javascript
// Toggle blink state every 5 game loops
if (bonusTimer % 5 === 0) {
    bonusBlinkState = !bonusBlinkState;
}

// Only draw if visible during blink
if (bonusFood && bonusBlinkState) {
    // Draw golden mouse with sparkle effects
}
```

## 🎯 Final Game Features

The completed game includes:
- **Core Mechanics**: Arrow/WASD controls, wrap-around edges, progressive difficulty
- **Visual Design**: Snake with head/body/tail differentiation, realistic mice graphics
- **Advanced Features**: Golden bonus mice (100 points), blinking effects, level progression
- **Technical Excellence**: HTML5 Canvas rendering, efficient game loop, modern event handling

## 🚀 Key Learnings

- **Iterative prompting** produces better results than monolithic requests
- **Context and specificity** are crucial for optimal AI assistance
- **AI excels** at implementing well-defined requirements
- **Complex features** can be built through logical decomposition

## 🎉 Conclusion

Building this Snake game with Amazon Q CLI showcased the power of AI-assisted development. What traditionally would require days of coding was accomplished in hours through effective AI collaboration. Amazon Q didn't just generate code - it became a collaborative partner that understood game development principles and implemented sophisticated solutions.

This demonstrates that AI tools like Amazon Q CLI empower developers to build more ambitious projects faster and with higher quality.

---

**Built with**: Amazon Q CLI, HTML5 Canvas, JavaScript ES6, CSS3

**Tags**: #AmazonQCLI #GameDevelopment #AI #WebDevelopment #JavaScript
