# 🌊 Interactive Real-Time Fluid Simulation

A single-file, browser-native 2D Navier–Stokes fluid lab that runs with Canvas 2D and vanilla JavaScript. Drag the mouse to push and paint smoke-like fluid, tune the solver live, and switch visualization modes while it runs.

## 🚀 Run It

- Open `index.html` directly in a modern browser, or serve it locally with any static web server.
- GitHub Pages target after Pages is enabled: <https://emooney.github.io/fluid-sim>

## 🖱️ Interaction

- **Left drag**: push the fluid and inject dye.
- **Right drag**: push fluid without dye by default.
- **Touch / pen**: supported via Pointer Events.
- **Space**: pause/resume.
- **R**: reset fluid.
- **H**: hide/show controls.
- **E**: toggle auto emitters.

## 🎛️ Settings & Dials

The control panel includes 35+ live controls:

- **Simulation**: simulation resolution, dye resolution, timestep, substeps, pressure iterations, pressure fade.
- **Physics**: velocity damping, dye persistence, vorticity curl, buoyancy, X/Y gravity.
- **Brush**: radius, push force, dye amount, spray jitter, paint/velocity-only/dye-only/erase modes, right-drag dye toggle.
- **Color**: hue, saturation, brightness, rainbow cycling, velocity color blending.
- **Emitters**: auto emitter toggle, emitter count, emitter strength, orbit radius.
- **Display**: dye/velocity/pressure/curl views, exposure, contrast, glow, glow radius, background lift, vignette, grid overlay, velocity vector dots.
- **Presets**: Seed Plumes, Reset, Silk, Storm, Smoke.

## 🧪 Solver Pipeline

1. **Semi-Lagrangian advection** for velocity and dye.
2. **External forces** for brush splats, gravity, buoyancy, and auto emitters.
3. **Vorticity confinement** to restore swirling detail lost during advection.
4. **Pressure projection** with Jacobi relaxation to keep the velocity field approximately incompressible.
5. **Display shader** with tone mapping, glow, velocity/pressure/curl debug views, grid, and vector-dot overlays.

## 📂 Files

- `index.html` — Single-file WebGL 2 simulation; no dependencies or build step.
- `README.md` — This documentation.

## 🛠️ Tech

- Canvas 2D renderer
- Vanilla JavaScript
- CPU Stable Fluids / Navier–Stokes solver
