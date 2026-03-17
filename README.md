# 🎯 YOLOv5 Object Detection

A real-time object detection project built using **YOLOv5** — one of the most popular and efficient object detection architectures. This project demonstrates end-to-end object detection using a Jupyter Notebook environment, leveraging pretrained YOLOv5 weights on the COCO dataset.

---

## 📌 Project Overview

Object detection is a core computer vision task that identifies and localizes multiple objects within an image or video frame. This project uses **YOLOv5 (You Only Look Once - v5)** by Ultralytics to perform fast and accurate object detection.

| Feature | Detail |
|---|---|
| Model | YOLOv5s (small, pretrained) |
| Dataset | COCO (80 classes) |
| Framework | PyTorch |
| Environment | Jupyter Notebook / Google Colab |
| Task | Object Detection (bounding boxes + labels) |

---

## 🧠 What is YOLO?

**YOLO (You Only Look Once)** is a real-time object detection algorithm that processes an entire image in a single forward pass through a neural network — making it significantly faster than traditional sliding-window or region-proposal methods.

YOLOv5 divides the input image into a grid and simultaneously predicts:
- **Bounding boxes** around detected objects
- **Class labels** for each detected object
- **Confidence scores** for each prediction

---

## 🗂️ Repository Structure

```
yolov5-object-detection/
│
└── yolov5_object_detection.ipynb   # Main notebook with full detection pipeline
```

---

## 🚀 Getting Started

### Prerequisites

```bash
pip install torch torchvision
pip install opencv-python matplotlib
pip install ultralytics   # or clone YOLOv5 repo directly
```

### Clone YOLOv5 (if not using Ultralytics pip package)

```bash
git clone https://github.com/ultralytics/yolov5
cd yolov5
pip install -r requirements.txt
```

### Run the Notebook

1. Open `yolov5_object_detection.ipynb` in Jupyter or Google Colab
2. Run cells sequentially
3. Provide an input image or video path
4. View detection results with bounding boxes and labels

---

## 📷 How It Works

1. **Load Model** — Pretrained YOLOv5s weights loaded via `torch.hub`
2. **Preprocess Input** — Image resized and normalized
3. **Inference** — Single forward pass produces detections
4. **Post-process** — Non-Maximum Suppression (NMS) filters overlapping boxes
5. **Visualize** — Bounding boxes and class labels drawn on output image

```python
import torch

# Load pretrained YOLOv5 model
model = torch.hub.load('ultralytics/yolov5', 'yolov5s', pretrained=True)

# Run inference
results = model('your_image.jpg')
results.show()
```

---

## 🏷️ Detectable Classes (COCO — 80 classes)

Includes: person, car, truck, bus, bicycle, motorbike, dog, cat, bottle, chair, laptop, phone, and 68 more.

---

## 📊 YOLOv5 Model Variants

| Model | Size | mAP@0.5 | Speed (ms) |
|---|---|---|---|
| YOLOv5n | Nano | 28.0 | 6.3 |
| YOLOv5s | Small | 37.4 | 7.2 |
| YOLOv5m | Medium | 45.4 | 8.2 |
| YOLOv5l | Large | 49.0 | 10.1 |
| YOLOv5x | XLarge | 50.7 | 12.1 |

> This project uses **YOLOv5s** — balancing speed and accuracy for demo purposes.

---

## 🛠️ Tech Stack

- **Python 3.x**
- **PyTorch** — Deep learning framework
- **YOLOv5** — Object detection model (Ultralytics)
- **OpenCV** — Image processing
- **Matplotlib** — Visualization
- **Google Colab / Jupyter Notebook** — Development environment

---

## 👤 Author

**Subodh Maheshwari**  
B.Tech CSE-AI | Vivekananda Global University, Jaipur  
Specialization: Artificial Intelligence & Data Science  

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-blue?style=flat&logo=linkedin)](https://www.linkedin.com/in/subodhmaheshwari)
[![GitHub](https://img.shields.io/badge/GitHub-Follow-black?style=flat&logo=github)](https://github.com/subodhmaheshwari5)

---

## 📄 License

This project is open-source and available under the [MIT License](LICENSE).

---

> ⭐ If you found this project helpful, consider giving it a star!
