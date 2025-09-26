# Aadhaar Masker — YOLOv8 + Tesseract + FastAPI

**Aadhaar Masker** is a FastAPI-based service that detects Aadhaar numbers in images using YOLOv8 and Tesseract OCR, then securely blurs and masks them (keeping only the last 4 digits). It includes REST endpoints for direct image masking and debugging, designed for quick deployment from a Colab notebook.

> ⚠️ **Privacy Note:** Aadhaar numbers are highly sensitive. Use this tool only with authorized data and do not expose real Aadhaar images or tokens in public repositories.

---

## Features
- YOLOv8 object detection to locate Aadhaar number regions in images.
- Tesseract OCR to extract digits and decide which number to mask.
- Strong blur inside detected regions with masked overlay (e.g. `XXXX XXXX 1234`).
- FastAPI endpoints:
  - `POST /predict` → returns masked PNG image.
  - `POST /predict_debug` → returns detections, OCR text, and base64 masked image for debugging.
- Works directly from a Colab notebook or can be run locally.

---

## Installation
1. Clone this repository.
2. Install Python requirements:
   ```bash
   pip install -r requirements.txt
