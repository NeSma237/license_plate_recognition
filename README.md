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
## 📦 Dataset

- Source: Roboflow workspace – nesma-4qzxa

- Project: license-plate-recognition-rxg4e-znlxo

- Version: v1

- Format: YOLOv11

## 🏋️‍♀️ Training
```
from ultralytics import YOLO
model = YOLO("yolov8n.pt")

model.train(
    data="/content/License-Plate-Recognition-1/data.yaml",
    epochs=15,
    imgsz=640,
    batch=8
)
```

---

## 📊 Performance
|      Metric      | Value |
| :--------------: | :---: |
|   **Precision**  | 0.981 |
|    **Recall**    | 0.929 |
|    **mAP@0.5**   | 0.966 |
| **mAP@0.5:0.95** | 0.693 |

## 📁 Output

🧠 Trained weights saved to:
```runs/detect/train/weights/best.pt```

📊 Training logs and label plots:
``` runs/detect/train/ ```

## 📌 Notes

- 🚀 Model uses Automatic Mixed Precision (AMP) for faster training

- 🧮 Data augmentation includes blur, grayscale, and CLAHE

- 💻 GPU used: Tesla T4 with CUDA acceleration

## 💬 Acknowledgements

Thanks to Roboflow and Ultralytics for their open-source tools that made this project possible.
##### Made with ❤️ by Nesma.
