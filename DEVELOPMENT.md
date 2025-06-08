# 🛠️ Development Log & Decisions

## Development Philosophy
**"Ship fast, iterate faster"** - Build working prototypes quickly, get feedback, improve.

## Technical Decisions

### Why Single HTML File for Prototype?
**Decision**: Start with everything in one file  
**Reasoning**: 
- Faster prototyping
- Easier to test and share
- No build process complexity
- Can refactor to components later once we know what works

**Tradeoffs**: 
- ✅ Quick to build and test
- ❌ Will get messy as features grow
- ❌ Harder to maintain long-term

### Why Web-Based vs Native App?
**Decision**: Web application (HTML/CSS/JS)  
**Reasoning**:
- Works on any device (phone, tablet, desktop)
- No app store approval needed
- Easy to deploy to home server
- Claude can build it quickly
- Easy to iterate and update

### Why Web Audio API vs External Audio Files?
**Decision**: Starting with Web Audio API, moving to real files  
**Reasoning**:
- Web Audio API gives us precise timing control
- Can generate notes programmatically for prototyping
- Real audio files will sound better but harder to sync
- Hybrid approach: use real audio for final product

## Development Timeline

### Session 1 (June 8, 2025)
**Goals**: Build initial prototype  
**Accomplished**:
- Created basic interactive tablature
- Implemented beat highlighting system
- Added tempo control
- Built metal aesthetic
- Basic audio generation working

**Challenges Faced**:
- Audio quality is poor (sounds like video game)
- Tablature accuracy unknown
- Need better audio solution

### Session 1B (June 8, 2025) - MAJOR BREAKTHROUGH! 🔥
**Goals**: Integrate real audio files
**Accomplished**:
- ✅ **REAL AUDIO INTEGRATION WORKING!** - Crystal clear Green Day audio
- Downloaded Brain Stew track using spotdl
- Built comprehensive Web Audio API implementation
- Solved file:// protocol fetch restrictions with HTTP server
- Enhanced error reporting with detailed debugging info
- Created proper project structure with documentation
- Implemented loading progress bars and error handling

**Technical Solutions**:
- Used Python HTTP server to serve files (bypassed browser security)
- Web Audio API for precise audio control
- Fetch API for loading MP3 files with progress tracking
- Real-time audio position tracking and seeking

**Current Status**: 
- ✅ Audio loads and plays perfectly
- ✅ Tempo control working (affects pitch)
- ❌ Timing sync needs calibration (red highlights don't match audio yet)

**Next Session Goals**:
- Fine-tune tablature timing to match real audio
- Calibrate beat timing with actual song structure
- Add more songs once timing system is perfected

## Code Architecture Notes

### Data Structure for Songs
```javascript
const songs = {
  'brain-stew': {
    title: 'Brain Stew',
    artist: 'Green Day',
    tempo: 80,
    chords: ['Em', 'G'],
    tabData: [...], // Array of beat objects
    audioFile: 'path/to/audio.mp3'
  }
}
```

### Beat System
Each beat has timing info and which notes to highlight:
```javascript
const beat = {
  time: 0, // Beat number
  chord: 'Em', // Current chord
  notes: [
    {string: 'E', fret: 0},
    {string: 'A', fret: 2}
  ]
}
```

## Performance Considerations
- Keep audio files small (compress to reasonable quality)
- Optimize for mobile devices (Brenna's phone)
- Minimize JavaScript execution during playback
- Use CSS animations for smooth highlighting

## User Experience Principles
1. **Metal First** - Aesthetic and song choice must appeal to target user
2. **Visual Learning** - Rely heavily on visual cues (colors, movement)
3. **Progressive Difficulty** - Start dead simple, build complexity
4. **Instant Gratification** - User should feel success quickly
5. **Real Music** - Use songs user actually wants to play

## Tools & Libraries Used
- **No external dependencies** (for now) - vanilla HTML/CSS/JS
- **Web Audio API** - built into browsers
- **CSS Grid/Flexbox** - responsive layout
- **Local Storage** - save user progress

## Deployment Strategy
1. **Development**: Local files in Termux
2. **Testing**: Python HTTP server on phone
3. **Staging**: Copy to home server for family testing
4. **Production**: Same as staging (home network only)

## Future Architecture Considerations
When the project grows, consider:
- **Component-based structure** (React/Vue)
- **Build process** (webpack/vite)
- **State management** (for complex interactions)
- **Audio worklets** (for advanced audio processing)

## Lessons Learned
- **Start ugly, make it pretty later** - Functionality first
- **User feedback early** - Brenna's input is crucial
- **Document decisions** - Future you will thank present you
- **Keep scope small** - Don't try to build everything at once

---
*This document should be updated after each development session*