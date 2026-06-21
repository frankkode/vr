# Inside the Heart — WebXR Educational Tour

An immersive WebXR experience that lets you explore a beating 3D human heart in your browser. Built with [A-Frame](https://aframe.io), it works on desktop, mobile, and VR headsets.

## Features

- **3D Beating Heart** — A fully rigged, anatomically annotated heart model with real-time cardiac animation
- **Guided 5-Stop Tour** — Explore the four chambers (right atrium, right ventricle, left atrium, left ventricle) plus an overview, each with narrated descriptions and camera fly-throughs
- **Blood Flow Visualization** — Animated particle streams tracing deoxygenated (blue) and oxygenated (red) blood through the heart, lungs, and body
- **Real-Time ECG** — Animated ECG waveform with BPM display and systole/diastole phase indicator
- **Interactive Controls** — Rotate the heart by dragging, pause/slow the heartbeat, toggle transparency (X-ray mode), and mute narration
- **VR Support** — Full WebXR support for compatible headsets with laser controller interaction
- **Quiz Mode** — A 3-question anatomy quiz displayed as an in-scene billboard

## How to Run

The project is a single static HTML file. Serve it with any HTTP server:

```bash
npx serve .
```

Then open `http://localhost:3000` in your browser.

> Some features (speech synthesis, WebXR) may not work when opening the file directly from disk (`file://`). Always use a local server.

## Controls

| Action | Desktop | Mobile/VR |
|--------|---------|-----------|
| Rotate heart | Click + drag | Touch drag / VR controller grab |
| Advance tour | Click "Next" button | Tap "Next" / VR laser click |
| Pause heartbeat | Press Space or click pause button | Tap pause button |
| Toggle slow-motion | Click slow-mo button | Tap slow-mo button |
| Toggle X-ray mode | Click transparency button | Tap transparency button |
| Mute/unmute narration | Click mute button | Tap mute button |
| Take quiz | Click quiz button | Tap quiz button |

## Tech Stack

- [A-Frame 1.5.0](https://aframe.io) — WebXR framework
- [aframe-extras 6.1.1](https://github.com/n5ro/aframe-extras) — animation-mixer for skeletal animation playback
- Web Speech API — narrated tour descriptions
- HTML5 Canvas — real-time ECG rendering

## Credits

- **3D Heart Model**: ["Human Heart Beating - Annotations"](https://sketchfab.com/3d-models/human-heart-beating-annotations-10e9a26f7e004a09bb357d30e4e35f29) by dcpisith, licensed under [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/)
- Built as an educational project demonstrating WebXR for anatomy visualization

## License

Code is unlicensed. The 3D heart model (`models/heart.glb`) is [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/) by dcpisith — see [models/ATTRIBUTION.txt](models/ATTRIBUTION.txt) for details.

## By:Developed by Frank Masabo
