# Cyber-Physical Solar Tracking & Energy Node

## What is this project?
This is a smart solar power system designed to maximize solar energy collection. It automatically moves a solar panel to follow the sun using light sensors and motor controls, while continuously recording power and system data in real time.

---

## Current Features (Scope)
* **Dual-Axis Solar Tracking:** Uses 4 light sensors (LDRs) and 2 servo motors to automatically follow the brightest light source.
* **Solar Energy Harvesting:** Benchtop setup using a 6V solar panel, TP4056 charge controller, and a Li-ion battery.
* **Live Telemetry Logging:** Reads real-time voltage and sensor metrics via USB/Serial using Python.
* **Clean Project Architecture:** Well-organized folders for code, hardware schematics, documents, and media.

---

## Future Roadmap (Planned Upgrades)
* **Power Upgrade:** Scale up to an 18V / 30W panel with a 3S battery pack and active BMS protection.
* **Wireless Telemetry:** Add LoRaWAN and MQTT protocol support for remote data logging over long distances.
* **Cyber-Physical Security Testing:** Implement anomaly detection algorithms to protect the system against physical sensor tampering and false data injection.

---

## Repository Structure

```text
solar_project/
├── docs/       # Research notes and concept documents
├── hardware/   # Component list (BOM) and pinout connections
├── firmware/   # C++ code for ESP32 / Arduino microcontrollers
├── telemetry/  # Python scripts for data logging
└── media/      # Photos and videos of the prototype
