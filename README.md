# Weed Detection with YOLOv8

A quick prototype that detects weeds in agricultural field images using the YOLOv8n (nano) model.

## 📊 Results
Evaluated on a test set of 180 images:

| Metric | Value |
|---|---|
| Precision | 0.60 |
| Recall | 0.53 |
| mAP50 | 0.56 |

## ⚙️ Training Setup
- **Model:** YOLOv8n (pretrained weights)
- **Data:** about 200 training images from Roboflow Universe
- **Epochs:** 10
- **Image size:** 416
- **Hardware:** CPU only

## 🚀 Usage
Install the package with `pip install ultralytics`, then run:

```python
from ultralytics import YOLO

model = YOLO("best.pt")
model.predict("your_image.jpg", save=True, imgsz=416, conf=0.4)
```

## 📈 Next Steps
- Train on the full training set (about 3,600 images)
- Use a GPU to allow more epochs and improve accuracy

## 🗄️ Dataset
- **Name:** Weeds (v3), exported from Roboflow on January 10, 2023
- **Author:** Augmented Startups, via Roboflow Universe
- **License:** [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/)
- **Note:** I used a subset of about 200 training images for this prototype.
