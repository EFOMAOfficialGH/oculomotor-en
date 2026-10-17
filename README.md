# NOTE:This Project is by docramiro / Ramiro Esparza, I only added English language as an option, Original site: github.com/docramiro/oculomotor

# Oculomotor · Cranial Nerve Simulator

A web-based simulator of ocular motility and cranial nerve palsies involving cranial nerves III, IV, and VI.

## Features

- **Interactive 3D face:** Follows a target using the mouse or finger tracking through the camera.
- **Orbital anatomy:** Explore both orbits, with individually isolatable extraocular muscles and nerves.
- **Clinical cases:** Includes clinical scenarios and a diplopia diagnostic algorithm, with support for custom cases.
- **Bilingual interface:** Switch between Spanish and English. The selected language is saved in the browser.

## Getting Started

Open `index.html` or `oculomotor/index.html` in your browser. No installation is required.

**Note:** Camera access requires HTTPS, such as through GitHub Pages or Cloudflare. The 3D graphics and camera features load external libraries from the internet.

For educational use only. This is not a diagnostic tool.

## Third-Party Credits

- **3D face model:** The “Infinite” 3D scan by Lee Perry-Smith of Infinite Realities. Licensed under [Creative Commons Attribution 3.0 (CC BY 3.0)](https://creativecommons.org/licenses/by/3.0/). Distributed with the [three.js examples](https://github.com/mrdoob/three.js). The model was modified by opening the eyelids and adjusting the mesh.
- **three.js:** [MIT License](https://github.com/mrdoob/three.js/blob/dev/LICENSE).
- **MediaPipe Tasks Vision:** [Apache License 2.0](https://www.apache.org/licenses/LICENSE-2.0).
- **IBM Plex:** [SIL Open Font License](https://openfontlicense.org/), distributed through Google Fonts.

## License

The original code and content are released under the **MIT License** (see the `LICENSE` file). You may use, copy, modify, and distribute them, provided that the copyright and license notices are retained.

The 3D face scan remains under the **CC BY 3.0** license and must always be attributed to Lee Perry-Smith.

Third-party assets and libraries remain subject to their respective licenses.

## How to Use

### Online

Open the URL of the published website.

### Run Locally

1. Download the repository by selecting **Code → Download ZIP**.
2. Extract the downloaded archive.
3. Open `oculomotor/index.html` in your browser.

The basic simulator can be opened locally, but the 3D graphics and camera features require an internet connection to load external libraries.

### Modify the Project

Fork the repository and edit the source files.

## Source Code Structure

The `fuente/` directory contains the editable source code. The file `oculomotor/index.html` is generated from these sources.

| File or Directory | Description |
|---|---|
| `fuente/src/a_head.html` | Styles and examination-sheet theme |
| `fuente/src/b_body.html` | Page structure |
| `fuente/src/c_main.js` | Biomechanical model, nerve palsies, clinical cases, diplopia algorithm, and camera |
| `fuente/src/d_three.js` | Three.js 3D visualization of the face, orbits, muscles, and nerves |
| `fuente/src/e_data.js` | Clinical cases, diplopia decision tree, and anatomical reference sheets |
| `fuente/head/` | 3D face processing script (`cut.py`) and mesh (`head.json`) |
| `fuente/assets/` | Face textures |

## Build Instructions

To regenerate the application after editing the source files, run:

```bash
cd fuente
python build.py
```

Requires Python 3. No additional Python dependencies are needed for the build process.

### Reprocess the 3D Face

Install the required dependencies:

```bash
pip install trimesh numpy
```

Then run:

```bash
python head/cut.py LeePerrySmith.glb
```

Run these commands from the appropriate project directory containing the referenced files.

## Language Settings

Use the language selector in the upper-right corner of the simulator to choose **Español** or **English**. Your preference is stored in the browser's `localStorage` and persists when you reopen the application.

---

**Oculomotor Cranial Nerve Simulator** — an educational resource for exploring ocular motility, extraocular muscle anatomy, cranial nerve palsies, and diplopia.
