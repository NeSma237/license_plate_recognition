# 📸 License Plate Recognition with YOLOv8

## 🧠 Overview
This project trains a deep learning model to **detect and recognize license plates** in images using the **YOLOv8** architecture.  
It leverages **Roboflow** for dataset management and annotation, and **Ultralytics YOLO** for model training and inference.

---

## 🚀 Features
- ⚡ Uses **YOLOv8n** for fast and lightweight detection  
- 🔗 Integrates with **Roboflow API** to download annotated datasets  
- 🧩 Trains on a custom license plate dataset for **15 epochs**  
- 🎯 Achieves **high accuracy** with *mAP@0.5 ≈ 0.96* and *mAP@0.5–0.95 ≈ 0.69*  
- 💡 Supports **real-time inference** and evaluation  

---

## 🧰 Installation
Install the required dependencies:

```bash
pip install ultralytics roboflow
```
##📦 Dataset

- Source: Roboflow workspace – nesma-4qzxa

- Project: license-plate-recognition-rxg4e-znlxo

- Version: v1

- Format: YOLOv11

🏋️‍♀️ Training
``` from ultralytics import YOLO

model = YOLO("yolov8n.pt")

model.train(
    data="/content/License-Plate-Recognition-1/data.yaml",
    epochs=15,
    imgsz=640,
    batch=8
)
```
