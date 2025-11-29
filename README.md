# Real-Time Object Detection with Depth

Real-time object detection and 3D coordinate extraction using **YOLOv5** and **Intel RealSense D435**, designed as a perception front-end for robotic arm grasping.

---

## Example

![Example Detection](./assets/example_with_count.png)

---
![Example Detection](./assets/example_with_depth.png)

---

## Overview

This project integrates YOLOv5 with the Intel RealSense D435 depth camera to:

- Detect objects in real time from RGB images
- Use the aligned depth map to compute **3D coordinates** of detected targets
- Provide these 3D positions as input for downstream **robotic arm grasping** or other manipulation tasks

---

## Key Features

- 🔍 **Real-time object detection** with YOLOv5  
- 📏 **Depth-aware 3D localization** using Intel RealSense D435  
- 🤖 **Robot-ready output** for grasp planning and control  
- 🧩 Modular design: easy to plug into existing robotics pipelines

---

## Requirements

- Python 3.x  
- PyTorch + YOLOv5 dependencies  
- Intel RealSense SDK (librealsense) and Python bindings (`pyrealsense2`)  
- A connected Intel RealSense D435 camera

---

## Getting Started

### 1. Clone the repository

```bash
git clone https://github.com/WillWu111/Real-Time-Object-Detection-with-Depth.git
cd Real-Time-Object-Detection-with-Depth
```
### 2. Set up the environment

```
conda create -n rt-yolo-depth python=3.10 -y
conda activate rt-yolo-depth
pip install torch torchvision torchaudio --index-url https://download.pytorch.org/whl/cu121
pip install opencv-python numpy pyrealsense2
```

### 3. Usage
```
cd yolo
python predict.py
```
