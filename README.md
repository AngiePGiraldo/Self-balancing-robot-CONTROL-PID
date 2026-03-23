# 🤖 Self-Balancing Robot using PID Control (Arduino + ESP32)

*Applying control theory to stabilize an inverted pendulum system using real-time feedback and PID control.*

![Robot](media/robot.jpg)

---

## 📌 Overview
This project presents the design and construction of a self-balancing robot based on the inverted pendulum principle.

The system consists of a two-wheeled robot capable of maintaining its balance autonomously by using sensor feedback and a PID controller. The robot continuously adjusts its position in real time to remain upright.

The project integrates control theory, embedded systems, and signal processing.

---

## 🎯 Objectives
- Design and build a two-wheeled self-balancing robot  
- Implement a PID controller for stabilization  
- Process sensor data from an MPU6050 (accelerometer + gyroscope)  
- Apply digital filtering to improve signal accuracy  
- Control the system using Arduino and ESP32  

---

## ⚙️ System Description

The robot is based on the **inverted pendulum model**, an inherently unstable system that requires continuous control to maintain equilibrium.

### 🔹 Key Components
- Microcontroller: Arduino UNO + ESP32  
- Sensor: MPU6050 (accelerometer and gyroscope)  
- Actuators: DC motors with gearbox  
- Motor driver: H-bridge  
- Power system: Batteries  
- Structure: Two-wheel platform  

---

## 🧠 Control Theory

### 🔹 Inverted Pendulum Principle
The robot behaves like an inverted pendulum, which is naturally unstable. Without control, it will fall due to gravity.

The system must constantly apply corrective forces to maintain vertical stability.

---

### 🔹 PID Controller
A PID (Proportional–Integral–Derivative) controller is used to stabilize the robot:

- **Proportional (P):** reacts to current error  
- **Integral (I):** corrects accumulated error  
- **Derivative (D):** anticipates future error  

The controller calculates the necessary motor speed adjustments based on the tilt angle.

---

## 📡 Sensor Processing

### 🔹 MPU6050
The MPU6050 provides:
- Acceleration data  
- Angular velocity  

### 🔹 Digital Filtering
Sensor data is filtered to reduce noise and improve stability:

- Combines accelerometer and gyroscope data  
- Produces a more accurate tilt angle  

---

## 🔄 System Operation

### 1. Initialization
- Microcontroller starts  
- Sensor calibration is performed  
- PID parameters are initialized  

---

### 2. Real-Time Loop
The robot continuously performs:

1. Reads MPU6050 data  
2. Calculates tilt angle  
3. Compares with desired angle (vertical position)  
4. Computes PID correction  
5. Sends control signals to motors  

---

### 3. Stabilization
The robot dynamically adjusts motor speed and direction to maintain balance.

---

## ⚡ Control Logic

- Error = Desired angle − Measured angle  
- PID output → Motor control signal  
- Continuous feedback loop ensures stability  

---

## 🖼️ System Diagram
![Control Diagram](media/diagram.png)

---

## 🎥 Demo
[![Watch the demo](https://img.youtube.com/vi/VIDEO_ID/0.jpg)](https://www.youtube.com/watch?v=VIDEO_ID)

---

## 📂 Project Structure
