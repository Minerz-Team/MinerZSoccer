# Bill of Materials (BOM)

This document lists the components required to build the MinerZ Soccer Robot.

## Required Components

| Qty | Component | Notes |
| ------ | ----------- | -------- |
| 1 | ESP32 DevKit (30-pin) | Standard ESP32 development board |
| 1 | ESP32 IO Shield | Includes onboard voltage regulator |
| 1 | L298N Motor Driver | Standard dual H-bridge module |
| 2 | TT DC Gear Motors | Typical yellow plastic gear motors, 3–6V |
| 2 | Wheels (48 mm) | Compatible with TT gear motors |
| 1 | 2x18650 Battery Holder | Series configuration (2S) |
| 2 | 18650 Rechargeable Cells | Matched cells recommended |
| 1 | Power Switch | SPST switch |
| 1 | 3D Printed Chassis | See hardware/3d-models |
| 4 | M3x35 Screws | Motor mounting |
| 4 | M3 Nuts | Motor mounting |
| Assorted | Jumper Wires | Male-to-male and male-to-female |

---

## Motor Options

The robot was designed around the common TT-style plastic gear motors.

Typical gear ratios:

- 48:1
- 60:1

Both variants are compatible with the chassis and firmware.

---

## Battery Requirements

The robot uses:

- 2 × 18650 Li-Ion cells
- Connected in series (2S)

Electrical characteristics:

| Parameter | Value |
| ----------- | --------- |
| Nominal Voltage | 7.4 V |
| Fully Charged Voltage | 8.4 V |

Use only quality rechargeable cells in good condition.

---

## Tools Required

Recommended tools:

- Small Phillips screwdriver
- M3 wrench or pliers
- Wire cutter
- Hot glue gun (optional)
- Double-sided foam tape (optional)

---

## Optional Components

These items are not required but may improve reliability:

| Component | Purpose |
| ----------- | ------------ |
| Plastic standoffs | Alternative electronics mounting |
| Heat shrink tubing | Cable management |
| Zip ties | Cable management |
| XT30 connector | Battery quick-disconnect |

---

## Electronics Mounting

The design intentionally avoids complicated mounting hardware.

The ESP32 IO Shield and L298N can be secured using:

- Double-sided foam tape
- Hot glue
- Plastic standoffs (optional)

The battery holder slides directly into the dedicated slot integrated into the chassis.
