# 📡 Radar Surveillance System

A real-time radar surveillance system designed to detect objects, track their direction of movement, provide an audio alert, and indicate whether an object is approaching or moving away using red and green LEDs.

---

## 🚀 Project Overview

The Radar Surveillance System uses an ultrasonic sensor mounted on a servo motor to continuously scan the surrounding area.

When an object is detected, the system:

- 📍 Detects the presence of an object
- 📏 Measures the distance to the object
- 🔄 Tracks the direction of the detected object
- 🔊 Generates a sound alert when an object is detected
- 🔴 Turns the red LED ON when the object is moving towards the system
- 🟢 Turns the green LED ON when the object is moving away
- 📡 Continuously scans the surrounding area in real time

---

## 🛠️ Components Used

### Hardware

- Arduino UNO
- HC-SR04 Ultrasonic Sensor
- Servo Motor
- Red LED
- Green LED
- Buzzer
- Resistors
- Breadboard
- Jumper Wires

### Software

- Arduino IDE
- Embedded C / Arduino C

---

## 🔌 Circuit Connections

The system consists of an Arduino UNO connected to the HC-SR04 ultrasonic sensor, servo motor, buzzer, and LED indicators.

The ultrasonic sensor is mounted on the servo motor to enable scanning across different angles.

### Circuit Diagram

![Circuit Connections](images/circuit-connections.jpg)

---

## 🤖 Hardware Prototype

The completed prototype integrates the ultrasonic sensor, servo motor, Arduino UNO, LEDs, and buzzer into a physical radar surveillance model.

### Final Project Prototype

![Radar Surveillance System Prototype](images/radar-prototype.jpg)

---

## ⚙️ Working Principle

### 1. Object Scanning

The HC-SR04 ultrasonic sensor is mounted on a servo motor. The servo continuously rotates the sensor through a predefined angular range.

### 2. Object Detection

The ultrasonic sensor emits an ultrasonic pulse and measures the reflected echo to determine the distance of an object.

### 3. Direction Tracking

The servo angle and distance measurements are monitored during scanning to track the direction and movement of the detected object.

### 4. Audio Alert

When an object is detected within the specified detection range, the buzzer produces an alert sound.

### 5. Object Moving Towards the System 🔴

If the measured distance decreases during successive detections, the system identifies that the object is moving towards the radar.

**Red LED → ON**

### 6. Object Moving Away 🟢

If the measured distance increases during successive detections, the system identifies that the object is moving away from the radar.

**Green LED → ON**

---

## 🔄 System Flow

```text
             START
               |
               v
       Initialize System
               |
               v
       Servo Starts Scanning
               |
               v
      Ultrasonic Measurement
               |
               v
       Object Detected?
          /          \
        NO            YES
        |              |
        |              v
        |       Measure Distance
        |              |
        |              v
        |       Track Direction
        |              |
        |              v
        |         Sound Alert
        |              |
        |              v
        |       Compare Distance
        |          /        \
        |    Decreasing    Increasing
        |        |             |
        |        v             v
        |     RED LED       GREEN LED
        |     ON 🔴          ON 🟢
        |        \             /
        |         \           /
        |          v         v
        +------ Continue Scanning# RADAR-SURVEILLANCE-SYSTEM
