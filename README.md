# 🚀 IoT Smart Radar Tracker

An IoT-based smart radar system that combines **Arduino hardware** with **Python Computer Vision** to detect, monitor, and track objects in real time.

The system performs **180° scanning**, measures object distance using an ultrasonic sensor, processes camera input through Computer Vision, and controls a **Pan-Tilt mechanism** to track detected targets.

---

## 🎯 Project Overview

The **IoT Smart Radar Tracker** is a team-based project that combines **IoT, Embedded Systems, Computer Vision, and Python** to create an interactive real-time tracking and surveillance system.

The system integrates an **Arduino UNO R4 Minima**, **HC-SR04 ultrasonic sensor**, servo motors, camera, buzzer, and Python-based Computer Vision.

The goal is to detect objects, estimate their distance, and automatically orient the Pan-Tilt mechanism toward detected targets while providing real-time feedback through the computer interface.

---

## 💡 Problem & Solution

### Problem

Traditional surveillance and monitoring systems often require continuous human observation and manual control.

### Solution

This project introduces an automated tracking system that combines:

* 📡 Ultrasonic sensing
* 👁️ Computer Vision
* 🔄 180° radar scanning
* 🎯 Pan-Tilt tracking
* 💻 Real-time Python processing
* 🔌 Arduino-Python communication
* 🔊 Alert mechanisms

Together, these components allow the system to detect and respond to objects in real time.

---

## ⚙️ How It Works

The system consists of two main parts:

### 🔌 1. Arduino Hardware

The Arduino controls the physical components of the system.

The **HC-SR04 ultrasonic sensor** performs distance measurements while the servo motors control the Pan-Tilt mechanism.

The Arduino communicates with the Python application through **USB Serial communication**.

### 🧠 2. Python Computer Vision

The computer receives camera input and processes it using:

* **MediaPipe**
* **OpenCV-Contrib-Python**
* **NumPy**

The Python application performs real-time Computer Vision processing and communicates with the Arduino using **PySerial**.

The Computer Vision results are then used to control the tracking mechanism.

---

## 🔄 System Workflow

```text
                     ┌──────────────────┐
                     │      Camera      │
                     └────────┬─────────┘
                              │
                              ▼
                     ┌──────────────────┐
                     │ Computer Vision  │
                     │ MediaPipe        │
                     │ OpenCV-Contrib   │
                     │ NumPy            │
                     └────────┬─────────┘
                              │
                              ▼
                     ┌──────────────────┐
                     │ Object Detection │
                     │   & Tracking     │
                     └────────┬─────────┘
                              │
                              │ PySerial
                              ▼
              ┌───────────────────────────────┐
              │       Arduino UNO R4          │
              │                               │
              │  ┌─────────────────────────┐  │
              │  │ HC-SR04 Ultrasonic      │  │
              │  │ Distance Measurement    │  │
              │  └────────────┬────────────┘  │
              │               │               │
              │               ▼               │
              │      ┌─────────────────┐      │
              │      │ Pan-Tilt Servos │      │
              │      └─────────────────┘      │
              └───────────────────────────────┘
                              │
                              ▼
                     ┌──────────────────┐
                     │ Real-Time System │
                     │    Response      │
                     └──────────────────┘
```

---

## ✨ Key Features

* 🔄 **180° Radar Scanning**
* 👁️ **Real-Time Computer Vision**
* 🎯 **Object Detection & Tracking**
* 📏 **Ultrasonic Distance Measurement**
* 🔧 **Automatic Pan-Tilt Control**
* 🔊 **Buzzer Alerts**
* 💻 **Real-Time Visualization**
* 🔌 **Arduino ↔ Python Serial Communication**
* ⚡ **Integrated IoT + Computer Vision System**

---

## 🛠️ Tech Stack

### 💻 Software

| Technology            | Purpose                                            |
| --------------------- | -------------------------------------------------- |
| Python                | Computer Vision application and system integration |
| MediaPipe             | Computer Vision and tracking                       |
| OpenCV-Contrib-Python | Image and video processing                         |
| NumPy                 | Numerical and array processing                     |
| PySerial              | Arduino-Python serial communication                |
| Arduino IDE           | Arduino development                                |

### 🔌 Hardware

| Component                 | Purpose                         |
| ------------------------- | ------------------------------- |
| Arduino UNO R4 Minima     | Main microcontroller            |
| HC-SR04                   | Ultrasonic distance measurement |
| Servo Motors              | Pan-Tilt movement               |
| Camera                    | Real-time visual input          |
| Buzzer                    | Detection alerts                |
| Laser Diode               | Visual pointing mechanism       |
| Breadboard & Jumper Wires | Hardware connections            |

