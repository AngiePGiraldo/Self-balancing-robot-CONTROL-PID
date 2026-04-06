# 🤖 Self-Balancing Robot using PID Control (Arduino + ESP32)

*Applying control theory to stabilize an inverted pendulum system using real-time feedback and PID control.*

<p align="center">
  <!-- Dos imágenes abajo -->
  <img src="https://github.com/AngiePGiraldo/Self-balancing-robot-CONTROL-PID/blob/f3d4512e6a55740b22b476a2bfff1324cc5d3034/Step2.jpg" width="350"/>
  <img src="https://github.com/AngiePGiraldo/Self-balancing-robot-CONTROL-PID/blob/f3d4512e6a55740b22b476a2bfff1324cc5d3034/Step1.jpg" width="350"/>
</p>

<p align="center">
  <!-- Imagen principal -->
  <img src="https://github.com/AngiePGiraldo/Self-balancing-robot-CONTROL-PID/blob/f3d4512e6a55740b22b476a2bfff1324cc5d3034/Step3.jpeg" width="400"/>
</p>


## 🎥 Demo

You can see the robot in action at the following link:  

[▶️ View Pendulum Robot Demo](https://www.youtube.com/shorts/_cYoVbgTlMY)


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
<p align="center">
  <!-- Imagen principal -->
  <img src="https://github.com/AngiePGiraldo/Self-balancing-robot-CONTROL-PID/blob/42abaf94716247d9164f9af9e24d7a854b836e3c/control.png" width="300"/>
</p>

---

## ⚡ Control Logic

- Error = Desired angle − Measured angle  
- PID output → Motor control signal  
- Continuous feedback loop ensures stability  

---

## 🖼️ System Diagram

<p align="center">
  <!-- Imagen principal -->
  <img src="https://github.com/AngiePGiraldo/Self-balancing-robot-CONTROL-PID/blob/42abaf94716247d9164f9af9e24d7a854b836e3c/Connections%20of%20actuators%20and%20sensors.png" width="400"/>
</p>

