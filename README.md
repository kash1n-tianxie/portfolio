# 手势控制粒子系统 / Gesture-Controlled Particle System

An interactive 3D particle visualization system controlled by hand gestures via MediaPipe Hands.

## ✨ Features

- **Real-time hand gesture control** powered by MediaPipe Hands
- **Left hand** — Control particle explosion/reconstruction by opening/closing
- **Right hand (open)** — Orbital rotation by tilting wrist direction
- **Right hand (fist)** — Cycle through models
- **1-Euro Filter** — Adaptive low-pass filtering for smooth, low-latency gesture input
- **Cinematic post-processing** — Unreal Bloom via Three.js EffectComposer
- **UV texture sampling** — Particles colored from original model textures
- **Privacy-preserving sensor view** — Only hand skeleton is shown, no raw video

## 🎮 Controls

| Gesture | Action |
|---|---|
| ✋ Left hand open | Explode particles outward |
| ✊ Left hand fist | Reconstruct model |
| 🖐 Right hand open + tilt | Rotate model (orbital) |
| ✊ Right hand fist | Switch to next model |

## 🚀 Live Demo

👉 [Open on GitHub Pages](https://YOUR_USERNAME.github.io/YOUR_REPO_NAME/)

## 🛠 Tech Stack

- [Three.js r128](https://threejs.org/) — 3D rendering & post-processing
- [MediaPipe Hands](https://developers.google.com/mediapipe/solutions/vision/hand_landmarker) — Hand tracking
- [1-Euro Filter](http://cristal.univ-lille.fr/~casiez/1euro/) — Gesture smoothing
- Vanilla HTML / CSS / JavaScript — No build step required

## 📁 Models

Place your `.glb` model files in the root directory:

```
index.html
dog.glb       ← Model 1
model1.glb    ← Model 2
model2.glb    ← Model 3
model3.glb    ← Model 4
```

## ⚡ Run Locally

```bash
# Python 3
python3 -m http.server 8888
# Then open: http://localhost:8888
```

> **Note:** Must be served over HTTP (not file://) for camera access and MediaPipe to work.

## 📄 License

MIT
