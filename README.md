# Automatic License Plate Recognition 

An end-to-end **Automatic License Plate Recognition** pipeline built using a custom-trained **YOLOv8** model for license plate detection and **EasyOCR** for text extraction.

> Achieved **99.5% mAP50 during validation** using a lightweight YOLOv8n backbone.

---

## Demo

**Input → Detection → OCR Output**

```
Input Image → YOLOv8 Detection → Bounding Box Crop → EasyOCR → "MH12JC2813"
```

---

## Features

* Custom-trained YOLOv8 license plate detector
* EasyOCR for text extraction from cropped license plates
* End-to-end Automatic License Plate Recognition pipeline
* Lightweight and fast using YOLOv8n
* Supports inference on custom vehicle images
* High-accuracy license plate localization

---

## Model Performance

Trained for **30 epochs** on a custom dataset using **640 × 640** image resolution.

| Metric    | Score     |
| --------- | --------- |
| Precision | **99.3%** |
| Recall    | **99.1%** |
| mAP@50    | **99.5%** |
| mAP@50-95 | **86.5%** |

> The high mAP@50 score indicates strong license plate localization performance.

---

## Technologies Used

| Tool                 | Purpose                       |
| -------------------- | ----------------------------- |
| Python               | Core programming language     |
| YOLOv8 (Ultralytics) | License plate detection       |
| OpenCV               | Image processing and cropping |
| EasyOCR              | Text recognition              |
| Matplotlib           | Visualization                 |

---

## Training Configuration

| Parameter  | Value            |
| ---------- | ---------------- |
| Base Model | YOLOv8n          |
| Epochs     | 30               |
| Batch Size | 16               |
| Image Size | 640 × 640        |
| Task       | Object Detection |

---

## Pipeline Workflow

```
Input Image
      │
      ▼
YOLOv8 License Plate Detection
      │
      ▼
Bounding Box Extraction
      │
      ▼
Plate Cropping
      │
      ▼
OCR using EasyOCR
      │
      ▼
Extracted License Plate Text
```

---

## Getting Started

1. Open the notebook:

```text
license_plate_detection_ocr.ipynb
```

2. Install the required libraries:

```bash
pip install ultralytics easyocr opencv-python matplotlib
```

3. Load the trained YOLOv8 model (`best.pt`) and run inference on custom vehicle images.

4. The notebook demonstrates the complete pipeline:

* License plate detection using YOLOv8
* Bounding box extraction
* Plate cropping
* OCR-based text extraction using EasyOCR

---

## Project Structure

```
license-plate-detection-yolov8-easyocr/
│
├── models/
│   └── best.pt
│
├── license_plate_detection_ocr.ipynb
├── README.md
```

---

## About

This project was built to explore real-world computer vision applications using deep learning. The complete pipeline from dataset preparation and model training to OCR integration was implemented independently.
