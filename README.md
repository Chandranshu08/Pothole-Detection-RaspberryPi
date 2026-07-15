# AI-Based Pothole Detection System 🚧

An embedded computer vision system that detects potholes in real time using a Raspberry Pi and a custom-trained YOLOv8 model. Future versions will automatically upload pothole locations to Firebase with GPS coordinates and visualize them on a live map.

---

## Project Status

### ✅ Completed

- Raspberry Pi 4 setup
- SSH remote access
- Python development environment
- Custom YOLOv8n model trained on Kaggle
- Model transferred to Raspberry Pi
- PyTorch + OpenCV configured on Raspberry Pi
- Ultralytics installed
- Successfully loaded trained model on Raspberry Pi

### 🚧 In Progress

- Raspberry Pi Camera integration
- Real-time pothole detection
- Live inference optimization

### 📅 Planned

- GPS integration
- Firebase database
- Live map visualization
- Web dashboard
- Automatic pothole logging
- Confidence filtering
- Offline caching

---

# Hardware

- Raspberry Pi 4 (64-bit)
- Raspberry Pi Camera Module (to be connected)
- GPS Module (planned)

---

# Software Stack

- Python
- YOLOv8n
- PyTorch
- OpenCV
- Ultralytics
- Kaggle (training)
- Raspberry Pi OS / Debian
- Firebase (planned)

---

# Model

Architecture:
- YOLOv8n

Training Platform:
- Kaggle GPU (Tesla T4)

Training Parameters

- Epochs: 100
- Image Size: 640×640
- Batch Size: 16
- Early Stopping Patience: 20

Validation Results

| Metric | Value |
|--------|------:|
| Precision | 0.920 |
| Recall | 0.738 |
| mAP@50 | 0.818 |
| mAP@50-95 | 0.496 |

---

# Development Log

## Day 1

- Set up Raspberry Pi
- Configured SSH over Wi-Fi
- Created project structure
- Created Python virtual environment

---

## Day 2

### Model Training

- Selected Roboflow pothole dataset
- Trained YOLOv8n for 100 epochs on Kaggle GPU
- Saved trained weights (`best.pt`)

### Raspberry Pi Deployment

- Created project directory

```
projects/
└── pothole-detector/
    ├── models/
    ├── scripts/
    ├── data/
    └── outputs/
```

- Transferred trained model to Raspberry Pi using SCP

### Issues Encountered

- Colab GPU quota exhausted
- Switched training workflow to Kaggle
- Incorrect dataset split
- Model download confusion
- PyTorch pip installation attempted to install CUDA packages
- Ran out of storage during installation
- Discovered corrupted dpkg database
- Repaired package manager without reflashing Raspberry Pi
- Installed ARM-compatible PyTorch
- Installed OpenCV
- Installed Ultralytics
- Successfully loaded custom YOLO model on Raspberry Pi

---

# Current Repository Structure

```
pothole-detector/
│
├── models/
│   └── best.pt
│
├── scripts/
│
├── data/
│
├── outputs/
│
└── README.md
```

---

# Next Milestones

- [ ] Connect Raspberry Pi Camera
- [ ] Capture live video
- [ ] Run YOLO inference on camera frames
- [ ] Draw bounding boxes
- [ ] Save detected potholes
- [ ] Read GPS coordinates
- [ ] Upload detections to Firebase
- [ ] Display potholes on map

---

# Goal

Develop a low-cost embedded AI system capable of automatically detecting potholes in real time and creating a crowd-sourced road damage database for smarter road maintenance.
