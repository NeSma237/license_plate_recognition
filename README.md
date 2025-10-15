# license_plate_recognition
Train a YOLOv8 model to detect and recognize license plates using a custom Roboflow dataset. Achieves high accuracy with fast inference, suitable for real-time applications. Easy setup with Python and Ultralytics YOLO

## License Plate Recognition with YOLOv8

This project trains a YOLOv8 model to detect and recognize license plates using a custom dataset from Roboflow. It achieves high accuracy with fast inference, supporting real-time applications. Easy to install and train with Python and Ultralytics YOLO.

### Features
Uses YOLOv8n for fast and lightweight detection.

Integrates with Roboflow API to download annotated datasets.

Trains on custom license plate dataset for 15 epochs.

Achieves high accuracy with mAP50 ≈ 0.96 and mAP50-95 ≈ 0.69.

Supports real-time inference and evaluation.
🧰 Installation

pip install ultralytics roboflow

📦 Dataset

Source: Roboflow workspace nesma-4qzxa

Project: license-plate-recognition-rxg4e-znlxo

Version: v1

Format: YOLOv11

🏋️‍♀️ Training

from ultralytics import YOLO

model = YOLO("yolov8n.pt")
model.train(
    data="/content/License-Plate-Recognition-1/data.yaml",
    epochs=15,
    imgsz=640,
    batch=8
)

📊 Performance

Metric

Value

Precision

0.981

Recall

0.929

mAP@0.5

0.966

mAP@0.5:0.95

0.693

📁 Output

Trained weights saved to: runs/detect/train/weights/best.pt

Training logs and label plots saved in runs/detect/train/

📌 Notes

Model uses Automatic Mixed Precision (AMP) for faster training.

Data augmentation includes blur, grayscale, and CLAHE.

GPU used: Tesla T4 with CUDA acceleration.
