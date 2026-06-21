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