---

## 🏗️ System Architecture

The project follows a hybrid **IoT + Computer Vision architecture**:

```text
              ┌─────────────┐
              │   Camera    │
              └──────┬──────┘
                     │
                     ▼
           ┌────────────────────┐
           │ Python CV Layer     │
           │                    │
           │ MediaPipe          │
           │ OpenCV-Contrib     │
           │ NumPy              │
           └─────────┬──────────┘
                     │
                     │ PySerial
                     ▼
           ┌────────────────────┐
           │ Arduino Control    │
           │ Layer              │
           └─────────┬──────────┘
                     │
              ┌──────┴───────┐
              ▼              ▼
       ┌────────────┐  ┌──────────────┐
       │  HC-SR04   │  │  Pan-Tilt    │
       │  Sensor    │  │  Servos      │
       └────────────┘  └──────────────┘
```

---

## 📁 Project Structure

```text
IoT-Smart-Radar-Tracker/
│
├── Arduino_Code/
│   └── tracking_system/
│       └── tracking_system.ino
│
├── Python_App/
│   ├── main.py
│   ├── tracker.py
│   ├── serial_comm.py
│   ├── config.py
│   ├── hand_landmarker.task
│   └── requirements.txt
│
├── Docs_and_Media/
│   ├── Smart_Radar_System_Report.pdf
│   ├── iot_project-Dashboard.pdf
│   ├── circuit_wiring.jpg
│   └── radar_demo.gif
│
├── .gitignore
└── README.md
```

> The project structure may vary depending on the final repository organization.

---

## 👨‍💻 My Contribution

### Computer Vision & Python

My contribution focused on the **Python-based Computer Vision component** and its integration with the Arduino-controlled tracking system.

Key responsibilities included:

* Developing the Computer Vision component using **MediaPipe** and **OpenCV-Contrib-Python**.
* Processing camera input in real time.
* Implementing object detection and tracking functionality.
* Using **NumPy** for numerical and data processing operations.
* Implementing **Python ↔ Arduino communication** using PySerial.
* Integrating Computer Vision results with the Pan-Tilt tracking mechanism.
* Contributing to the real-time behavior and integration of the overall system.

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

The project involved collaboration across different areas including:

* Embedded Systems
* IoT
* Computer Vision
* Python
* Hardware Integration
* System Development

---

## 🎥 Demo & Documentation

Explore the project through the following resources:

### 🎥 Project Demo Video

A demonstration of the Smart Radar system operating in real time.

**[▶️ Watch Project Demo](https://drive.google.com/file/d/1vAxZLY_458RVwomwx5LIzLksTTPDwrOj/view?usp=sharing)**

### 📊 IoT Project Dashboard

Project dashboard and presentation containing an overview of the system and its implementation.

**[📊 View IoT Project Dashboard](https://docs.google.com/presentation/d/1OB8Cuo7KbTeh2MEcdL5jA7xYNDSrro3n/edit?usp=sharing&ouid=116769900194078493481&rtpof=true&sd=true)**

### 📄 Smart Radar System Report

Detailed project documentation covering the system concept, implementation, and development.

**[📄 View Smart Radar System Report](https://docs.google.com/document/d/17Hs8i78201mNCiZVNW5llVckPj1hTbRd/edit?usp=sharing&ouid=116769900194078493481&rtpof=true&sd=true)**

---

## 🚀 Future Improvements

Possible future improvements include:

* 🤖 More advanced object detection models.
* 🎯 Improved tracking accuracy.
* 👥 Multiple-object tracking.
* 📏 Improved distance estimation.
* 📡 Wireless communication instead of USB Serial.
* 🌐 Web-based monitoring dashboard.
* 🎮 Remote system control.
* 📊 Additional IoT sensors.
* ⚡ Improved system performance and response time.

---

## 📌 Project Type

**Team Project — IoT + Computer Vision + Embedded Systems**

---

## ⭐ Summary

The **IoT Smart Radar Tracker** demonstrates how **Computer Vision and IoT hardware** can work together to create an interactive real-time tracking system.

By combining **Arduino, ultrasonic sensing, Python, MediaPipe, OpenCV-Contrib-Python, NumPy, and PySerial**, the project connects physical sensing and motion control with intelligent visual processing.

The project represents a practical application of **Computer Vision, IoT, Embedded Systems, and Python integration** in a real-world system.
