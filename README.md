# MOOD — Expression Lab

A static browser app using face-api.js for real face detection and facial-expression classification, with both continuous live webcam analysis and one-photo analysis.

## Run locally (Windows / VS Code)

1. Extract this folder.
2. Open it in VS Code.
3. Install the free **Live Server** extension, or use another local HTTP server.
4. Right-click `index.html` → **Open with Live Server**.
5. Click **Start camera** and grant camera permission, or choose **Choose photo** to select an image.
6. Use **Change visual style** to cycle the artwork treatment, or **Save visual** to download the current generative visual as an SVG.

Do not open the file using `file://` if webcam access is blocked. Use `http://localhost` or HTTPS.

## What runs where

- Webcam frames and selected photos are processed in the browser using face-api.js.
- The Tiny Face Detector and Face Expression model files are downloaded from jsDelivr on first use.
- No backend, API key, account, image upload, or recording feature is included.
- Internet access is needed to load the library and model weights.

## Model output

The model estimates seven facial-expression categories: neutral, happy, sad, angry, fearful, disgusted, and surprised. Its scores are model outputs, not calibrated probabilities and not reliable measurements of a person's internal emotional state. Lighting, head pose, occlusion, cultural differences, and individual differences can affect results.

## Known limitations

- Browser inference performance varies by device.
- CDN/model availability can change; production deployment should pin and self-host reviewed library/model assets with appropriate license notices.
- This prototype is not intended for clinical, hiring, surveillance, identity, or other consequential decisions.
- A production product should add explicit privacy/consent UX, accessibility testing, performance testing, and user validation.
