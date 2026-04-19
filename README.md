# 🚗 Driver Drowsiness Detection System

## 📌 Overview

This project is a real-time driver drowsiness detection system built using **Python, OpenCV, and MediaPipe**.
It monitors eye movements through a webcam and detects fatigue based on the **Eye Aspect Ratio (EAR)**.

The system dynamically calibrates itself to the user's eye characteristics, improving accuracy across different individuals.

---

## 🎯 Features

* 👁️ Real-time eye tracking using **MediaPipe Face Mesh**
* 📊 Eye Aspect Ratio (EAR) based drowsiness detection
* ⚙️ **Dynamic threshold calibration** for personalized detection
* 🔄 EAR smoothing using buffer to reduce noise
* ⏱️ Temporal consistency check to avoid false alarms (blink vs drowsiness)
* 🚀 Frame skipping optimization for better performance
* 📹 Webcam-based live monitoring system

---

## 🧠 How It Works

1. Webcam captures live video frames

2. MediaPipe detects facial landmarks

3. Eye landmarks are extracted

4. EAR (Eye Aspect Ratio) is calculated:

   EAR = (A + B) / (2 × C)

5. System performs:

   * Initial calibration (first few frames)
   * Threshold setting based on user’s average EAR

6. If EAR drops below threshold for continuous frames:
   → Driver is marked as **DROWSY**

---

## 🛠️ Tech Stack

* Python
* OpenCV
* MediaPipe
* SciPy

---

## ⚙️ Installation

```bash
pip install opencv-python mediapipe scipy
```

---

## ▶️ Usage

```bash
python your_script_name.py
```

* Press **Q** to quit the application

---

## 📊 Key Concepts Used

* Computer Vision
* Facial Landmark Detection
* Eye Aspect Ratio (EAR)
* Signal Smoothing
* Real-time Processing Optimization

---

## ⚠️ Limitations

* Performance may vary under:

  * Poor lighting conditions
  * Extreme head angles
  * Occlusions (glasses, hands)
* Depends on webcam quality

---

## 🚀 Future Improvements

* Add alarm/alert system (sound/vibration)
* Mobile or embedded system deployment
* Use deep learning models for higher accuracy
* Multi-face detection support
* Integration with vehicle systems

---

## 📸 Output

* Displays:

  * EAR value
  * Driver status (**AWAKE / DROWSY**)
  * Eye landmark visualization

---

## 👩‍💻 Author

Akshadha Vikraman

---

## ⭐ Acknowledgment

* MediaPipe for face landmark detection
* OpenCV for real-time video processing
