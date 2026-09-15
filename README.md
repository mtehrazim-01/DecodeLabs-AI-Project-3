# DecodeLabs-AI-Project-3
# 🔍 AI Project 4 — Basic Text Recognition Using OCR

A Python-based Optical Character Recognition (OCR) project developed as part of the **DecodeLabs AI Project Series**.

This project demonstrates how text can be automatically detected and extracted from an image using **OpenCV** for image preprocessing and **Tesseract OCR** for text recognition.

---

## 📌 Project Overview

The goal of this project is to build a basic OCR pipeline that:

- Takes an image containing text as input
- Preprocesses the image to improve text recognition
- Extracts text using Tesseract OCR
- Calculates word-level confidence scores
- Draws bounding boxes around detected text
- Validates the OCR output using an **80% confidence threshold**
- Saves the processed images and recognized text

---

## 🛠️ Technologies Used

- **Python**
- **OpenCV**
- **Pytesseract**
- **Tesseract OCR**
- **NumPy**
- **Pillow**

---

## ⚙️ OCR Pipeline

The project follows these main steps:

### 1. Input Image
The system receives an image containing readable text.

### 2. Grayscale Conversion
The image is converted from RGB/color format to grayscale.

### 3. Gaussian Blur
Gaussian blurring is applied to reduce noise and improve preprocessing.

### 4. Adaptive Thresholding
Adaptive thresholding separates the text from the background and improves readability.

### 5. OCR Processing
The preprocessed image is passed to **Tesseract OCR** to recognize the text.

### 6. Confidence Calculation
Each detected word is assigned a confidence score.

### 7. Validation
The recognized text is considered successful when the average confidence meets the required **80% threshold**.

### 8. Bounding Boxes
Bounding boxes are drawn around the detected words to visualize the OCR results.

---

## 📂 Project Structure

```text
AI_Project4/
│
├── input/
│   └── sample_text.png
│
├── output/
│   ├── 01_grayscale.png
│   ├── 02_blurred.png
│   ├── 03_adaptive_threshold.png
│   ├── 04_ocr_result.png
│   └── recognized_text.txt
│
├── src/
│   ├── ocr_pipeline.py
│   └── make_sample.py
│
├── docs/
│   └── Project4_Report.md
│
├── requirements.txt
└── README.md
