# AI-Based Pothole Detection System using Raspberry Pi 4

An edge AI system that detects potholes in real-time using a Raspberry Pi 4, Raspberry Pi Camera, and a custom-trained YOLOv8 model. The long-term goal is to store pothole detections in Firebase and visualize them on an interactive map using GPS coordinates.

---

## Project Status

**Current Phase:** Dataset Selection & Model Training

### Completed

- [x] Raspberry Pi 4 headless setup
- [x] Raspberry Pi OS Bookworm (64-bit) installed
- [x] SSH configured and working
- [x] Raspberry Pi connected to Wi-Fi hotspot
- [x] Python environment configured
- [x] OpenCV installed and verified
- [x] Raspberry Pi camera utilities (`rpicam-apps`) installed
- [x] Virtual environment created
- [x] Roboflow dataset selected
- [x] Google Colab training environment configured

### In Progress

- [ ] Train custom YOLOv8n model
- [ ] Evaluate model accuracy
- [ ] Deploy model to Raspberry Pi

### Upcoming

- [ ] Connect Raspberry Pi Camera
- [ ] Live pothole detection
- [ ] Save detection images locally
- [ ] Integrate Firebase
- [ ] Add GPS module
- [ ] Display potholes on interactive map
- [ ] Optimize inference speed

---

# Hardware

- Raspberry Pi 4 Model B (4 GB RAM)
- Raspberry Pi Camera Module (to be connected)
- Official Raspberry Pi Power Adapter
- microSD Card
- Laptop (Linux)
- iPhone Hotspot (used for headless SSH)

---

# Software

## Raspberry Pi

- Raspberry Pi OS Bookworm (64-bit)
- Python 3.11
- OpenCV
- rpicam-apps
- SSH

## Development

- Google Colab
- Ultralytics YOLOv8
- Roboflow
- Git
- GitHub
- VS Code

---

# Project Architecture

```
                 Google Colab
                      │
                      │ Train YOLOv8n
                      ▼
                  best.pt Model
                      │
             Copy via SCP / GitHub
                      │
                      ▼
             Raspberry Pi 4
                      │
             Raspberry Pi Camera
                      │
                      ▼
              YOLO Inference
                      │
          ┌───────────┴───────────┐
          ▼                       ▼
   Save Detection          Firebase (Future)
          │                       │
          └───────────┬───────────┘
                      ▼
              Interactive Map
```

---

# Repository Structure

```
pothole-detection-system/

├── README.md
├── LICENSE
├── .gitignore
├── training/
│   ├── train.ipynb
│   ├── train.py
│   └── dataset.md
│
├── raspberry_pi/
│   ├── src/
│   │   ├── main.py
│   │   ├── detector.py
│   │   ├── camera.py
│   │   ├── firebase.py
│   │   └── gps.py
│   │
│   └── requirements.txt
│
├── models/
│   └── README.md
│
├── docs/
│
└── web_dashboard/
```

---

# Dataset

Current Dataset

- Roboflow Universe
- Pothole Dataset
- Version 17
- Object Detection

Dataset Statistics

- Total Images: **2718**
- Train: **2124**
- Validation: **371**
- Test: **223**
- Classes: **1 (Pothole)**

---

# Model

Framework

- Ultralytics YOLOv8

Model

- **YOLOv8n**

Reason for choosing YOLOv8n

- Lightweight
- Fast inference
- Suitable for Raspberry Pi 4
- Good balance between speed and accuracy

---

# Planned Workflow

```
Road Image
      │
      ▼
Raspberry Pi Camera
      │
      ▼
YOLOv8n Model
      │
      ▼
Pothole Detected
      │
      ▼
Capture Image
      │
      ▼
Store Metadata
      │
      ▼
Firebase
      │
      ▼
Interactive Map
```

---

# Future Features

- GPS integration
- Firebase Cloud Storage
- Firestore Database
- Interactive dashboard
- Heatmap of potholes
- Severity estimation
- Offline detection
- Automatic image upload
- Live video inference
- Web dashboard

---

# Development Timeline

### Phase 1

- Raspberry Pi setup
- Environment setup
- Dataset selection

### Phase 2

- Train YOLOv8n
- Evaluate model

### Phase 3

- Deploy model to Raspberry Pi
- Camera integration

### Phase 4

- Firebase integration

### Phase 5

- GPS integration

### Phase 6

- Interactive map

### Phase 7

- Performance optimization

---

# Current Progress

| Task | Status |
|------|--------|
| Raspberry Pi Setup | ✅ |
| SSH Configuration | ✅ |
| Python Environment | ✅ |
| Camera Setup | ⏳ |
| Dataset Selection | ✅ |
| Model Training | ⏳ |
| Raspberry Pi Inference | ⏳ |
| Firebase | ⏳ |
| GPS | ⏳ |
| Interactive Map | ⏳ |

---

# Author

**Chandranshu Dharmik**

B.Tech Internet of Things Engineering

Final Year Project (Work in Progress)

---

## License

This project is currently under development.