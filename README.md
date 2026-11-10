# atomQUEST 2026 — Smart Temperature-Controlled Ceiling Fan

A smart ceiling-fan prototype designed for **atomQUEST 2026**, combining temperature-based automatic speed control with an energy-efficient ceiling-fan blade concept designed in **SOLIDWORKS**.

## Project Overview

The project aims to develop a smart fan system that automatically adjusts fan operation according to the surrounding temperature.

The system combines:

- Arduino-based control
- Temperature sensing
- Automatic fan control
- DC motor-based prototype
- Current monitoring using INA219
- Custom ceiling-fan blade CAD design
- Temperature-dependent control logic

## Objectives

1. Design an efficient ceiling-fan blade geometry.
2. Monitor ambient temperature continuously.
3. Automatically adjust fan operation according to temperature.
4. Monitor electrical current consumption.
5. Develop a low-voltage prototype using Arduino.
6. Create a CAD model of the proposed fan blade using SOLIDWORKS.

## System Architecture

```text
             Temperature Sensor
                    │
                    ▼
              Arduino Uno
                    │
        ┌───────────┴───────────┐
        │                       │
        ▼                       ▼
 Temperature-Based         Serial Monitor
 Control Algorithm          (Laptop)
        │
        ▼
   Fan Driver / MOSFET
        │
        ▼
     DC Fan Motor
        │
        ▼
     Airflow Output

INA219 ───────► Arduino
  │
  └── Current / Power Monitoring
```

## Hardware

| Component | Purpose |
|---|---|
| Arduino Uno | Main controller |
| Temperature Sensor | Measures ambient temperature |
| DC Motor / Fan | Fan prototype |
| INA219 | Current monitoring |
| MOSFET / Driver | Fan power control |
| 12V DC Supply | Motor power |
| Breadboard & Jumper Wires | Prototype connections |

## Temperature-Based Control

The basic control concept is:

| Temperature | Fan Response |
|---|---|
| Low | Low / OFF |
| Moderate | Medium |
| High | High |

The controller continuously reads the temperature and changes the fan output accordingly.

Hysteresis can be incorporated into the control logic to prevent rapid switching around temperature thresholds.

## CAD Blade Design

The ceiling-fan blade was designed in **SOLIDWORKS** with emphasis on:

- Aerodynamic blade profile
- Airflow generation
- Reduced drag
- Efficient geometry
- Manufacturability
- Integration with a ceiling-fan concept

### Blade Design

The CAD model forms the mechanical design component of the project and can be further optimized through simulation and physical testing.

## Project Workflow

```text
Temperature Measurement
          ↓
Arduino Processing
          ↓
Temperature-Based Decision
          ↓
Fan Speed Control
          ↓
Airflow Generation
          ↓
Current Monitoring
          ↓
Performance Evaluation
```

## Control Logic

The controller follows a temperature-dependent strategy:

```text
Read Temperature
       ↓
Compare with Threshold
       ↓
Determine Required Fan Output
       ↓
Control Motor
       ↓
Read Current
       ↓
Display Data on Serial Monitor
       ↓
Repeat
```

## Monitoring

The INA219 module can be used to monitor the electrical characteristics of the motor.

The laptop Serial Monitor can display parameters such as:

```text
Temperature: XX °C
Current: XX mA
Fan Output: XX %
```

This provides a simple method for observing system behaviour during testing.

## Key Features

- 🌡️ Temperature-based automatic control
- ⚡ Electrical current monitoring
- 🌀 Custom fan-blade CAD design
- 🖥️ Serial Monitor-based data display
- 🔌 Low-voltage prototype architecture
- 🔧 Arduino-based control system

## Repository Structure

```text
atomQUEST-smart-fan/
│
├── README.md
│
├── CAD/
│   ├── fan_blade.SLDPRT
│   └── blade_design_images/
│
├── Arduino/
│   └── smart_fan.ino
│
├── Documentation/
│   └── project_report.pdf
│
└── Media/
    └── prototype_video.mp4
```

## Applications

The concept can be extended to:

- Smart ceiling fans
- Energy-efficient cooling systems
- IoT-enabled appliances
- Smart home automation
- Temperature-controlled ventilation
- HVAC control systems

## Future Improvements

- Replace the prototype DC motor with a BLDC ceiling-fan motor.
- Implement closed-loop RPM control.
- Add Wi-Fi/IoT monitoring.
- Develop a more optimized aerodynamic blade profile.
- Perform CFD analysis of the blade.
- Compare airflow and power consumption for different blade geometries.
- Develop a dedicated PCB instead of a breadboard prototype.

## Project Status

**atomQUEST 2026 — Round 2 Project**

The project combines a functional prototype concept with a custom SOLIDWORKS blade design and temperature-based fan-control architecture.

## Team

**Team:** Classic  
**Institute:** Netaji Subhas University of Technology (NSUT)  
**Competition:** atomQUEST 2026  
**Track:** Fan
