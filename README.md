# Vehicle_Stability-_Assistance_System-ESP-TCS-ABS-

## Table of Contents
- [Introduction](#introduction)
- [Problem Statement](#problem-statement)
- [Objectives](#objectives)
- [Design Methodology](#design-methodology)
- [Expected Components](#expected-components)

---

## Introduction

Safety braking systems are a critical component of modern vehicles that help prevent accidents and reduce the severity of collisions. These systems work in conjunction with the driver, using advanced sensors and computer technology, to detect potential hazards and automatically apply the brakes to avoid or mitigate collisions.

Instead of using hydraulic fluid to transmit braking force, brake-by-wire systems use electronic signals. The **Electronic Control Unit (ECU)** is the core component that processes information from various sensors and makes split-second decisions to activate braking components.

---

## Problem Statement

During critical maneuvers, such as obstacle avoidance, vehicles can easily lose control due to excessive skidding. Significant lateral forces act on the tires, affecting the yaw moment and orientation of the vehicle, especially during high-speed steering maneuvers.

To address these challenges, the **Electronic Stability Program (ESP)** was introduced to enhance vehicle control in such scenarios.

- **Oversteering**: The rear end of the car loses traction during a turn.
- **Understeering**: The front end of the car loses traction, causing the vehicle to slide forward during a turn.

ESP helps to control these behaviors and prevent instability during critical maneuvers such as lane changes with emergency braking.

![2](https://github.com/user-attachments/assets/5357577d-6244-4c88-9c64-05b182a603f9)


---

## Objectives

The **Electronic Stability Program (ESP)** is designed to improve vehicle stability by:

- Enhancing braking efficiency by applying brakes selectively to specific wheels.
- Preventing wheel lock-up during hard braking, allowing the driver to maintain steering control.
- Reducing skidding or sliding, especially in challenging driving conditions.
- Preventing drive wheels from losing traction during acceleration.

![Capture](https://github.com/user-attachments/assets/747e318d-d4d6-44e4-b839-8bd4fd314dce)


## Design Methodology

Our methodology is based on **Model-Based Development (MBD)** with the following phases:

1. **System Modeling**:
   - Develop accurate mathematical models of the vehicle's dynamics.
   
2. **Develop Control Algorithm using MATLAB/Simulink**:
   -  Design robust control algorithms to detect and counteract 
      vehicle instability using one or more than one of advanced 
      control algorithms like ( PID, Fuzzy logic , LQR, MPC ).
   
3. **Integration with Software Architecture**:
   - Auto-generated code in MATLAB can be used 
    to implement software application layer (SAL).
     A SAL is a layer of code that provides a 
    higher-level abstraction of the underlying 
    hardware or software components.
     Then we will implement the drivers of the 
    other layers e.g.: HAL & MCAL.
![4](https://github.com/user-attachments/assets/9082aba2-fe15-4e41-902b-09ec8589fa7a)


   
4. **Testing and Validation**:
   - Using
   -  **Software-in-the-Loop (SIL)**
   - Initial testing where software is tested in isolation from hardware using 
    simulated or emulated interfaces.
   - **Model-in-the-Loop (MIL)**
   - Testing of mathematical or computational models of a system to ensure 
    their accuracy and reliability before integrating them with software or hardware
   -  **Hardware-in-the-Loop (HIL)**
      Final testing stage where software and hardware are tested together 
      using real hardware interfaces to validate the system's functionality under realistic conditions. MATLAB 
      and Simulink are a powerful tool for HIL testing. Simulink can be used to create detailed models of 
      physical systems, and MATLAB can be used to generate real-time code from these models. This code 
      can then be run on a target hardware platform, such as a real-time controller
5. **Deployment to Embedded Target**:
   - Transfer the developed and tested Electronic Stability Program (ESP) software and control 
    algorithms from a development environment to an embedded system within the vehicle. 
    This deployment is conducted on a physical model for a real vehicle to ensure the system's 
    performance under actual operating conditions.

---

## Expected Components

- **ECUs**
- Raspberry Pi 4 Model B**
- STM32F446RE (NUCLEO-F446RE)**
- **Sensors**:
  - Yaw Rate Sensor
  - Lateral Acceleration Sensor
  - Steering Angle Sensor
  - Wheel Speed Sensor
  - Pressure Sensor
- **Hardware Tools**:
  - STLINK V2 Debugger
  - CAN Transceivers
 
  -- **Hydraulic Circuit**:
  -Pumps
  -Valves

