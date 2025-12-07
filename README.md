# 🌊 SIF2026
**FPGA-Assisted Real-time Vibration Damping System for Semiconductor Equipment**

## 📖 Project Overview
반도체 노광 장비 등 초정밀 공정에서 발생하는 미세 진동을 능동적으로 제어(Active Damping)하는 시스템입니다.
STM32 MCU가 실시간 PID 제어를 수행하고, FPGA가 고속 데이터 로깅 및 분석을 가속화하는 **Dual-Core Architecture**를 채택했습니다.

## 🚀 Key Features
- **Active Damping:** VCM(Voice Coil Motor) 액추에이터를 이용한 실시간 진동 상쇄
- **Hybrid Architecture:**
  - **MCU (STM32):** 1kHz Real-time PID Control loop
  - **FPGA (Artix-7):** High-speed Data Acquisition & Pre-processing
- **Real-time Monitoring:** Python(PyQtGraph) 기반의 60FPS 실시간 진동 시각화
- **Zero-Latency Response:** 스피커(VCM)의 빠른 응답성을 활용한 즉각적인 외란 제거

## 🛠️ Hardware Spec
- **Main Controller:** STM32 Nucleo-F446RE (Cortex-M4F @ 180MHz)
- **Data Accelerator:** Digilent Arty A7 (Xilinx Artix-7 FPGA)
- **Sensor:** MPU6050 (6-Axis IMU) via I2C
- **Actuator:** 3-inch Woofer Speaker (Modified VCM)
- **Driver:** L298N Dual H-Bridge

## 💻 Software Stack
- **Firmware:** STM32CubeIDE (C/C++), HAL Library
- **Hardware Logic:** Xilinx Vivado (Verilog HDL)
- **PC Application:** Python 3.9, PyQtGraph, PySerial

## 🎥 Demo
