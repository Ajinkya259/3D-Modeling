# 🎬 AI-Powered Educational Animation Platform

> A personal project that turns text descriptions into professional educational animations using AI and Manim.

## What Is This?

I built this platform to solve a simple problem: creating educational animations is hard and time-consuming. Instead of learning complex animation software, you just describe what you want in plain English, and the AI generates professional Manim animations for you.

Think of it as having 3Blue1Brown's animation skills at your fingertips, without knowing how to code.

## How It Works

### The Simple Version
1. You type: "Show how binary search works"
2. AI writes the animation code
3. System renders it into a video
4. You get a professional animation

### The Technical Version
The platform uses GPT-4 to understand your natural language prompt and generate Manim (Mathematical Animation Engine) code. This code is then executed in a sandboxed environment to produce the animation. The result is rendered as a video file that you can download or use in your projects.

## Features

### Core Functionality
- **Natural Language Input**: Describe animations in plain English
- **AI Code Generation**: GPT-4 writes Manim animation scripts
- **Real-Time Rendering**: Watch your animation being created
- **Multiple Formats**: Export as MP4, WebM, or GIF
- **Resolution Options**: 720p, 1080p, or 4K output

### Editor Features
- **Timeline Editor**: Arrange and combine multiple scenes
- **Transitions**: Add fades, dissolves, and wipes between scenes
- **Scene Management**: Save, organize, and reuse animations
- **Code Viewer**: See and edit the generated animation code
- **Preview System**: Watch animations before final render

### Project Organization
- **Projects**: Group related animations together
- **Scene Library**: Reuse animations across projects
- **Version Control**: Keep track of animation iterations
- **Batch Export**: Export entire projects at once

## Tech Stack

### Frontend
- **React 18** with TypeScript for the UI
- **Tailwind CSS** for styling
- **Vite** for fast development builds
- **Video.js** for video playback

### Backend
- **FastAPI** (Python) for the API server
- **Manim** for animation generation
- **Azure OpenAI** for GPT-4 integration
- **Supabase** for authentication and database
- **Redis** for caching
- **Docker** for sandboxed code execution

### Infrastructure
- Local file storage for animations
- WebSocket for real-time updates
- Queue system for rendering jobs

## Project Structure

```
3D-Modeling/
│
├── cursor-3d-animation/
│   ├── backend/                 # FastAPI server
│   │   ├── app/
│   │   │   ├── api/            # API endpoints
│   │   │   ├── services/       # Core services
│   │   │   │   ├── ai_service.py              # AI integration
│   │   │   │   ├── manim_renderer.py          # Animation rendering
│   │   │   │   ├── prompt_enhancement.py      # Prompt optimization
│   │   │   │   └── scene_service.py           # Scene management
│   │   │   └── models/         # Data models
│   │   └── storage/            # File storage
│   │
│   ├── frontend/               # React app
│   │   ├── src/
│   │   │   ├── components/     # UI components
│   │   │   ├── pages/         # Page components
│   │   │   └── services/      # API client
│   │   └── dist/              # Built files
│   │
│   └── start.sh               # Startup script
│
├── media/                     # Generated animations
├── README.md                 # This file
└── post.md                   # LinkedIn post content
```

## How the AI Works

### Prompt Enhancement
When you type a simple prompt like "show sorting", the AI enhances it to include:
- Specific visual elements
- Color schemes
- Animation timing
- Educational best practices

### Code Generation Process
1. **Understanding**: AI parses your natural language input
2. **Enhancement**: Adds details for better visualization
3. **Code Writing**: Generates complete Manim Python code
4. **Validation**: Checks code for errors
5. **Execution**: Runs code in sandboxed environment
6. **Rendering**: Produces final video output

### Example Input/Output

**Input**: "Visualize quicksort algorithm"

**Generated Code** (simplified):
```python
class QuickSortVisualization(Scene):
    def construct(self):
        # Create array visualization
        array = [5, 2, 8, 1, 9]
        bars = self.create_bars(array)
        
        # Animate sorting process
        self.quicksort_animate(bars, 0, len(array)-1)
```

**Output**: Professional animation showing the quicksort process step-by-step

## Supported Animation Types

### Mathematics
- Geometric proofs and constructions
- Function graphs and transformations
- Calculus concepts (derivatives, integrals)
- Linear algebra visualizations

### Computer Science
- Algorithm visualizations (sorting, searching)
- Data structure operations
- Network and graph algorithms
- Machine learning concepts

### Physics
- Mechanics simulations
- Wave and particle animations
- Electromagnetic field visualizations
- Quantum mechanics concepts

### General Education
- Process flows and diagrams
- Timeline animations
- Concept explanations
- Data visualizations

## Performance Details

### Rendering Speed
- Simple scenes: 5-10 seconds
- Complex scenes: 30-60 seconds
- Timeline compilation: 2-5 seconds per scene

### Quality Settings
- **720p**: Fast rendering, good for previews
- **1080p**: Standard quality, best balance
- **4K**: Highest quality, slower rendering

### Resource Usage
- RAM: 2-4GB during rendering
- CPU: Multi-core utilized for faster processing
- Storage: ~50-200MB per minute of animation

## Current Limitations

- Maximum scene duration: 30 seconds
- Manim-only animations (Three.js coming soon)
- English prompts only
- Some complex 3D animations not yet supported

## Future Enhancements

### Planned Features
- Voice narration with AI-generated speech
- Support for Three.js and p5.js
- Template library for common animations
- Collaborative editing features
- Mobile app for viewing animations

### Experimental Features
- Real-time collaborative editing
- Custom animation styles
- Interactive animations
- AR/VR support

## Why I Built This

As someone who loves educational content but struggled with animation tools, I wanted to make it easier to create high-quality educational animations. Inspired by channels like 3Blue1Brown, I realized that AI could bridge the gap between having an idea and creating a professional animation.

The goal is simple: democratize animation creation so anyone can explain complex concepts visually.

## Technical Challenges Solved

### Code Generation Accuracy
Getting AI to write working Manim code consistently required extensive prompt engineering and a custom validation system.

### Rendering Pipeline
Building a secure sandboxed environment for executing arbitrary Python code while maintaining performance was challenging.

### Real-Time Updates
Implementing WebSocket connections for live rendering progress without overwhelming the client.

### State Management
Managing complex timeline states with multiple scenes, transitions, and edits required careful architecture design.

## Interesting Technical Details

### AI Prompt Engineering
The system uses a multi-stage prompt enhancement process:
1. Initial prompt analysis
2. Context injection (animation best practices)
3. Technical specification generation
4. Code template selection
5. Final code generation

### Security Measures
- Docker containers for code isolation
- Resource limits on rendering processes
- Input sanitization for user prompts
- Rate limiting on API endpoints

### Optimization Techniques
- Redis caching for repeated scenes
- Lazy loading for timeline components
- Incremental rendering for previews
- CDN delivery for final videos

## Want to Collaborate?

This is a personal project, but I'm always interested in connecting with others working on similar problems or interested in educational technology.

Feel free to reach out: **ajinkyasambare01@gmail.com**

## Final Thoughts

This project represents my attempt to make professional animation accessible to everyone. It's not perfect, but it's a step toward a future where anyone can create engaging educational content without technical barriers.

The intersection of AI and creative tools is fascinating, and this project explores just one possibility in that space.

---

- *Built with Claude Code ❤️ and lots of coffee ☕*


