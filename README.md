# 🚀 IoT Smart Radar Tracker

An IoT-based **object tracking system** designed for real-time surveillance and automatic target tracking.

The system combines **Arduino hardware** with **Python Computer Vision** to detect and track objects in real time. An **HC-SR04 ultrasonic sensor** performs 180° scanning, while a **Pan-Tilt mechanism** controlled by two servo motors enables two-axis target movement.

---

## 🎯 Project Overview

The **Smart Radar System** is a team-based IoT project that combines:

* 📡 Ultrasonic sensing
* 👁️ Computer Vision
* 🔄 180° radar scanning
* 🎯 Pan-Tilt target tracking
* 💻 Python-based processing
* 🔌 Arduino-Python serial communication
* 🔊 Alert system

When an object is detected, the system processes the available sensor and camera information and automatically controls the Pan-Tilt mechanism toward the target.

The system also includes a **laser diode** for visual pointing and a **buzzer** for alerts.

---

## 💡 Problem & Solution

### Problem

Real-time surveillance and object tracking can require continuous human monitoring and manual control.

### Solution

This project provides an automated tracking system that combines an ultrasonic radar mechanism with Computer Vision and Arduino-based hardware control.

The system can:

* Scan the surrounding area across **180°**.
* Measure the distance of detected objects.
* Process camera input using Computer Vision.
* Automatically control a **two-axis Pan-Tilt mechanism**.
* Track detected targets.
* Provide visual and audio alerts.
* Display the system response in real time.

---

## ⚙️ How It Works

The system consists of two main components: **Arduino Hardware** and a **Python Computer Vision Application**.

### 🔌 Arduino Hardware

The Arduino UNO R4 Minima is responsible for the hardware control layer.

It handles:

* HC-SR04 ultrasonic distance measurement.
* 180° scanning.
* Pan and Tilt servo control.
* Buzzer activation.
* Laser activation.
* Serial communication with the Python application.

### 🧠 Python Computer Vision

The Python application handles the Computer Vision side of the project.

It uses:

* **MediaPipe**
* **OpenCV-Contrib-Python**
* **NumPy**

The Python application processes camera input, performs object detection/tracking, and communicates with the Arduino through **PySerial**.

---

## 🔄 System Workflow

```text
                         ┌─────────────────┐
                         │     Camera      │
                         └────────┬────────┘
                                  │
                                  ▼
                    ┌────────────────────────┐
                    │ Python Computer Vision │
                    │                        │
                    │ MediaPipe              │
                    │ OpenCV-Contrib-Python  │
                    │ NumPy                  │
                    └───────────┬────────────┘
                                │
                                │ PySerial
                                ▼
                    ┌────────────────────────┐
                    │     Arduino UNO R4     │
                    │        Minima          │
                    └───────────┬────────────┘
                                │
               ┌────────────────┼────────────────┐
               │                │                │
               ▼                ▼                ▼
        ┌────────────┐   ┌──────────────┐   ┌─────────┐
        │  HC-SR04   │   │  Pan-Tilt    │   │ Buzzer  │
        │  Ultrasonic│   │   Servos     │   │         │
        │   Sensor   │   │              │   └─────────┘
        └────────────┘   └──────────────┘
                                │
                                ▼
                         ┌─────────────┐
                         │ Laser Diode │
                         └─────────────┘
```

---

## ✨ Key Features

* 🔄 **180° Radar Scanning**
* 👁️ **Real-Time Computer Vision**
* 🎯 **Object Detection & Tracking**
* 📏 **Ultrasonic Distance Measurement**
* 🔧 **Two-Axis Pan-Tilt Movement**
* 🔊 **Buzzer Alerts**
* 🔴 **Laser Pointing Mechanism**
* 💻 **Real-Time Computer Interface**
* 🔌 **Arduino ↔ Python Serial Communication**
* ⚡ **Integrated IoT + Computer Vision System**

---

## 🛠️ Tech Stack

### 💻 Software

| Technology                | Purpose                                |
| ------------------------- | -------------------------------------- |
| **Python**                | Computer Vision and system integration |
| **MediaPipe**             | Computer Vision and tracking           |
| **OpenCV-Contrib-Python** | Image and video processing             |
| **NumPy**                 | Numerical and array processing         |
| **PySerial**              | Arduino ↔ Python serial communication  |
| **Arduino IDE**           | Arduino development                    |
| **C++**                   | Arduino hardware control               |

### 🔌 Hardware

| Component                 | Purpose                                            |
| ------------------------- | -------------------------------------------------- |
| **Arduino UNO R4 Minima** | Main microcontroller                               |
| **HC-SR04**               | Ultrasonic distance measurement and radar scanning |
| **2× Servo Motors**       | Pan-Tilt two-axis movement                         |
| **Camera**                | Real-time visual input                             |
| **Laser Diode**           | Visual pointing mechanism                          |
| **Buzzer**                | Audio alerts                                       |
| **Breadboard**            | Circuit assembly and power distribution            |
| **Jumper Wires**          | Hardware connections                               |

---

## 🔌 Circuit Connections

### HC-SR04 Ultrasonic Sensor

| Connection | Arduino |
| ---------- | ------- |
| VCC        | 5V      |
| GND        | GND     |
| TRIG       | Pin 4   |
| ECHO       | Pin 5   |

### Laser Module

| Connection | Arduino |
| ---------- | ------- |
| Positive   | Pin 7   |
| Negative   | GND     |

