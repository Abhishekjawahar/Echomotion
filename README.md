
# 🎵 EchoMotion

**Turn motion into music.**
EchoMotion is a browser-based audiovisual instrument that transforms real-time movement into expressive sound and generative visuals.

---

## ✨ Overview

EchoMotion bridges the gap between **visual motion** and **musical expression**.
Using blob tracking and intelligent mapping, it converts moving shapes (from camera or video) into harmonically structured sound—creating a playable, interactive art system.

Whether you're an artist, musician, or creative coder, EchoMotion lets you **perform with motion itself**.

---

## 🚀 Features

* 🎥 **Real-time blob tracking**
* 🎵 **Motion → music mapping (pitch, rhythm, dynamics)**
* 🎹 **Scale-quantized sound (musical, not chaotic)**
* ⏱ **Tempo (BPM) synchronization**
* 🔊 **Built-in synth engine (Web Audio API)**
* 🌫 **Trail-based generative visuals**
* ⚡ **Performance presets (Calm / Rhythm / Chaos)**
* 🎹 **MIDI input support**
* ⌨️ **Keyboard controls for live performance**
* 🖥 **Fullscreen performance mode**

---

## 🧠 How It Works

1. **Motion Detection**
   Moving objects are tracked as blobs with position and velocity.

2. **Mapping Layer**

   * X position → Pitch
   * Y position → Tone / brightness
   * Velocity → Volume
   * Blob count → Density

3. **Musical Constraints**

   * Notes are quantized to scales (pentatonic, minor, major)
   * Timing is synced to BPM grid

4. **Sound Engine**
   Synthesized audio is generated in real time using the Web Audio API.

5. **Visual Feedback**
   Motion creates trails and flashes, tightly synced with sound.

---

## 🎛 Controls

### UI Controls

* **BPM** – Controls tempo
* **Scale** – Pentatonic / Minor / Major
* **Volume** – Master audio level
* **Reverb** – Adds spatial depth
* **Trail** – Visual persistence

---

### ⌨️ Keyboard Shortcuts

| Key          | Action                 |
| ------------ | ---------------------- |
| `1`          | Calm preset            |
| `2`          | Rhythm preset          |
| `3`          | Chaos preset           |
| `Space`      | Trigger notes          |
| `UI Button`  | Toggle interface       |
| `Fullscreen` | Enter performance mode |

---

## 🎨 Presets

* **Calm** → Ambient, slow evolving textures
* **Rhythm** → Structured beats and patterns
* **Chaos** → High-energy, dense interactions (still musical)

---

## ▶️ How to Run

1. Clone or download this repository
2. Open `index.html` in a modern browser (Chrome recommended)
3. Allow camera access (if using live input)
4. Click anywhere on screen to enable audio
5. Start moving objects in front of the camera 🎥

---

## 🛠 Tech Stack

* HTML5 Canvas
* JavaScript (Vanilla)
* Web Audio API
* (Optional) MediaDevices API for camera input

---

## 🔌 Input Format (for custom tracking)

If integrating your own blob tracker, use:

```js
blobs = [
  { x: Number, y: Number, v: Number } // v = velocity (optional)
];
```

---

## 🎯 Use Cases

* 🎨 Interactive art installations
* 🎧 Experimental music creation
* 🎥 Live visuals + sound performance
* 🧪 Creative coding experiments
* 🕹 Gesture-based instruments

---

## 🚧 Future Ideas

* Multi-layer synth (bass / lead / pad separation)
* Blob interaction → percussion
* Save / share presets
* WebGL shader-based visuals
* AI-based pose tracking (hands / body)

---

## 📜 License

MIT License — free to use, modify, and share.

---

## 🙌 Acknowledgment

Inspired by the idea of **synesthesia** — experiencing one sense through another.
EchoMotion explores what it means to *hear movement* and *see sound*.

---

## 💡 Final Note

EchoMotion is not just a tool—it's an instrument.
Experiment, perform, and push it into unexpected creative directions.

---
