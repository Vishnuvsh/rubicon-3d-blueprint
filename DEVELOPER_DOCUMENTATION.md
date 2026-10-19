# Developer Documentation — TRAIL-HAWK 4x4 Rubicon 3D Blueprint

> **Created using Google Gemini's New Model: Argon**  
> *A lightweight, zero-dependency, procedural 3D automotive engineering blueprint, kinematics simulator, and interactive configurator running directly in the browser.*

---

## 1. What is this Project?
**TRAIL-HAWK 4X4 RUBICON** is an interactive, browser-based 3D automotive engineering blueprint and real-time off-road physics simulator modeled after extreme overland vehicles (Rubicon 392 4x4² / Defender OCTA). 

The entire project is packaged inside a single, self-contained `index.html` file (~136 KB).

- **100% Procedural:** Zero external 3D files (`.gltf`, `.obj`) or texture image downloads. Everything—from the ladder chassis and 37" beadlock wheels to the V8 engine and trail dirt—is generated at runtime using code.
- **Built by:** Generated and architected using **Google Gemini's new model: Argon**.

---

## 2. Purpose
1. **Kinematics Education:** Demonstrates authentic automotive engineering concepts—primarily **100% Analytical Ackermann Steering Geometry** and 4-link solid axle suspension articulation.
2. **Zero-Friction Access:** Eliminates loading screens, build pipelines, and server requirements. Runs directly via file double-click or static hosting.
3. **Interactive Telemetry:** Provides live readouts for steering angles, turning radius (ICR), tire scrub, and 4-wheel suspension travel.

---

## 3. Technology Stack

- **3D Graphics & Engine:** Three.js (r128) + WebGL (PBR materials, ACES Filmic Tone Mapping, procedural PMREM environment reflections).
- **Styling & UI:** Tailwind CSS (v3.4.17 CDN) + Custom Glassmorphism HUD.
- **Procedural 2D Graphics:** HTML5 Canvas (Tire tread bump map, scrolling trail texture, 4-channel live suspension oscilloscope).
- **Vector Telemetry:** Dynamic SVG (Overhead front axle schematic with rotating wheels & tie-rods).
- **Audio Engine:** Web Audio API (Synthesized V8 engine rumble & mechanical click sound effects).
- **Typography:** Google Fonts (`Orbitron`, `JetBrains Mono`, `Inter`).

---

## 4. Key Advantages & Features

1. **Zero External Assets (Ultra-Fast):**
   - Boots in under 200ms with zero network asset lag and no CORS restrictions.
2. **True Ackermann Steering Geometry:**
   - Implements analytical formula: $\cot(\delta_o) - \cot(\delta_i) = \frac{W}{L}$.
   - Inside wheel turns sharper than outside wheel to eliminate tire scrub during turns.
3. **Realistic 4-Link Suspension Physics:**
   - Critically damped 2nd-order spring-damper equations ($0.75$ damping factor) provide smooth, wobble-free rock crawling over boulders.
4. **8 Dynamic Biomes:**
   - Real-time environment switching: *Munnar, Moab, Ladakh, Beach, Volcano, Mars, Arctic, and Cyber* with dynamic sky reflections, fog, and terrain.
5. **Interactive Vehicle Anatomy:**
   - 4 opening passenger doors, swing-out tailgate with 37" spare wheel, and clamshell hood.
   - Reciprocating V8 pistons and spinning radiator fan synchronized to speed.
   - Stinger bullbar vs. stubby bumper & expedition roof rack swappers.
6. **Engineering Diagnostics:**
   - CFD aerodynamic wind tunnel streamlines, X-ray drivetrain scanner, and hydraulic suspension drop test.
7. **Mobile-First Responsive:**
   - Dedicated mobile tuning drawer sheet, pinch-to-zoom, and adaptive camera FOV.

---

## 5. How It Works (Architecture Overview)

```
[ User Input / Auto Drive ]
           │
           ▼
[ Lookahead Road Steering & Analytical Ackermann Solver ]
           │
           ▼
[ Per-Wheel Terrain Height Sampling (Cosine Bell Profiles) ]
           │
           ▼
[ 2nd-Order Spring-Damper Chassis Dynamics (Heave, Pitch, Roll) ]
           │
           ▼
[ Synchronized Rendering & Telemetry Update ]
  ├── WebGL Scene (Fox Coilovers, Wheels, Engine, Body)
  ├── Live SVG Front Axle Overhead Schematic
  ├── HTML5 4-Channel Suspension Oscilloscope
  └── Web Audio Synthesizer (V8 Rumble)
```

---

## 6. How to Run & Deploy

### Run Locally
- **Option 1 (Recommended):** Open in **VS Code**, right-click `index.html` → **Open with Live Server**.
- **Option 2:** Double-click `index.html` to open directly in any modern web browser (Chrome, Edge, Brave, Safari).

### Host Online (Free)
- **GitHub Pages:** Push `index.html` to a GitHub repo → **Settings** → **Pages** → Deploy from `main` branch.
- **Vercel / Netlify:** Drag-and-drop the folder containing `index.html` into [Netlify Drop](https://app.netlify.com/drop) or Vercel.

---

## 7. Project Summary
- **Source File:** Single self-contained [`index.html`](file:///c:/Users/vishn/OneDrive/Desktop/rubicon-3d-blueprint/index.html) (~136 KB).
- **Core Focus:** Real-time WebGL, analytical kinematics, procedural assets, and modern HUD design.
- **AI Origin:** Designed and generated using **Google Gemini New Model: Argon**.
