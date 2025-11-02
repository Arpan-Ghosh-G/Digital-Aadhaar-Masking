# Aadhaar Masker — YOLOv8 + Tesseract + FastAPI

<p align="center">
  <img src="demo_aadhaar_masking.png" alt="Aadhaar Masking Demo" width="600"/>
</p>

**Aadhaar Masker** is a FastAPI-based service that detects Aadhaar numbers in images using a **pre-trained YOLOv8 Aadhaar number detection model** and Tesseract OCR, then securely blurs and masks them (keeping only the last 4 digits). It includes REST endpoints for direct image masking and debugging, designed for quick deployment from a Colab notebook.

> ⚠️ **Privacy & Legal Note:** Aadhaar numbers are highly sensitive personal data. Use this tool only with authorized data and do not expose real Aadhaar images or tokens in public repositories.

---

## 📂 Project Media & Resources
All demo **videos**, **images**, and **related assets** used for testing or demonstrations are available here:  
👉 [Google Drive Folder — AADHAAR MASKING DEMO](https://drive.google.com/drive/folders/1szpD9fldYu59KfEU3MuxUp4LgQPPwx4Y?usp=drive_link)

---

## ✨ Features
- **Pre-trained YOLOv8 model** specifically for detecting Aadhaar number regions in images.
- **Tesseract OCR** to extract digits and decide which number to mask.
- **Strong blur** inside detected regions with masked overlay (e.g. `XXXX XXXX 1234`).
- **FastAPI endpoints:**
  - `POST /predict` → returns masked PNG image.
  - `POST /predict_debug` → returns detections, OCR text, and base64 masked image for debugging.
- Works directly from a **Colab notebook** or can be **run locally**.

---

## 🛠 Installation
1. Clone this repository:
   ```bash
   git clone https://github.com/Arpan-Ghosh-G/Digital-Aadhaar-Masking.git
   cd Digital-Aadhaar-Masking
