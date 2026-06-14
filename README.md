# MammoAI — Breast Cancer Detection System

> ** Academic Prototype Notice:** This system is developed for **educational and research purposes only**. It has not undergone clinical trials or regulatory approval. All predictions are simulated and must **never** be used for real medical decisions.

---

## Overview

**MammoAI** is a front-end demonstration of a deep learning–powered breast cancer detection system. It simulates a Convolutional Neural Network (CNN) inference pipeline for mammographic image analysis, complete with Grad-CAM heatmap visualization and performance analytics.

Built as a single-file web application — no framework, no build step, just open `index.html`.

---

## Features

| Feature | Description |
|---|---|
| **Image Upload** | Drag-and-drop or browse for mammogram/X-ray images (JPEG, PNG, BMP, WebP, DICOM-like) |
| **CNN Pipeline** | Animated 5-step inference simulation: Preprocessing → Conv Extraction → Pooling → Classification → Grad-CAM |
| **Grad-CAM Heatmap** | Simulated gradient-weighted Class Activation Map highlighting suspicious regions |
| **Confidence Scoring** | Probabilistic output with risk stratification (Low / Medium / High) |
| **Performance Analytics** | Live Chart.js graphs — dataset distribution, training/validation accuracy, ROC curve, loss curves, confusion matrix |
| **Diagnostic Results** | Benign/Malignant verdict with feature contribution scores and clinical action advice |
| **Fully Offline** | Single HTML file, zero backend, zero installation required |

---

## Quick Start

### Option 1 — Open directly (simplest)
```bash
# Clone the repo
git clone https://github.com/YOUR_USERNAME/mammogram-ai-diagnosis.git
cd mammogram-ai-diagnosis

# Open in browser
open index.html          # macOS
start index.html         # Windows
xdg-open index.html      # Linux
```

### Option 2 — Serve locally (recommended for best experience)
```bash
# Using Python
python3 -m http.server 8080

# Using Node.js
npx serve .

# Using VS Code
# Install the "Live Server" extension → Right-click index.html → Open with Live Server
```
Then visit `http://localhost:8080` in your browser.

---

## Project Structure

```
mammogram-ai-diagnosis/
│
├── index.html          # Main application (single-file SPA)
├── README.md           # Project documentation
├── LICENSE             # MIT License
├── .gitignore          # Git ignore rules
│
└── assets/             # (reserved for future assets)
```

---

## App Navigation

The app has **6 pages** navigable from the top navbar:

1. **Home** — Hero section with stats and feature overview
2. **Upload** — Drag-and-drop mammogram image uploader with file preview
3. **Analysis** — Animated CNN inference pipeline with real-time step tracking
4. **Results** — Diagnostic verdict, confidence metrics, Grad-CAM heatmaps, feature scores
5. **Data** — Model analytics charts (accuracy, loss, ROC, confusion matrix)
6. **About** — Dataset info, CNN architecture, model performance, and explainability details

---

## 🤖 Simulated AI Pipeline

```
Input Image (224×224 normalized)
        │
        ▼
┌─────────────────────┐
│  Conv Block ×4      │  3×3 kernels · ReLU · BatchNorm
│  (Feature Maps)     │  512 feature maps
└──────────┬──────────┘
           │
           ▼
┌─────────────────────┐
│  Max Pooling ×3     │  2×2 stride
└──────────┬──────────┘
           │
           ▼
┌─────────────────────┐
│  Dense Layers       │  512 → 256 → 64 · Dropout 0.4
└──────────┬──────────┘
           │
           ▼
┌─────────────────────┐
│  Output (Sigmoid)   │  Binary probability → Benign / Malignant
└──────────┬──────────┘
           │
           ▼
    Grad-CAM Heatmap Generation
```

---

## Simulated Model Performance

| Metric | Value |
|---|---|
| Test Accuracy | **97.4%** |
| Precision | **96.9%** |
| Recall | **97.8%** |
| F1 Score | **97.3%** |
| AUC-ROC | **0.9847** |
| 5-fold CV Mean | **96.9% ± 0.4%** |
| Avg. Inference Time | **2.8 seconds** |

---

## Dataset Reference

The simulated model is based on the **CBIS-DDSM** (Curated Breast Imaging Subset of DDSM):

- **Total Images:** 9,736 (5,210 benign · 4,526 malignant)
- **Modality:** Full-field digital mammography (FFDM), CC and MLO views
- **Annotations:** Radiologist-verified ROI bounding boxes and pathology labels
- **Source:** The Cancer Imaging Archive (TCIA) / National Cancer Institute
- **Resolution:** Up to 4,096 × 5,625 px (downsampled to 224×224 for training)

---

## Tech Stack

| Category | Technology |
|---|---|
| Frontend | HTML5, CSS3, Vanilla JavaScript (ES2020) |
| Charts | [Chart.js v4.4.1](https://www.chartjs.org/) |
| Fonts | Syne, Lato, JetBrains Mono (Google Fonts) |
| AI Reference Stack | TensorFlow 2.x, Keras, Python 3.11, CUDA 12.1 |
| Explainability | Grad-CAM (simulated) |

---

## Live Demo

You can deploy this instantly on:

- **GitHub Pages** → Settings → Pages → Source: `main` branch → `/root`
- **Netlify Drop** → Drag the folder to [app.netlify.com/drop](https://app.netlify.com/drop)
- **Vercel** → `vercel deploy`

---

## Contributing

Contributions, issues, and feature requests are welcome!

1. Fork the project
2. Create your feature branch: `git checkout -b feature/AmazingFeature`
3. Commit your changes: `git commit -m 'Add some AmazingFeature'`
4. Push to the branch: `git push origin feature/AmazingFeature`
5. Open a Pull Request

---

## License

Distributed under the MIT License. See [`LICENSE`](LICENSE) for more information.

---

## ⚕️ Medical Disclaimer

This tool is an **educational prototype** only. It does not constitute medical advice, diagnosis, or treatment. Always seek the guidance of a qualified healthcare provider for medical concerns. Never disregard professional medical advice or delay in seeking it because of something produced by this software.

---


