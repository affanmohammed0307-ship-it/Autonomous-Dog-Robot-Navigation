

https://github.com/user-attachments/assets/3024fc90-f5d9-4be3-9d15-715217c848c5





https://github.com/user-attachments/assets/37021e00-36bc-4d67-9208-6acbde53766a

# Autonomous Dog Robot Navigation

Campus autonomous navigation system for a quadruped robot using 
ESP32, multi-sensor fusion, and a web-based mission control interface.



https://github.com/user-attachments/assets/bd1c0b8b-896e-45a3-93ff-430b2bee3cac

## What it does
- Autonomous point-to-point campus navigation using sensor fusion
- Web interface with mission commands: Go to B Building, Go to H Building, Stop
- Real-time obstacle detection and avoidance using LiDAR and Ultrasonic sensors
- GPS-based outdoor localization combined with IMU orientation tracking
- Hijack module architecture — plugs into existing robot hardware without modifying it

## Hardware
| Sensor | Purpose |
|---|---|
| 2D LiDAR | Obstacle detection and mapping |
| Ultrasonic | Close-range proximity detection |
| Camera (ESP32-CAM) | Visual feed |
| IMU (BNO055) | Orientation and motion tracking |
| GPS | Outdoor localization |
| ESP32 Dev Module | Navigation logic and motor control |
| ESP32 CAM Module | Camera feed |

## Software Architecture
```
Web Interface (Mission Commands)
        ↓
ESP32 Dev — Navigation Controller (RobotNav.ino)
        ↓
Sensor Fusion (LiDAR + Ultrasonic + IMU + GPS)
        ↓
Path Planning → Motor Commands → Robot Motion
```

## Key Files
- `RobotNav.ino` — Main navigation logic, sensor fusion, path planning
- `Controller.h` — Motor control and hardware abstraction layer
- `CAS_Cam_code` — ESP32-CAM firmware for visual feed
- `BNO055_Sensor_Integration1.txt` — IMU integration notes
- `FINAL_PATH.txt` — Waypoint definitions for campus navigation

## How to run
1. Flash `RobotNav.ino` to ESP32 Dev module via Arduino IDE
2. Flash `CAS_Cam_code` to ESP32-CAM module
3. Power on the robot and connect to the web interface
4. Select mission: Go to B Building / Go to H Building / Stop

## Built with
Arduino IDE · ESP32 · BNO055 IMU · LiDAR · GPS · C++
