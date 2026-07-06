

https://github.com/user-attachments/assets/4d9b1e94-e2e3-4042-be28-08845a11f739



# Autonomous Quadruped (Dog Robot) Navigation Stack 🐕🤖

## 🎯 Project Overview
This project implements a high-performance navigation and path-planning pipeline for a quadruped robot. The system utilizes an **ESP32-based** architecture to perform real-time sensor fusion and environment mapping, enabling autonomous decision-making on resource-constrained hardware.

## 🚀 Key Technical Features
- **High-Precision Sensor Fusion:** Integrated the **Bosch BNO055 9-axis IMU** for absolute orientation and motion tracking.
- **Embedded Perception:** Utilized **ESP32-CAM** for real-time visual data acquisition and environment awareness.
- **Hybrid Processing Pipeline:** Developed a dual-layer communication stack (C++ on the edge, Python for high-level data processing) to manage real-time path planning.
- **Signal Filtering:** Implemented Kalman/Complementary filters to minimize sensor noise and drift during dynamic locomotion.

## 🛠️ Hardware & Software Stack
- **Microcontroller:** ESP32-DevKit, ESP32-CAM (Dual-Core 240MHz)
- **Primary Sensor:** Bosch BNO055 (Absolute Orientation Sensor via I2C)
- **Languages:** C++ (Embedded), Python (Backend & Visualization)
- **Communication:** I2C, UART, Serial Data Streaming
- **Tools:** Arduino IDE, VS Code, Git

## 📂 System Architecture
1. **Perception Layer:** Continuous polling of the BNO055 and Camera feed.
2. **Navigation Logic:** On-device path calculation using simplified kinematic models.
3. **Execution Layer:** PWM-based motor/servo control for stable gait execution.
4. **Telemetry:** Real-time data logging to Python for performance analysis and path visualization.

---
*Developed as part of the Master's in Mechatronics and CPS at DIT Deggendorf.*
