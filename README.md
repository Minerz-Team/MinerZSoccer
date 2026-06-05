# ⚽ MinerZ Soccer Robot

An open-source educational soccer robot platform based on ESP32, WiFi communication, 3D printed parts, and a desktop Driver Station.

Designed for robotics clubs, STEM programs, classroom competitions, and hobbyist projects.

---

## Overview

This project provides everything needed to build and operate a low-cost WiFi-controlled soccer robot:

- ESP32 firmware using ESP-IDF
- Desktop Driver Station for Windows and macOS
- Modular electronics using widely available components
- 3D printable chassis
- Assembly and wiring documentation
- Optional competition scoring system

The platform was created with simplicity, accessibility, and educational use in mind.

---

## Features

- WiFi-based robot control
- Differential drive (tank steering)
- ESP32 SoftAP mode for competition environments
- Desktop Driver Station
- Automatic motor fail-safe
- Fully open-source firmware
- Simple modular hardware
- Single-piece 3D printed chassis
- No custom PCB required

---

## Hardware

The robot is intentionally built from inexpensive and easy-to-source components.

### Main Components

| Qty | Component |
|------|-----------|
| 1 | ESP32 DevKit (30-pin) |
| 1 | ESP32 Expansion Shield |
| 1 | L298N Motor Driver |
| 2 | DC Gear Motors |
| 2 | Wheels |
| 1 | Battery Holder |
| 2 | Rechargeable Cells |
| 1 | Power Switch |
| 1 | 3D Printed Chassis |
| 4 | M3 Screws |
| Assorted | Jumper Wires |

A complete Bill of Materials is available in:

`docs/bom.md`

---

## Mechanical Design

The chassis is designed as a single 3D printed part to simplify assembly and reduce manufacturing time.

### Attribution

This design is based on:

**Soccer Robot – Battle & Soccer Hybrid Chassis**  
Author: Diego Armaker

Original model:

https://www.thingiverse.com/thing:7239226

Licensed under:

Creative Commons Attribution (CC BY)

Modifications were made to adapt the design to this platform and its electronics.

---

## Assembly

The robot can be assembled using basic tools and commonly available components.

Assembly instructions:

`docs/assembly.md`

---

## Wiring

The electronics are completely modular and do not require soldering beyond basic motor and power connections.

Wiring guide:

`docs/wiring.md`

---

## Software Components

### ESP32 Firmware

Firmware written in C using ESP-IDF.

Repository:

`soccer-robot-firmware-esp32`

### Driver Station

Desktop application used to control the robot.

Supported platforms:

- Windows
- macOS

Repository:

`soccer-robot-driver-station`

Precompiled binaries are available in the Releases section.

### Scoring System

Optional scoring and match-management software inspired by educational robotics competitions.

Repository:

`soccer-robot-scoring-system`

---

## Downloads

Precompiled applications are available under GitHub Releases.

Available downloads may include:

- Driver Station (Windows)
- Driver Station (macOS)
- Scoring System (Windows)
- Scoring System (macOS)

---

## Project Structure

```text
soccer-robot/
├── docs/
│   ├── assembly.md
│   ├── bom.md
│   ├── wiring.md
│   └── competition-setup.md
│
├── hardware/
│   ├── 3d-models/
│   └── wiring/
│
├── images/
│
└── README.md
```

---

## Intended Use

This project is intended for:

- Educational robotics programs
- STEM workshops
- School competitions
- Robotics clubs
- Makerspaces
- Hobby robotics enthusiasts

---

## License

Firmware and software components are released under the MIT License unless otherwise specified.

The modified chassis design remains subject to the attribution requirements of the original CC BY license.

See the LICENSE file for details.

---

## Contributing

Contributions, bug reports, documentation improvements, and feature suggestions are welcome.

If you build a robot using this project, feel free to share photos, videos, or improvements with the community.

---

## Acknowledgments

Special thanks to:

- Espressif Systems for ESP32 and ESP-IDF
- The open-source robotics community
- Diego Armaker for the original chassis design
- Everyone contributing to educational robotics initiatives
