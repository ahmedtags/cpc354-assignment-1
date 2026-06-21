# CPC354 - Computer Graphics (Assignment 1)

This repository contains the interactive WebGL application implementation and PDF report for **CPC354: Computer Graphics - Assignment 1** (Semester 1, Academic Session 2025/2026) at Universiti Sains Malaysia (USM).

## Course Details
- **Course Code:** CPC354
- **Course Name:** Computer Graphics
- **Semester:** Semester 1, Year 3 (2025/2026)

---

## Assignment Overview

The project is an interactive 2D/3D graphics application built using native WebGL:
- **WebGL Website (`WebGL Website.html`):** Renders interactive geometric objects (including vertices, matrices, colors).
- **Controls & Interaction:** Supports interactive controls for scaling, rotating, translating, and changing colors of the rendered objects in real-time.
- **Underlying Mathematics:** Implements matrix transformation helpers, projections, and shader loading.

---

## What I Did
- Developed the front-end interface and WebGL scene in [`WebGL Website.html`](WebGL%20Website.html).
- Handled vector and matrix math using utility libraries [`MV.js`](MV.js), [`flatten.js`](flatten.js), and shader compilation in [`initShaders.js`](initShaders.js).
- Documented design decisions, layout, transformation matrices, and code description in the group report: [`CPC354_GROUP3DD_REPORT.pdf`](CPC354_GROUP3DD_REPORT.pdf).
- Consolidated the original assignment guideline: [`ASSI1-CPC354.pdf`](ASSI1-CPC354.pdf).

---

## Tools & Tech Stack
- **Languages:** JavaScript, HTML, CSS, GLSL (OpenGL Shading Language)
- **Framework:** Native WebGL API

---

## How to Run

1. Open [`WebGL Website.html`](WebGL%20Website.html) in any modern web browser (Google Chrome, Firefox, Microsoft Edge) supporting WebGL.
2. Interact with the interface controls on the screen (using sliders or keyboard inputs) to manipulate the rendered geometries, adjust transformations (rotation, scaling, translation), and switch palettes.

---

## 📸 Web Interface Output

When running [`WebGL Website.html`](WebGL%20Website.html) in a modern web browser, the interactive application initializes the WebGL canvas and renders a 3D extruded logo with the following elements:

### 1. WebGL Canvas Viewport
- **Size:** `800x600` pixels, rendered on a light gray background with depth testing enabled.
- **Renders:** Extruded 3D models of characters **"C"**, **"A"**, **"R"**, **"T"** with front faces, back faces, and side extrusion panels.
- **Outlines:** Clean black outlines drawn using a dedicated outline shader program with polygon offsets to prevent z-fighting.

### 2. UI Control Dashboard (Side Panel)
- **Word Settings:** Text input to configure the active word (e.g. `CART`, `CAT`, `CAR`).
- **Geometry Controls:** Extrusion depth slider (`0.00` to `0.50`, default `0.15`).
- **Animation Controls:** 
  - Animation speed slider (`0.5x` to `5.0x`, default `2.0x`).
  - Action buttons: `▶ Start/Resume Animation`, `⏸ Stop`, `↻ Reset`.
- **Outline Controls:** Toggle checkbox (`Enable Outlines`) and line thickness slider (`1` to `10` pixels).
- **Color Controls:** Dedicated HTML color pickers for each letter (`Letter 1` to `Letter 4`).

### 3. Integrated Animation State Machine
The TV Ident sequence follows a structured cycle when started:
1. **ROTATE_RIGHT:** Rotate the 3D logo 180° clockwise around the Y-axis.
2. **RETURN_1:** Return to the starting front position.
3. **ROTATE_LEFT:** Rotate 180° counter-clockwise around the Y-axis.
4. **RETURN_2:** Return to the starting position.
5. **SCALE_UP:** Scale up (zoom in) the 3D letters to fill the screen as a final TV transition.