### Pan Servo

| Connection | Arduino |
| ---------- | ------- |
| Signal     | Pin 9   |
| Power      | 5V      |
| Ground     | GND     |

### Tilt Servo

| Connection | Arduino |
| ---------- | ------- |
| Signal     | Pin 10  |
| Power      | 5V      |
| Ground     | GND     |

### Buzzer

| Connection | Arduino |
| ---------- | ------- |
| Positive   | Pin 6   |
| Negative   | GND     |

---

## 🏗️ System Architecture

The project uses a hybrid **IoT + Embedded Systems + Computer Vision** architecture.

```text
        ┌──────────────────┐
        │      Camera      │
        └────────┬─────────┘
                 │
                 ▼
      ┌──────────────────────┐
      │  Python Application   │
      │                      │
      │  MediaPipe           │
      │  OpenCV-Contrib      │
      │  NumPy               │
      │  Tracking            │
      └──────────┬───────────┘
                 │
                 │ PySerial
                 ▼
      ┌──────────────────────┐
      │    Arduino UNO R4    │
      │       Minima         │
      └──────────┬───────────┘
                 │
       ┌─────────┼─────────┐
       │         │         │
       ▼         ▼         ▼
    HC-SR04   Pan-Tilt   Alerts
              Servos     Buzzer/Laser
```

---

## 📁 Project Structure

```text
IoT-Smart-Radar-Tracker/
│
├── arduino/
│   └── tracking_system/
│       └── tracking_system.ino
│
├── python/
│   ├── main.py
│   ├── tracker.py
│   ├── pid_controller.py
│   ├── serial_comm.py
│   ├── config.py
│   ├── hand_landmarker.task
│   └── requirements.txt
│
├── Smart_Radar_System_Report.docx
├── iot project-Dashboard.pptx
├── التوصيلات.md
├── .gitignore
└── README.md
```

> Python cache files such as `__pycache__/` and `*.pyc` are excluded from the repository.

---

## 👨‍💻 My Contribution

### Computer Vision & Python

My contribution focused on the **Python-based Computer Vision component** and its integration with the Arduino-controlled tracking system.

Key responsibilities included:

* Developing the Computer Vision component using **MediaPipe** and **OpenCV-Contrib-Python**.
* Processing camera input in real time.
* Working on object detection and tracking functionality.
* Using **NumPy** for numerical and data processing operations.
* Implementing **Python ↔ Arduino communication** using PySerial.
* Integrating Computer Vision outputs with the Pan-Tilt tracking mechanism.
* Contributing to the Python-side system integration and real-time tracking behavior.

---

## 👥 Team Project

This project was developed collaboratively by a team of **11 members**.

### Team Members

* Taha Abdel-Samie Taha
* Taha Mohamed Taha
* Hazem Mohamed Salah
* Amin Reda Amin
* Hassan Mostafa Hassan
* Ibrahim Hassan Ibrahim
* Abdel-Rahman Ahmed Abdel-Shafy
* Ahmed El-Saudi Gad
* Eissa Ali Hamed
* Ahmed Zeidan Mokhtar
* Maged Qasem Hammad

The team worked across multiple areas including:

* IoT
* Embedded Systems
* Computer Vision
* Python
* Arduino
* Hardware Integration
* System Development

---

## 🎥 Demo & Documentation

Explore the project through the following resources:

### 🎥 Project Demo Video

A demonstration of the Smart Radar System operating in real time.

**[▶️ Watch Project Demo](https://drive.google.com/file/d/1vAxZLY_458RVwomwx5LIzLksTTPDwrOj/view?usp=sharing)**

### 📊 IoT Project Dashboard

Project dashboard and presentation covering the system and its implementation.

**[📊 View IoT Project Dashboard](https://docs.google.com/presentation/d/1OB8Cuo7KbTeh2MEcdL5jA7xYNDSrro3n/edit?usp=sharing&ouid=116769900194078493481&rtpof=true&sd=true)**

### 📄 Smart Radar System Report

Detailed documentation covering the project concept, hardware, circuit connections, and implementation.

**[📄 View Smart Radar System Report](https://docs.google.com/document/d/17Hs8i78201mNCiZVNW5llVckPj1hTbRd/edit?usp=sharing&ouid=116769900194078493481&rtpof=true&sd=true)**

---

## 🚀 Future Improvements

Possible future improvements include:

* 🤖 More advanced Computer Vision models.
* 🎯 Improved tracking accuracy.
* 👥 Multiple-object tracking.
* 📏 Improved distance estimation.
* 📡 Wireless communication instead of USB Serial.
* 🌐 Web-based monitoring dashboard.
* 🎮 Remote system control.
* 📊 Integration with additional IoT sensors.
* ⚡ Improved system performance and response time.

---

## 📌 Project Type

**Team Project — IoT + Computer Vision + Embedded Systems**

---

## ⭐ Summary

The **IoT Smart Radar Tracker** demonstrates the integration of **Computer Vision, IoT, and Embedded Systems** in a real-time object tracking application.

By combining **Arduino UNO R4 Minima, HC-SR04 ultrasonic sensing, Pan-Tilt servo control, Python, MediaPipe, OpenCV-Contrib-Python, NumPy, and PySerial**, the project connects physical sensing and motion control with intelligent visual processing.

This project provided practical experience in building and integrating a complete hardware-software system for real-time object detection and tracking.
