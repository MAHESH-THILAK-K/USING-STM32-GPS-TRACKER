# 📌 Project Overview

STM32-GPS-TRACKER is a compact, reliable, and industry-oriented GPS tracking system built around an **STM32 microcontroller** and the **SIM808 GSM/GPS module**. The system enables **real-time location tracking** and **cellular data transmission** for IoT and telemetry applications such as vehicle tracking, asset monitoring, and remote sensing.

The schematic and PCB are designed with **strong power integrity, EMI control, and manufacturability**, targeting a **4-layer PCB** suitable for real-world deployment.

---

## 🧩 System Architecture

| Block                    | Description                                           |
| ------------------------ | ----------------------------------------------------- |
| Power Input & Protection | Accepts 12 V input with fuse and surge protection     |
| DC-DC Regulation         | High-efficiency buck converter generates stable 3.3 V |
| Main Controller          | STM32 microcontroller manages system logic            |
| Communication Module     | SIM808 provides GSM + GPS functionality               |
| SIM Interface            | SIM card socket with ESD protection                   |
| RF Section               | U.FL connectors for GSM and GPS antennas              |
| User Interface           | Push buttons and status LEDs                          |
| Debug & Expansion        | SWD and header pins for programming and I/O           |

---

## 🔧 Core Controller – STM32 MCU

| Feature           | Description                  |
| ----------------- | ---------------------------- |
| MCU               | STM32 (ARM Cortex-M0 series) |
| Operating Voltage | 3.3 V                        |
| Clock Source      | External crystal oscillator  |
| Programming       | SWD (SWDIO, SWCLK, NRST)     |
| Communication     | UART interface to SIM808     |
| Control Signals   | SIM808 PWRKEY, RESET         |
| Indicators        | Status LEDs via GPIO         |

The STM32 acts as the **central controller**, handling GSM commands, GPS data processing, and system coordination.

---

## 📡 GSM/GPS Communication – SIM808

| Feature   | Description                          |
| --------- | ------------------------------------ |
| Module    | SIM808 GSM + GPS                     |
| GSM       | Cellular data communication          |
| GPS       | Satellite-based positioning          |
| Interface | UART (TX/RX)                         |
| Control   | Dedicated PWRKEY and RESET lines     |
| Antennas  | Separate GSM and GPS U.FL connectors |

The SIM808 enables **accurate positioning** and **wide-area data transmission**, making the system suitable for mobile and remote applications.

---

## 🔋 Power Design

| Feature       | Description                          |
| ------------- | ------------------------------------ |
| Input Voltage | 12 V DC                              |
| Regulator     | TPS5430 buck converter               |
| Output        | 3.3 V regulated rail                 |
| Filtering     | Bulk + ceramic decoupling capacitors |
| Protection    | Fuse and transient suppression       |

The switching regulator is designed to handle **high current bursts** from GSM transmission while maintaining voltage stability.

---

## 🛡️ SIM Card & Protection

| Feature             | Description                    |
| ------------------- | ------------------------------ |
| SIM Socket          | Standard SIM interface         |
| Signal Conditioning | Series resistors               |
| ESD Protection      | Dedicated ESD diode array      |
| Decoupling          | Local capacitor for SIM supply |

This ensures **reliable SIM operation** and protection against electrostatic discharge.

---

## 📶 RF & Antenna Design

| Feature       | Description                       |
| ------------- | --------------------------------- |
| GSM Antenna   | U.FL connector                    |
| GPS Antenna   | U.FL connector                    |
| Grounding     | Proper RF grounding and isolation |
| Layout Intent | Antenna keep-out zones respected  |

Designed to ensure **clean RF performance** and reduced interference.

---

## 🧪 PCB Design (4-Layer Optimized)

| Layer   | Purpose                       |
| ------- | ----------------------------- |
| Top     | Components and signal routing |
| Inner-1 | Solid GND plane               |
| Inner-2 | 3.3 V power plane             |
| Bottom  | Signal routing                |

Benefits:

* Low impedance power delivery
* Reduced EMI
* Stable GSM/GPS performance
* Improved thermal and electrical reliability

## 🚀 Engineering Notes

* Designed for **4-layer PCB manufacturing**
* Robust power integrity for GSM current spikes
* EMI-aware grounding and routing
* Modular and expandable design
* Suitable for academic, hobby, and industry use

---

## 👤 Author

**MAHESH THILAK (MTK)**
Embedded Systems | PCB Design | IoT | Robotics

---
