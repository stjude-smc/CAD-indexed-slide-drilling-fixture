# CAD Template

This is a structured template for CAD-based projects, designed for **version control** and **collaboration** using Git.

## Folder Structure

- **cad/** → CAD models (both designed and commercial parts)
  - **parts/mine/** → Your designed parts (`.FCStd`, `.STEP`, etc.)
  - **parts/commercial/** → Purchased parts (with a folder for each part). Includes 3D models, drawings, datasheets, etc.
  - **asm/** → CAD assemblies (`.FCStd`, `.STEP`)

- **bom/** → Bill of materials

- **mfg/** → Manufacturing files
  - **cnc/** → CNC toolpaths and G-code (`.DXF`, `.vcarve`, `.nc`, ...)
  - **3dp/** → 3D printing models (`.STL`, `.preform`, `.3mf`, `.gcode`, ...)
  - **laser/** → Laser cutting files (`.DXF`, `.SVG`, `.PDF`, `.las`)

- **docs/** → Drawings, datasheets, and assembly guides
  - **dwg/** → Drawings for parts and assemblies (`.PDF`)
  - **guides/** → Manufacturing and assembly instructions (`.PDF`)
  - PowerPoint with project description and development history

- **slides/** → Presentations and reports (`.PPTX`)
  - **images** → images you link in `README.md`

- **imgs** → images for `README.md`

## Usage

1. **Use this template** to start a new CAD project:

- Click "Use this template" on GitHub.
- Clone the new repo:

```bash
git clone https://github.com/stjude-smc/new-project.git
```

This way, all your new CAD projects will follow the same structure automatically.

2. **Organize your files:**

- Keep all CAD models in `cad/`
- Store vendor-supplied parts in `cad/parts/commercial/`
- Keep G-code and manufacturing files under `mfg/`
- Maintain proper documentation in `docs/`

3. **Track changes in Git:**

```
git add .
git commit -m "Initial commit"
git push
```

4. **Use [git-flow](https://www.gitkraken.com/learn/git/git-flow)** to clearly separate production and development:

- Iterative development is happening in the `develop` branch
- Big experimental changes happen in `feature` branches
- Once everything is more or less finalized, switch to `release` branch and generate finalized drawings, manufacturing files, and assembly instructions.
- Manufacturing-ready, tested releases go to `main` branch, and get a version number assigned.

This structure ensures that your CAD projects stay organized, making collaboration and manufacturing smoother.
