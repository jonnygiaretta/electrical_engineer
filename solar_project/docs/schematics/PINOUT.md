# System Architecture & Circuit Wiring Guide

This document provides the complete schematic diagrams, block architecture, and step-by-step wiring instructions for both the **Power Harvesting Subsystem (Phase 1 Bench MVP)** and the **Solar Tracking Subsystem (Phase 2)**.

---

## 1. System Block Diagram

```text
===================================================================================
                        POWER & HARVESTING SUBSYSTEM (PHASE 1)
===================================================================================

[ 6V / 5W Solar Panel ]
         │
   (IN+ / IN-)
         ▼
[ TP4056 Charger Module ] ───(B+ / B-)───> [ 18650 Li-ion Cell (3.7V) ]
         │
  (OUT+ / OUT-)
         ▼
[ DC-DC Boost Converter ] ───────────────> [ Regulated 5V USB Bus ]
                                                 │
                                                 ├──> [ USB Device / Load ]
                                                 └──> [ Microcontroller Power ]

===================================================================================
                        TRACKING & CONTROL SUBSYSTEM (PHASE 2)
===================================================================================

[ Light Sensors Array ]
  ├── LDR Top-Left (TL)     ──> GPIO 36 / A0 ┐
  ├── LDR Top-Right (TR)    ──> GPIO 39 / A1 ├─> [ Microcontroller (ESP32/Arduino) ]
  ├── LDR Bottom-Left (BL)  ──> GPIO 34 / A2 │          │
  └── LDR Bottom-Right (BR) ──> GPIO 35 / A3 ┘          ├── GPIO 18 / Pin 9  ──> [ Servo X (Pan) ]
                                                        └── GPIO 19 / Pin 10 ──> [ Servo Y (Tilt) ]
VCC (3.3V / 5V) ────[ LDR Sensor ]────┬────[ Microcontroller Analog Pin ]
                                       │
                                 [ 10kΩ Resistor ]
                                       │
                                      GND
