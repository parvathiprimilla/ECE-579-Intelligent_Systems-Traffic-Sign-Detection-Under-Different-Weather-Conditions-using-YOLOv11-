# ECE 579 – Intelligent Systems  
## Traffic Sign Detection Under Different Weather Conditions using YOLOv11

This repository contains code and materials for a **Traffic Sign Detection** project completed as part of **ECE 579 – Intelligent Systems**, a university course.

---

## Project Context

This repository is a **fork of the original project repository** created for a **group-based university course project**.  
It is maintained here **for academic reference, personal learning, experimentation, and portfolio purposes**.

All original authorship, credit and license from the upstream repository are fully preserved.

---

## Traffic Sign Detection Under Different Weather Conditions

This project focuses on detecting traffic signs in diverse weather conditions using the **YOLOv11** object detection architecture. The primary goal is to evaluate the robustness and accuracy of YOLOv11 when trained and tested on datasets containing weather variations like rain, fog, snow, and night conditions.

Key capabilities include:
- Object detection using YOLOv11 architecture
- Weather-augmented dataset training
- Performance evaluation across multiple weather scenarios
- Custom augmentation pipeline for improved robustness
- Real-time inference on challenging visual environments

---

## 👥 Team Contributions

This project was completed as a collaborative university course effort.  
Individual contributions are listed below for clarity and transparency.

### **Parvathi Primilla**
🔧 **Technical Contributions:**
- Developed and implemented **custom data augmentation pipelines** to simulate diverse weather conditions (rain, fog, snow, night)
- Conducted comprehensive **model evaluation and performance analysis** across different weather scenarios
- Performed **hyperparameter tuning and optimization** to improve detection accuracy
- Analyzed **per-class average precision (AP)** and identified challenging scenarios for low-contrast signs
- Generated **evaluation metrics and visualizations** including mAP@0.5, precision, and recall

👥 **Project Impact:**  
This project provided hands-on experience in applying deep learning object detection techniques to real-world challenging scenarios. My work emphasized data quality, augmentation strategies, and rigorous evaluation to ensure model robustness under adverse conditions.  
This fork is maintained to support experimentation, learning, and portfolio demonstration.

---

### **Hemanth Katikala Muniraj**
🔧 **Technical Contributions:**
- Led **dataset collection and preprocessing** for traffic sign images
- Configured and trained the **YOLOv11 model** with custom parameters
- Set up the **training pipeline** using PyTorch and Ultralytics framework
- Implemented **inference scripts** for real-time detection
- Integrated **OpenCV** for image processing and visualization

---

## 🧠 Overview
- **Course:** ECE 579 - Intelligent Systems
- **Model:** YOLOv11
- **Task:** Object Detection (Traffic Sign Detection)
- **Dataset:** Augmented traffic sign dataset with multiple weather conditions
- **Framework:** PyTorch + OpenCV + Ultralytics YOLO
- **Goal:** Improve and evaluate detection accuracy under challenging visual environments

---

## 📁 Project Structure
```
Traffic Sign Detection/
├── Night/                   # Night condition test images
├── Normal/                  # Normal weather test images
├── Rain/                    # Rainy condition test images
├── Snow/                    # Snowy condition test images
├── scripts/                 # Training and inference scripts
├── data/                    # Dataset and configuration files
└── results/                 # Evaluation results and metrics
```

---

## ⚙️ Installation

Make sure you have Python 3.8+ installed.


### Create a virtual environment 
```bash
python -m venv venv
source venv/bin/activate  
# On Windows: venv\Scripts\activate
```

### Install dependencies
```bash
pip install -r requirements.txt
```

---

## 🚀 Usage

### 1. Train the model
```bash
python scripts/train.py --data data/dataset.yaml --cfg yolov11.yaml --weights '' --epochs 50
```

### 2. Run inference
```bash
python scripts/detect.py --weights runs/weights/best.pt --source data/test/images
```

---

## 📊 Evaluation

Evaluation metrics include:
- **mAP@0.5** (Mean Average Precision at IoU threshold 0.5)
- **Precision and Recall** across all classes
- **Per-class Average Precision (AP)** under different weather conditions
- Results are saved in the `results/` directory

---

## 📈 Key Results

- **High detection accuracy** in normal weather conditions
- **Slight performance drops** in rain/night scenarios, particularly for low-contrast signs
- **Custom augmentation pipeline** proved critical to improving model robustness across diverse conditions
- Model maintains reasonable performance even under challenging visual environments

---

## 🧪 Dataset

The dataset used includes traffic sign images augmented with synthetic weather effects (rain, fog, snow, night) to simulate real-world driving scenarios under adverse conditions.  
Dataset annotations follow **YOLO format** (class, x_center, y_center, width, height).

---

## 🧰 Dependencies

- Python 3.8+
- PyTorch
- OpenCV
- Ultralytics YOLOv11
- Albumentations

Install all dependencies using:
```bash
pip install -r requirements.txt
```

---

## 📌 Acknowledgements

- [Ultralytics YOLO](https://github.com/ultralytics/ultralytics)
- OpenCV
- Albumentations

---

## 🔗 Original Repository

This is a **fork of the original project repository** by Hemanth Katikala Muniraj:  
[Original Repository](https://github.com/Hemanth-Katikala-Muniraj/Traffic-Sign-Detection-Under-Different-Weather-Conditions-using-YOLOv11-)

---

## Usage & Attribution

This repository is shared **for academic reference, personal learning, and portfolio demonstration purposes only**.

The project was developed as part of a collaborative university course effort.  
All original credit and authorship are acknowledged.  
No claim of sole ownership is made.

If you are a student or researcher interested in similar work, please use this repository as a **reference** rather than a redistributable software package.

---

## 📃 License

This project is licensed under the MIT License.
