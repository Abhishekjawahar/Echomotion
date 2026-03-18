# ECHOMOTION

> **Motion-reactive audiovisual instrument — move to make music and visuals.**

ECHOMOTION is a browser-based creative tool that uses your camera to detect motion, translating it in real time into generative music, mathematical visual overlays, and a rhythm engine. Built entirely with vanilla HTML, CSS, and the Web Audio API — no dependencies, no install, just open and play.

---

## ✨ Features

### 🎥 Motion Detection
- Real-time blob tracking via frame-differencing on a half-resolution pipeline for 30+ fps
- Adjustable sensitivity, min/max blob size
- Works with front camera, rear camera, or uploaded video files
- Overlap detection between tracked blobs

### 🎵 Music Engine
- Motion-mapped pitch quantized to musical scales (Pentatonic, Minor, Major, Dorian, Lydian, Whole Tone, Chromatic)
- Additive synthesis voices with stereo panning based on blob X position
- Chord voicings — Root, Dyad, Triad, 7th chord
- Convolution reverb, ping-pong delay, dynamics compressor
- Live chord name display

### 🎛 Base Layer
Six synthesized ambient layers that set the harmonic foundation:
| Layer | Character |
|---|---|
| Drone Pad | Warm detuned sine layers |
| Pulse Bass | Sub-octave LFO pulse synced to BPM |
| Deep Rumble | Low filtered noise texture |
| Crystal Shimmer | High airy detuned overtones |
| Organ Swell | Slow-attack harmonic organ wash |
| Dark Strings | Sawtooth + vibrato bowed texture |

### ♩ Rhythm Engine
- 16-step sequencer with 6 kit components: Kick, Snare, Closed Hi-Hat, Open Hi-Hat, Cymbal, Clap
- 5 built-in preset patterns: Four-on-the-Floor, Hip-Hop, Trap, Breakbeat, Jazz Brush
- Individual kit component toggles — use only the drums you want
- Direct step editing auto-switches to Custom mode
- Motion-reactive ghost hits — blob movement probabilistically fires extra hits
- Dedicated beat master volume, independent of melodic volume
- Lookahead scheduler for sample-accurate, drift-free timing
- All synthesis is pure Web Audio — no sample files required

### ⬡ Mathematical Overlays
Seven real-time visual overlays driven by blob positions:
| Symbol | Overlay | What it does |
|---|---|---|
| ∂Ω | Convex Hull | Smallest polygon enclosing all blobs |
| V(x) | Voronoi | Territory map — which blob "owns" each area |
| ∇F | Force Field | Gravitational attraction arrows toward blobs |
| 𝑥∘𝑦 | Lissajous | Motion trail as oscillating figure |
| △ | Delaunay | Optimal triangulation between blob centres |
| Σeⁱω | Fourier Rings | Expanding ripple rings on direction change |
| ∂u/∂t | Reaction-Diffusion | Turing-pattern organic texture seeded by blobs |

### 🎨 Color Controls
- Per-channel color pickers for every visual element
- 4 curated neon palette presets
- Global overlay alpha and glow intensity sliders

### 📹 Recording
- Record the canvas to WebM video
- Download directly from the browser

---

## 🚀 Getting Started

No build step, no server required.

```bash
# Clone the repo
git clone https://github.com/your-username/echomotion.git

# Open directly in browser
open index.html
```

Or just [open `index.html`](./index.html) directly in any modern browser (Chrome, Edge, Safari, Firefox).

**Permissions required:** Camera access (for live mode). Microphone is never used.

---

## 🛠 Technical Details

- **Zero dependencies** — pure HTML5, CSS3, Web Audio API, Canvas 2D
- **Single file** — entire application is `index.html`
- **Performance optimisations:**
  - Half-resolution motion detection pipeline
  - Separable 1D dilation mask (replaces O(n·r²) naive approach)
  - O(1) BFS queue with index pointer
  - Cached Voronoi canvas (no per-frame allocation)
  - Cached RD ImageData buffer
  - Lookahead audio scheduling (no `setInterval` drift)
  - All `shadowBlur` removed from hot draw path

---

## 🎮 How to Use

1. **Open** `index.html` in your browser and allow camera access
2. **Tap the sound ring** (red pulsing circle) to activate the music engine
3. **Move in front of the camera** — blobs will be detected and mapped to musical notes
4. **Open Math Overlays** to add visual geometry driven by your movement
5. **Open Add Beats** to start the rhythm engine and layer a drum pattern
6. **Open Palette** to customise all colors to your visual style
7. **Hit Record** to capture your performance as a video

---

## 📁 File Structure

```
echomotion/
├── index.html      # Entire application — self-contained
├── README.md       # This file
└── LICENSE         # MIT License
```

---

## Credits

Created by **Abhishek Jawahar**

Built with:
- [Web Audio API](https://developer.mozilla.org/en-US/docs/Web/API/Web_Audio_API)
- [Canvas 2D API](https://developer.mozilla.org/en-US/docs/Web/API/Canvas_API)
- [Share Tech Mono](https://fonts.google.com/specimen/Share+Tech+Mono) & [Rajdhani](https://fonts.google.com/specimen/Rajdhani) via Google Fonts

---

## 📄 License

MIT License © 2026 Abhishek Jawahar — see [LICENSE](./LICENSE) for full text.
