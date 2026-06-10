# 🌊 Interactive Real-Time Fluid Simulation

A GPU-accelerated 2D Navier-Stokes fluid solver running entirely in your browser via WebGL.

## 🚀 Live Demo

Open `index.html` in any modern browser, or [view it on GitHub Pages](https://TMooney27.github.io/fluid-sim).

## 🖱️ Controls

- **Left click + drag** → Push fluid around
- **Right click + drag** → Inject dye only
- **Touch** → Fully supported on mobile/tablet

## 🎛️ Settings & Dials (24+ controls)

| Category | Controls |
|---|---|
| **Physics** | Viscosity, Diffusion, Speed (dt), Grid Resolution (32–512), Jacobi Iterations |
| **Behavior** | Advection on/off, Vorticity Confinement on/off, Curl Strength, Density Decay, Velocity Damping |
| **Brush** | Radius, Force, Dye Intensity, Auto-Splats toggle, Splat Interval |
| **Color** | Hue, Saturation, Luminosity Mix, Color Cycle toggle, Cycle Speed |
| **Visuals** | Pause, Show Grid, Show Velocity Vectors, Vignette, Bloom Intensity |
| **Actions** | Reset Fluid, Randomize all settings |

## 🧪 Solver Pipeline

1. **Advection** — Semi-Lagrangian backtrace with bilinear sampling
2. **Vorticity Confinement** — Re-injects lost curl for swirling detail
3. **Pressure Projection** — Divergence → Jacobi relaxation → gradient subtract (mass conservation)
4. **Display** — HSL color mapping + bloom + vignette + optional grid/vector overlay

## 📂 Files

- `index.html` — Single-file simulation (no build step, no dependencies)

## 🛠️ Made With

- WebGL 1.0
- Vanilla JavaScript
- Navier-Stokes solver on GPU fragment shaders
