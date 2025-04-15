# ESP32 Virtual Pet Project (M5StickC PLUS2)

## 1. Overview

This project aims to create an interactive virtual pet experience running on the M5StickC PLUS2 hardware platform. The pets will have unique stats, needs, and personalities. Key features include interaction based on real-world movement (detected via IMU), time-based needs (using the RTC), and potential communication between devices.

## 2. Hardware

* **Target Device:** M5StickC PLUS2
* **Key Utilized Components:**
    * ESP32-PICO-V3-02 Microcontroller (with WiFi & Bluetooth)
    * 1.14" Color TFT LCD (ST7789V2, 135x240)
    * MPU6886 6-Axis IMU (Accelerometer + Gyroscope)
    * BM8563 Real-Time Clock (RTC)
    * SPM1423 Microphone
    * Passive Buzzer
    * Programmable Buttons (A, B, C/Power)
    * IR Transmitter (Potential future use)
    * Built-in Battery + Charging Circuit

## 3. Software & Development Environment

* **Language/Framework:** C++ / Arduino Framework
* **IDE:** Visual Studio Code + PlatformIO IDE Extension
* **Key Libraries (Planned):**
    * `M5Unified`: For easy interaction with M5StickC PLUS2 built-in hardware (Display, IMU, RTC, Buttons, Buzzer, Mic, Power).
    * WiFi / Bluetooth Libraries (Standard ESP32): For device-to-device communication.
    * (Potentially) MQTT Client library (e.g., `PubSubClient`) or BLE libraries depending on communication method chosen.
    * (Potentially) Audio processing libraries (e.g., `arduinoFFT`) if pursuing direct audio communication experiment.
* **Version Control:** Git / GitHub

## 4. Core Features (Planned)

* **Virtual Pet Simulation:** Pets with individual stats (e.g., happiness, hunger, energy), needs that change over time (using RTC), and distinct personalities/types.
* **Movement Interaction:** Utilize the built-in IMU (MPU6886) to detect movement (e.g., step counting). Implement missions requiring physical activity (e.g., "Walk 500 steps with me!").
* **Audio Feedback:** Use the built-in buzzer for alerts, confirmations, and pet sounds.
    * **Custom Language Experiment:** Develop a unique pet "language" using patterns of tones/beeps. This language will encode digital information (pet status, requests) while sounding distinct and potentially reflecting emotion (modulated pitch/speed).
* **Device-to-Device Communication:** Allow pets on different M5StickC PLUS2 devices to interact.
    * **Primary Method (Planned):** Use WiFi or Bluetooth LE for data exchange (sending status codes, requests). Received data triggers local sound generation using the custom language.
    * **(Experimental Method):** Investigate direct communication via sound (buzzer output detected by microphone input on another device). Acknowledged as technically challenging.
* **Microphone Input:** Potential use for sound detection features or the audio communication experiment.
* **Progression:** Unlock new pet types, items, or features by completing missions or caring for the pet.
* **Persistent State:** Use NVS or SPIFFS/LittleFS on the flash memory to save pet status and progression across restarts.

## 5. Getting Started / Setup

1.  **Prerequisites:** Install Git, VS Code, and the PlatformIO IDE extension.
2.  **Clone:** Clone this repository to your local machine.
3.  **Open:** Open the cloned project folder in VS Code.
4.  **Dependencies:** PlatformIO should automatically detect the `platformio.ini` file and prompt to install necessary libraries (like `M5Unified`) upon opening or building.
5.  **Connect Hardware:** Connect the M5StickC PLUS2 via USB-C.
6.  **PlatformIO Actions:** Use the PlatformIO toolbar or commands:
    * `Build`: Compile the code.
    * `Upload`: Compile and flash the firmware to the device.
    * `Monitor`: Open the serial monitor to view output/debug messages.

## 6. Project Status

* **Current Status:** Paused (As of YYYY-MM-DD) - Awaiting hardware arrival.
* **Phase:** Initial planning and feature definition complete. Basic project structure set up on GitHub.

## 7. Future Ideas / Roadmap

*(Add any other brainstormed ideas here later)*

* IR communication?
* More complex mini-games?
* Web interface for status?

## 8. License

*(Refer to your LICENSE file here if you added one, e.g., MIT License)*
