# ClimaField: IoT Weather Station

[![Project Status](https://img.shields.io/badge/Status-In%20Development-yellow)](#)
[![Hardware](https://img.shields.io/badge/Hardware-ESP32-blue)](#)
[![Field](https://img.shields.io/badge/Focus-Precision%20Agriculture-green)](#)
[![Language](https://img.shields.io/badge/Language-C++-orange)](#)
[![License](https://img.shields.io/badge/License-Proprietary-red)](#)

English Version | [Portuguese Version](README.md)

## 📌 About the project
**ClimaField** is a low-cost, high-precision weather station designed for monitoring agricultural microclimates at the field edge. Built on the ESP32 platform (C++), the project not only reads sensor data but also processes information locally (*Edge Computing*) to deliver ready-to-use metrics for on-field decision-making.

The combination of electronic engineering and agronomic science allows the equipment to act as a critical tool for precision agriculture, providing vital data for water management and the safety and efficacy of field operations.

## 🌱 Agronomic relevance
The data collected and processed by this station has direct applications in advanced agricultural operations:
- **Spraying windows:** The built-in calculation of the *dew point* and humidity monitoring are crucial for calculating *Delta T*, an essential metric to optimize crop protection applications (especially those performed by agricultural drones and aircraft), mitigating drift risks and rapid droplet evaporation.
- **Disease prevention and control:** Continuous monitoring of temperature and relative humidity helps in modeling alerts for fungal diseases.
- **Thermodynamic analysis:** Atmospheric pressure data assists in forecasting cold fronts and local rainfall with greater accuracy than large-scale regional meteorological models.

## 🚀 Roadmap and future implementations
- [x] Baseline reading of temperature, humidity, and atmospheric pressure.
- [x] Edge processing: Mathematical calculation of the dew point using the Magnus-Tetens equation.
- [ ] **Sensor expansion:** Integration of an anemometer and tipping bucket rain gauge.
- [ ] **IoT Telemetry:** Data transmission via MQTT protocol to remote dashboards.
- [ ] **Data integration:** Structuring pipelines (e.g., Python) for spatial microclimate analysis and integration with GIS tools.
- [ ] **Autonomous power:** Implementation of a solar panel with a charge controller (TP4056) for uninterrupted field operation.

## ⚖️ License and copyright
**© 2026 Douglas Mardegan Colodete. All rights reserved.**

This is a **proprietary** project. The materials provided here (documentation, schematics, operational logic, and visual demonstrations) are strictly for professional portfolio presentation purposes.

Copying, reproducing, distributing, modifying, or using (commercially or personally) any part of this project, hardware, or firmware without prior express written authorization from the author is **strictly prohibited**.

> *Note: Due to protected intellectual property, the full source code is not available for public cloning.*
