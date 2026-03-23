<div align="center">

<img src="https://img.shields.io/badge/HTL%20St.%20P%C3%B6lten-Robotics-e63946?style=for-the-badge&logo=probot&logoColor=white" alt="HTL St. Pölten Robotics"/>

### Autonomous robotics · [HTL St. Pölten](https://www.htlstp.ac.at/) · Austria

Competing in [Botball](https://www.botball.org/) & [ECER](https://ecer.botball.org/)

*"Raise the Floor, Don't Lower the Ceiling"*

![C++](https://img.shields.io/badge/C%2B%2B20-00599C?style=flat-square&logo=cplusplus&logoColor=white)
![C](https://img.shields.io/badge/C-A8B9CC?style=flat-square&logo=c&logoColor=black)
![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![Dart](https://img.shields.io/badge/Dart%2FFlutter-02569B?style=flat-square&logo=flutter&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white)
![C#](https://img.shields.io/badge/C%23-512BD4?style=flat-square&logo=dotnet&logoColor=white)

</div>

---

## What We Do

We build autonomous robots that compete on a game table — navigating, detecting objects, and completing missions with zero human input. Our platform, **RaccoonOS**, is a full custom stack running on the [KIPR Wombat](https://www.kipr.org/kipr/hardware/botball-controller-wombat) controller, from bare-metal firmware up to a visual programming environment.

## RaccoonOS Architecture

Five layers, one shared LCM communication backbone — no capability gaps between beginner and expert workflows.

```
 ┌─────────────────────────────────────────────────────────────┐
 │  Layer 5   Visual Flowchart Editor (WebIDE)                 │  Drag-and-drop mission
 │            Generates identical Python to hand-written code  │  building for beginners
 ├─────────────────────────────────────────────────────────────┤
 │  Layer 4   Declarative Python SDK                           │  Step-based missions:
 │            drive · turn · line-follow · wall-align          │  parallel, timeout, loops
 ├─────────────────────────────────────────────────────────────┤
 │  Layer 3   Raccoon CLI                                      │  Scaffolding, hardware
 │            Project toolchain & code generation              │  wizard, calibration, sync
 ├─────────────────────────────────────────────────────────────┤
 │  Layer 2   C++20 Middleware (LibStp)                        │  PID control, kinematics,
 │            Differential & mecanum · odometry · IMU fusion   │  automated PID tuning
 ├─────────────────────────────────────────────────────────────┤
 │  Layer 1   LCM Transport & Hardware Bridge                  │  SPI ↔ STM32F427 firmware
 │            raccoon-transport (C++ · Python · Dart)          │  25 kHz PWM · 200 Hz PID
 └─────────────────────────────────────────────────────────────┘
                        KIPR Wombat + Raspberry Pi
```

## Repositories

| Repository | Description | Tech |
|:-----------|:-----------|:-----|
| **[raccoon-lib](https://github.com/htl-stp-ecer/raccoon-lib)** | Core robotics library — PID control, kinematics, odometry, step-based missions | ![C++](https://img.shields.io/badge/-C%2B%2B20-00599C?style=flat-square&logo=cplusplus&logoColor=white) ![Python](https://img.shields.io/badge/-Python-3776AB?style=flat-square&logo=python&logoColor=white) |
| **[raccoon-transport](https://github.com/htl-stp-ecer/raccoon-transport)** | LCM-based inter-process messaging with reliable delivery | ![C++](https://img.shields.io/badge/-C%2B%2B20-00599C?style=flat-square&logo=cplusplus&logoColor=white) ![Dart](https://img.shields.io/badge/-Dart-02569B?style=flat-square&logo=dart&logoColor=white) ![Python](https://img.shields.io/badge/-Python-3776AB?style=flat-square&logo=python&logoColor=white) |
| **[raccoon-cli](https://github.com/htl-stp-ecer/raccoon-cli)** | Development toolchain — scaffolding, hardware wizard, codegen, remote sync | ![Python](https://img.shields.io/badge/-Python-3776AB?style=flat-square&logo=python&logoColor=white) |
| **[Firmware-Stp](https://github.com/htl-stp-ecer/Firmware-Stp)** | Bare-metal STM32F427 firmware — motor PID, servo, IMU, SPI bridge | ![C](https://img.shields.io/badge/-C-A8B9CC?style=flat-square&logo=c&logoColor=black) |
| **[stm32-data-reader](https://github.com/htl-stp-ecer/stm32-data-reader)** | Raspberry Pi ↔ STM32 SPI bridge, publishes sensor data via LCM | ![C++](https://img.shields.io/badge/-C%2B%2B20-00599C?style=flat-square&logo=cplusplus&logoColor=white) |
| **[botui](https://github.com/htl-stp-ecer/botui)** | StpVelox — on-robot Flutter desktop environment with dashboard & sensor viz | ![Flutter](https://img.shields.io/badge/-Flutter-02569B?style=flat-square&logo=flutter&logoColor=white) |
| **[raccoon-cam](https://github.com/htl-stp-ecer/raccoon-cam)** | High-performance camera streaming with LCM integration | ![C++](https://img.shields.io/badge/-C%2B%2B20-00599C?style=flat-square&logo=cplusplus&logoColor=white) |
| **[documentation](https://github.com/htl-stp-ecer/documentation)** | Technical docs site | ![Hugo](https://img.shields.io/badge/-Hugo-FF4088?style=flat-square&logo=hugo&logoColor=white) |
| **[spring-2026-gametable](https://github.com/htl-stp-ecer/spring-2026-gametable)** | ESP32-C3 drum dispenser controller with Next.js web UI | ![C++](https://img.shields.io/badge/-C%2B%2B-00599C?style=flat-square&logo=cplusplus&logoColor=white) ![Next.js](https://img.shields.io/badge/-Next.js-000?style=flat-square&logo=nextdotjs&logoColor=white) |
| **[Papers-and-Documentations](https://github.com/htl-stp-ecer/Papers-and-Documentations)** | Research papers & competition documentation archive | ![Docs](https://img.shields.io/badge/-Papers-grey?style=flat-square&logo=readme&logoColor=white) |

## Beyond the Stack

**Computer Vision** — YOLOv11 object detection trained on real footage and synthetic data from our Unity-based simulator with randomized camera angles, lighting, and object placement.

**Path Planning** — A\* pathfinder with correction-weighted costs that prefers routes along walls and lines, giving the robot tactile feedback for mid-mission self-correction instead of relying on dead reckoning.

**On-Robot UI** — StpVelox, a custom Flutter desktop environment running directly on the Pi via flutter-pi, with a real-time dashboard, sensor visualization, camera feed, and WiFi management.

**Custom OS** — StpOs, a reproducible Raspberry Pi image built with our own image creator, pre-configured with all RaccoonOS services.

---

<div align="center">

![Raspberry Pi](https://img.shields.io/badge/Raspberry%20Pi-A22846?style=flat-square&logo=raspberrypi&logoColor=white)
![STM32](https://img.shields.io/badge/STM32-03234B?style=flat-square&logo=stmicroelectronics&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)
![CMake](https://img.shields.io/badge/CMake-064F8C?style=flat-square&logo=cmake&logoColor=white)
![Unity](https://img.shields.io/badge/Unity-000000?style=flat-square&logo=unity&logoColor=white)
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white)

**St. Pölten, Austria** · [htlstp.ac.at](https://www.htlstp.ac.at/)

</div>
