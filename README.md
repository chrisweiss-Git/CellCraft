
# Diamond Precision — Robot Cell Designer (Prototype)

This is a self-contained, static web prototype you can open in a browser. It demonstrates:

- A **Cell Config Wizard** to enter assumptions
- A **2D layout planner** with reach checks and auto-placement
- A **3D simulator** (simplified) showing the robot service sequence (infeed → CNC → blow-off → vision → good/scrap)

## How to use

1. **Download and unzip** this project.
2. Open `index.html` in Chrome, Edge, or Firefox. (For best results, serve via a local HTTP server: `python3 -m http.server 8080` and open `http://localhost:8080`).
3. Visit **Cell Wizard** to adjust assumptions, then **2D Layout** to arrange the cell, then **3D Simulator** to play the animation.

> The Wizard's **Save** button downloads `data/sample_cell_config.json`. You can place that file into the `/data` folder to persist it for later.

## Deploying a public link

- **Vercel** (recommended):
  1. Create a new project from this folder.
  2. Framework: *Other* (static). 
  3. Build command: *None*; Output: `/`.
  4. Deploy → you get a public URL.
- **GitHub Pages**: Commit the folder to a repo → Settings → Pages → Deploy from `main` root.

## Notes

- Geometry and kinematics are abstract for speed. Production will use brand-accurate models, collision checking, discrete-event timing, and code generation.
- Three.js is loaded from a CDN. Ensure you have internet connectivity when viewing `simulator.html`.

## License
Prototype for internal evaluation by Diamond Precision Manufacturing (Saelens Corp). All rights reserved.
