# 🎸 Brenna's Interactive Guitar Learning App

## Project Vision
Create an interactive guitar learning application specifically designed for young metalheads who want to learn guitar through the songs they actually love, not boring traditional exercises.

## Dual Purpose: Learning & Building
**This project serves two goals:**

### 🎸 Primary Goal: Help Brenna Learn Guitar
- Create an engaging, metal-focused guitar learning experience
- Use interactive visual cues to teach timing and rhythm
- Focus on songs she actually wants to play

### 🛠️ Secondary Goal: Teach Nigel Proper Development Practices
- Demonstrate professional project structure and organization
- Show how to document decisions and maintain project context
- Practice iterative development (prototype → feedback → improve)
- Learn how to build maintainable code that survives across sessions
- Experience the full development lifecycle from concept to deployment

**This dual approach means every decision is documented, every process is explained, and the project becomes a learning experience for both users - Brenna learns guitar, Nigel learns development best practices.**

## The Problem We're Solving
- Traditional guitar learning focuses on folk songs and classics that don't inspire young metal fans
- Static tablature is hard for beginners to understand timing and rhythm
- No visual feedback makes learning boring and disconnected
- Most guitar apps don't cater to the metal/punk aesthetic and mindset

## Our Solution
An interactive web app that:
- Features actual metal/punk songs (Ghost, Metallica, System of a Down, Bad Religion, etc.)
- Shows tablature that lights up in real-time to teach rhythm and timing
- Uses authentic guitar sounds, not cheesy synthesized beeps
- Has a dark, metal aesthetic that matches the user's musical taste
- Provides gamified progress tracking to keep learners motivated

## Target User
**Brenna (14 years old)**
- Into bands like Ghost, Metallica, System of a Down, Bad Religion
- Beginner guitarist
- Needs visual and audio cues to learn effectively
- Motivated by playing songs she actually loves

## Current Status
**✅ Prototype Complete (v0.1)**
- Basic interactive tablature with red highlighting
- Tempo control (50-150 BPM)
- Chord diagrams that update with song progression
- Metal aesthetic (black/red theme)
- Web Audio API integration for basic sound

**🔧 Current Issues**
- Audio quality sounds like Nintendo beeps, not guitar
- Tablature timing might not be 100% accurate to real song
- Only one song implemented (Brain Stew)

## Technology Stack
- **Frontend**: HTML5, CSS3, JavaScript
- **Audio**: Web Audio API
- **Deployment**: Static files on home server
- **Development**: Local Termux environment

## Project Structure
```
brenna-guitar-project/
├── README.md              # This file - project overview
├── DEVELOPMENT.md         # Development process and decisions
├── TODO.md               # Feature roadmap and tasks
├── src/                  # Source code
├── prototypes/           # Working prototypes and experiments
├── assets/               # Static assets
│   ├── audio/           # Guitar samples, song files
│   └── images/          # Icons, backgrounds
├── docs/                # Additional documentation
└── tests/               # Any testing files
```

## Getting Started
1. Clone/copy this project to your development environment
2. Open any `.html` file in the `src/` or `prototypes/` folder
3. Use Python's built-in server for testing: `python -m http.server 8080`
4. Open browser to `localhost:8080`

## Contributing
This is a family project! Ideas and feedback welcome from:
- Brenna (primary user and tester)
- Nigel (project lead and idea generator)
- Claude (development partner)

## License
Family use only - built with love for learning! 🤘

---
*Started: June 2025*  
*Last Updated: June 8, 2025*