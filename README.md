# 🚶‍♂️ Real-Time People Counting using YOLOv11 + NVIDIA DeepStream + nvdsanalytics

## 📘 Overview
This project implements an **AI-powered people counting system** using **YOLOv11** integrated with **NVIDIA DeepStream SDK**.  
The system uses **line-crossing analytics** to count people entering and exiting a specific region in a video or live camera stream.

By combining YOLOv11’s detection accuracy and DeepStream’s high-performance video pipeline, this solution can handle **real-time analytics** on multiple video streams with **GPU acceleration**.

---

## 🧭 Project Scope

### 🎯 Objectives
- Detect **people** from live or recorded video streams using **YOLOv11**.
- Count **entries and exits** based on **line-crossing logic**.
- Display analytics results (counts, bounding boxes, tracking IDs) on the output video.
- Build a scalable DeepStream pipeline for **edge AI and smart surveillance** applications.

### 🧩 Applications
- 🏢 In temples and heritage building — monitoring crowd movement.
- 🛍️ Retail Analytics — customer flow tracking.
- 🏫 Campus Safety — entry/exit tracking.
- 🚇 Transportation Hubs — crowd management.
- 🚗 Parking or toll booth monitoring.

---

## ⚙️ System Architecture

![Flowchart illustrating the process](assets/DeepStream.png "Deepstream Flowchart")


Each block represents a **DeepStream plugin** that performs a specific role:
- `nvinfer`: runs YOLOv11 for object detection.
- `nvtracker`: assigns tracking IDs.
- `nvdsanalytics`: defines ROI and line-crossing zones.
- `nvdsosd`: overlays results on screen.

---

## 🧰 Prerequisites

Before running this project, make sure you have:

### ✅ Hardware
- NVIDIA GPU (dGPU or Jetson platform)
- Minimum 4 GB VRAM

### ✅ Software
| Component | Version |
|------------|----------|
| Ubuntu | 22.04 |
| Python | ≥ 3.10 |
| NVIDIA Drivers | Compatible with CUDA 12+ |
| CUDA Toolkit | 12.x |
| DeepStream SDK | ≥ 7.1 |
| TensorRT | Included with DeepStream |
| PyDS | Properly built & installed |

---

## 🚀 How to Use
🧩 Step 1: Clone or Copy the Repository
```
git clone https://github.com/mithunbs05/Crowd-Management.git
```

Step 2: Access it from DashBoard

---

### 🧩 Future Enhancements

- Add multiple camera stream support
- Save data to CSV / Database
- Add a web dashboard for real-time analytics
- Integrate MQTT or Kafka for IoT deployment
- Implement heatmap generation for movement analysis

### 🧩 Summary

This project demonstrates the integration of YOLOv11 and DeepStream SDK for edge-level, real-time people counting.
It’s a strong foundation for developing smart surveillance and analytics systems that combine deep learning with GPU-accelerated inference.
