# 🚗💤 Driver Drowsiness Detection System

![Driver Drowsiness Detection](https://img.shields.io/badge/Status-Active%20%26%20Stable-brightgreen)  
![License](https://img.shields.io/badge/License-MIT-blue.svg)

---

## 📌 Overview

The **Driver Drowsiness Detection System** is a real-time driver monitoring solution designed to enhance road safety. It detects the driver’s eye status and facial expressions using computer vision techniques to determine if the driver is **Active**, **Drowsy**, or **Sleepy**.

When signs of drowsiness or sleepiness are detected, the system immediately triggers appropriate **siren alerts** and displays visual stickers on the screen, preventing accidents due to fatigue.

---

## 🚀 Key Features

- 🔍 **Real-time Facial Monitoring:** Uses **OpenCV** and **Dlib** to detect eyes and facial landmarks.
- 🟢 **Active Status:** Normal eye behavior; no alerts.
- 🟠 **Drowsy Status:** Short eye closures detected; medium siren plays.
- 🔴 **Sleepy Status:** Prolonged eye closure; loud, urgent siren plays.
- 🎵 **Siren Alerts:** Different audio alerts for drowsy and sleepy states.
- 🖼️ **Visual Stickers:** On-screen status stickers like **Active**, **Drowsy**, and **Sleepy**.
- 💻 **Multithreaded Processing:** Ensures smooth performance using Python's **Threading**.
- ⚙️ **Highly Configurable:** Thresholds & sounds customizable.
- 🛠️ **Fast Execution:** Optimized with **CMake**-built **Dlib** and **Numpy** for fast computation.

---

## 🛠️ Libraries & Technologies Used

| **Library/Tool** | **Purpose**                                      |
|------------------|--------------------------------------------------|
| `OpenCV`         | Video capture, image processing, face detection  |
| `Dlib`           | Facial landmark detection (pre-trained models)   |
| `CMake`          | Building and compiling Dlib dependencies         |
| `Numpy`          | Efficient numerical calculations                 |
| `imutils`        | Simplified image processing functions            |
| `threading`      | Runs sound alerts in separate threads            |
| `playsound / pygame / sounddevice` | Plays siren sounds for alerts  |
| `face_recognition`| Face detection (alternative to dlib)            |

---

## 📂 Installation Steps

1. **Clone the Repository:**

```bash
git clone https://github.com/yourusername/driver-drowsiness-detection.git
cd driver-drowsiness-detection
```

2. **Install Required Libraries:**

```bash
pip install opencv-python dlib numpy imutils face_recognition pygame
```

> **Note:**  
For Dlib installation:
```bash
pip install cmake
pip install dlib
```
Ensure you have CMake installed and configured properly.

3. **Run the Program:**

```bash
python drowsiness_detection.py
```

---

## 📊 System Workflow

| **Status**       | **Condition Detected**                                 | **Action**                                       |
|------------------|------------------------------------------------------|-------------------------------------------------|
| 🟢 **Active**    | Normal open eyes, attentive state                     | No alert; "Active" sticker shown                 |
| 🟠 **Drowsy**    | Eyes closed for short duration (EAR below threshold)  | Medium siren; "Drowsy" sticker displayed        |
| 🔴 **Sleepy**    | Eyes closed for longer duration                       | Loud siren; "Sleepy" sticker displayed          |

---

## 🔔 Sound Alerts Behavior

- **Drowsy State:**
  - Plays medium-volume siren.
  - Display sticker: **Drowsy Status - Stay Alert!**

- **Sleepy State:**
  - Plays high-volume, urgent siren.
  - Display sticker: **Sleepy Status - Immediate Attention Needed!**

Both sounds run using **Python threading**, so real-time detection continues smoothly.

---

## 🎯 Folder Structure Example

```
driver-drowsiness-detection/
├── sounds/
│   ├── drowsy_alert.wav
│   └── sleepy_alert.wav
├── stickers/
│   ├── active.png
│   ├── drowsy.png
│   └── sleepy.png
├── models/
│   └── shape_predictor_68_face_landmarks.dat
├── drowsiness_detection.py
├── requirements.txt
└── README.md
```

---

## 🔥 Future Scope

- Vehicle system integration (automatic braking, vibration seat).
- Mobile app notifications.
- Night mode enhancement.
- Advanced emotion & fatigue recognition.

---

## 📄 License

This project is licensed under the **MIT License**.

---

## 🙏 Acknowledgments

- OpenCV Community
- Dlib & CMake Developers
- Pygame & Numpy Contributors
- Imutils & Face Recognition Libraries

---

## 🚘 **Stay Awake, Drive Safe!**
