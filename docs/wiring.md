# Wiring Guide

This document describes the recommended wiring configuration for the MinerZ Soccer Robot.

---

## System Overview

The robot consists of:

- ESP32 DevKit (30-pin)
- ESP32 IO Shield
- L298N Motor Driver
- Two TT Gear Motors
- 2S Battery Pack (2x18650)
- Power Switch

---

## Power Distribution

The robot uses a 2S battery pack.

Electrical characteristics:

| Parameter | Value |
| ------------ | --------- |
| Nominal Voltage | 7.4 V |
| Fully Charged Voltage | 8.4 V |

The positive battery lead is routed through the power switch before reaching the electronics.

### Power Topology

```text
Battery (+)
    │
    ▼
Power Switch
    │
    ├────────► ESP32 IO Shield VIN
    │
    └────────► L298N VIN

Battery (-)
    │
    ├────────► ESP32 IO Shield GND
    │
    └────────► L298N GND
```

All grounds must be connected together.

---

## Control Connections

The firmware expects the following pin assignment.

### ESP32 → L298N

| ESP32 GPIO | L298N Pin | Function |
| ------------ | ------------ | ------------ |
| GPIO32 | ENA | Motor A PWM |
| GPIO33 | IN1 | Motor A Direction |
| GPIO25 | IN2 | Motor A Direction |
| GPIO26 | ENB | Motor B PWM |
| GPIO18 | IN3 | Motor B Direction |
| GPIO27 | IN4 | Motor B Direction |

These are the default firmware pin assignments.

Changing them requires modifying the firmware configuration.

---

## Motor Connections

### Motor A

```text
L298N OUT1
L298N OUT2
```

Connect to the left motor.

### Motor B

```text
L298N OUT3
L298N OUT4
```

Connect to the right motor.

If a motor rotates in the wrong direction:

- Swap the motor wires
- Or enable the motor inversion option in firmware

---

## Recommended Wiring Diagram

![Wiring Diagram](../hardware/wiring/wiring-diagram.webp)

---

## Wiring Verification Checklist

Before inserting the batteries:

- [ ] Battery polarity verified
- [ ] Shared ground connected
- [ ] Switch installed on positive lead
- [ ] ESP32 shield powered correctly
- [ ] L298N powered correctly
- [ ] Motor wires connected
- [ ] No exposed conductors touching

---

## First Power-On

Expected behavior:

1. ESP32 powers on.
2. WiFi network becomes available.
3. Motors remain stopped.
4. No component overheats.

If anything behaves unexpectedly, disconnect power immediately and recheck wiring.
