# MOOD — Expression Lab

An interactive browser-based experience for real-time facial detection and facial-expression classification, built with **JavaScript and face-api.js**.

MOOD combines browser-based machine learning with generative visuals to explore how facial-expression estimates can drive a visual experience.

## Features

- **Live camera analysis** — continuously analyzes webcam frames for faces and facial expressions.
- **Photo analysis** — select an image to run facial detection and expression classification.
- **Generative visuals** — explore different visual treatments inspired by the model's output.
- **SVG export** — save the current generated visual as an SVG file.
- **Browser-based processing** — webcam frames and selected photos are processed locally in the browser.

## Tech Stack

- HTML
- CSS
- JavaScript
- face-api.js
- Tiny Face Detector
- Face Expression Recognition model

## Run Locally

1. Clone or download this repository.
2. Open the project folder in VS Code.
3. Install the free **Live Server** extension, or start another local HTTP server.
4. Open `index.html` using Live Server.
5. Click **Start camera** and grant camera permission, or select **Choose photo**.
6. Use **Change visual style** to explore the artwork treatments, or **Save visual** to export the current visual as SVG.

Use `http://localhost` or HTTPS rather than opening the page through `file://` if browser permissions prevent camera access.

## How It Works

- The application uses face-api.js to detect faces and estimate facial-expression categories.
- The Tiny Face Detector and Face Expression model weights are loaded from jsDelivr when needed.
- Inference runs in the browser; no application backend or API key is required.
- An internet connection is required to load the JavaScript library and model files.

## Expression Categories

The model estimates seven categories:

`Neutral` · `Happy` · `Sad` · `Angry` · `Fearful` · `Disgusted` · `Surprised`

These outputs are model estimates, not calibrated probabilities or reliable measurements of a person's internal emotional state. Results may vary with lighting, head pose, occlusion, and individual differences.

## Privacy & Responsible Use

- Webcam frames and selected photos are processed in the browser.
- The prototype does not include a backend, image-upload service, or recording feature.
- This project is not intended for clinical diagnosis, hiring decisions, surveillance, identity verification, or other consequential decisions.

## Limitations & Future Improvements

- Inference performance depends on the user's device and browser.
- The application depends on third-party CDN and model availability.
- A production release should review licensing, pin and self-host dependencies where appropriate, and include accessibility, performance, privacy, and consent testing.

## Project Status

A browser-based prototype exploring the intersection of machine learning, interactive design, and generative visual experiences.
