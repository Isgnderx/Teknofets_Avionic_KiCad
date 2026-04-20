# Teknofets_Avionic_KiCad

# Advanced Rocket Avionics System (KiCad Design)

## Overview

This repository contains an **advanced avionics system schematic** designed in **KiCad** for a **TEKNOFEST rocket project**.

The goal of this system was to develop a **more refined and integrated avionics architecture** compared to earlier EasyEDA-based iterations. This version focuses on improved modularity, cleaner signal routing, and a more structured hardware design approach.

However, due to unforeseen circumstances, the project was **postponed before completion**, leaving this design in a **partially finished state**.

Even though the system is incomplete, it is being shared as a **technical reference**, **learning resource**, and **foundation for future avionics development**.

---

## Project Status

**Status:** Incomplete / Archived / Reference Design

- Design is partially complete  
- Not validated for real flight  
- Some subsystems may require redesign or verification  
- Firmware integration not finalized  

This repository represents a **work-in-progress engineering effort**, not a finished product.

---

## System Architecture

The schematic shows a **centralized avionics system** built around a microcontroller platform with multiple integrated subsystems:

- Sensor acquisition  
- Telemetry communication  
- Data logging  
- Power distribution  
- Peripheral control  

---

## Core Controller

### **Arduino Mega 2560 Shield-Based Design**

At the center of the system is an **Arduino Mega 2560 shield layout**, acting as the main processing unit.

Responsibilities include:

- Sensor data acquisition  
- Communication management (SPI, I2C, UART)  
- Data logging coordination  
- Telemetry handling  
- Peripheral control  

The shield-based approach allows:

- rapid prototyping  
- modular development  
- easier debugging and replacement  

---

## Communication Interfaces

The design integrates multiple communication protocols:

### **SPI Bus**
Used for:
- SD Card module
- LoRa module

### **I2C Bus**
Used for:
- Sensor communication (BNO055, BMP390)

### **UART**
Used for:
- GPS module (NEO-6M)

This multi-bus architecture enables simultaneous operation of several subsystems.

---

## Telemetry System

### **LoRa Module**

The schematic includes a **LoRa communication module** (likely SX127x/SX126x family).

Purpose:
- Long-range wireless telemetry  
- Real-time transmission of flight data  

Possible transmitted data:
- altitude  
- orientation  
- GPS coordinates  
- system status  

---

## Navigation System

### **GPS Module (NEO-6M)**

The design integrates a **NEO-6M GPS module**, connected via UART.

Functions:
- Position tracking  
- Time synchronization  
- Recovery support  

---

## Data Logging

### **Micro SD Card Module**

An SPI-based **SD card module** is included.

Used for storing:
- sensor data  
- flight logs  
- GPS coordinates  
- telemetry backup  

This ensures data is preserved even if wireless communication fails.

---

## Sensor System

### **BNO055 (IMU)**

- 9-DOF sensor (accelerometer, gyroscope, magnetometer)
- Provides orientation and motion data
- Likely connected via I2C

Use cases:
- attitude estimation  
- motion tracking  
- flight dynamics analysis  

---

### **BMP390 (Barometric Sensor)**

- High-precision pressure sensor
- Used for altitude estimation

Use cases:
- altitude tracking  
- ascent/descent detection  
- flight phase identification  

---

## Power System

### **Battery Input & Distribution**

The system includes:

- battery input connector  
- power filtering components  
- regulated outputs  

Power rails likely include:
- 5V (for Arduino and some modules)
- 3.3V (for sensors and communication modules)

---

## Power Regulation

The schematic suggests:

- onboard voltage regulation  
- decoupling capacitors  
- stable power delivery to sensitive components  

Proper power design is critical for:

- sensor accuracy  
- communication stability  
- system reliability  

---

## Peripheral Control

### **Buzzer Circuit**

A transistor-driven buzzer is included.

Functions:
- system status indication  
- error alerts  
- debugging feedback  

---

## Signal Conditioning

### **Resistors & Supporting Components**

The design includes:

- pull-up resistors (I2C lines)  
- base resistor for transistor switching  
- filtering components  

These are essential for:
- signal integrity  
- stable communication  
- safe operation of switching elements  

---

## Design Characteristics

Compared to the EasyEDA version, this KiCad design appears:

- cleaner and more structured  
- more modular  
- better organized around communication buses  
- closer to a manufacturable architecture  

This suggests it was intended as a **next iteration toward a real PCB implementation**.

---

## Intended Workflow

1. Sensors collect environmental and motion data  
2. Arduino Mega processes incoming data  
3. Data is:
   - logged to SD card  
   - transmitted via LoRa  
4. GPS provides position tracking  
5. Buzzer provides real-time feedback  
6. System powered through regulated battery input  

---

## Why This Project Was Not Completed

This avionics system was developed as part of a **TEKNOFEST rocket project**, but due to various reasons, the overall project was **postponed before completion**.

As a result:

- hardware design remained unfinished  
- integration phase was not completed  
- testing and validation were not performed  

Despite this, the design is still valuable as:

- a reference for avionics architecture  
- a learning resource  
- a starting point for similar projects  

---

## Repository Purpose

This repository is shared to:

- document engineering work  
- provide insight into avionics system design  
- help others working on similar projects  
- keep unfinished work accessible instead of abandoned  

---
