# Voxel Maze Adventure

![Voxel Maze Adventure](https://raw.githubusercontent.com/lalomorales22/Voxel-Maze-Adventure/main/screenshot.png)

A browser-based 3D voxel adventure game featuring character customization, procedural maze generation, and AI-powered NPCs using Ollama.

## Features

- **Customizable Character Creator**: Design your own voxel character with different body types, colors, hairstyles, and accessories
- **Multiple Maze Generation Algorithms**: Choose from 6 different procedural generation methods:
  - Fixed Maps (Version 1.0)
  - Depth-First Search (Version 2.1)
  - Kruskal's Algorithm (Version 2.2)
  - Prim's Algorithm (Version 2.3)
  - Recursive Division (Version 2.4)
  - Binary Tree (Version 2.5)
- **AI-Powered NPCs**: Chat with in-game enemies using Ollama LLMs
- **Engaging Gameplay**: Collect coins, find keys, avoid enemies, and reach the exit

## Getting Started

### Option 1: Play Online

Visit the [GitHub Pages demo](https://lalomorales22.github.io/Voxel-Maze-Adventure/) to play directly in your browser.

### Option 2: Run Locally

1. Clone the repository:
```bash
git clone https://github.com/lalomorales22/Voxel-Maze-Adventure.git
cd Voxel-Maze-Adventure
```

2. Start a local web server:
```bash
# Using Python (recommended)
python -m http.server 8000

# OR using Node.js
npx serve
```

3. Open your browser and go to `http://localhost:8000`

## AI Chat Integration with Ollama

The game includes an AI chat feature for talking with NPCs using Ollama, an open-source LLM runner.

### Setting Up Ollama

1. Install Ollama from [ollama.ai](https://ollama.ai)
2. Start Ollama with CORS enabled:
```bash
OLLAMA_ORIGINS=* ollama serve
```

3. Pull one of the compatible models:
```bash
ollama pull llama3.2:1b   # Fastest, smallest model
ollama pull llama3.2:3b   # Balanced option
ollama pull deepseek-r1   # Alternate model option
```

Once Ollama is running with a model, the game will automatically connect to it when you open the chat panel.

### Fallback Mode

If you don't have Ollama installed or experience connection issues, the game includes a "Fallback Mode" that simulates AI responses. Enable it from the chat panel settings.

## Game Controls

- **W/A/S/D or Arrow Keys**: Move character
- **Space**: Action
- **P**: Pause game
- **Right-click + Drag**: Rotate camera
- **Mouse Wheel**: Zoom camera

## Technical Details

This project uses:
- Three.js for 3D rendering
- Pure JavaScript for game logic and maze generation
- HTML/CSS for the UI
- Ollama API for AI chat features

No external dependencies or build tools are required!

## Maze Algorithms

Each maze generation algorithm creates a unique playing experience:

- **DFS**: Creates long corridors with few branches
- **Kruskal's**: Generates a more "perfect" maze with equal path distribution
- **Prim's**: Creates mazes with short, winding passages
- **Recursive Division**: Produces mazes with long straight corridors
- **Binary Tree**: Creates mazes with a distinct "flow" toward one corner

## License

MIT License

## About

Created by [Lalo Morales](https://github.com/lalomorales22)

Feel free to contribute, report issues, or suggest improvements!
