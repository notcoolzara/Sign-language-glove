# Sign Language Translation Glove Using Arduino Nano

## Overview
This project showcases a wearable glove capable of translating sign language gestures into readable text and transmitting it wirelessly to a mobile device. It utilizes **Arduino Nano**, **flex sensors**, an **MPU6050 gyroscope/accelerometer**, and an **HC-05 Bluetooth module**, providing a low-cost solution to bridge the communication gap for individuals relying on sign language.

---

## Features
- Detects and recognizes hand gestures using **flex sensors** and **MPU6050 motion data**.
- Translates gestures into text.
- Sends real-time translations to a connected mobile device via **Bluetooth**.

---

## Components
- **Arduino Nano**: Microcontroller for data processing.
- **Flex Sensors (x3)**: Measure finger bending.
- **MPU6050 Gyroscope/Accelerometer**: Detects hand motion and orientation.
- **HC-05 Bluetooth Module**: Enables wireless communication.
- **Miscellaneous Components**: Glove, wires, resistors.

---

## System Design
### 1. Hardware
- **Flex Sensors**: Capture finger bending values.
- **MPU6050**: Measures motion data (acceleration and gyroscope).
- **Bluetooth Communication**: Sends recognized gestures to a mobile device.

### 2. Software
The Arduino code implements:
- **Sensor Calibration**: Ensures consistent gesture recognition by storing calibration values in EEPROM.
- **Gesture Recognition**: Combines flex sensor and motion data to classify gestures.
- **Bluetooth Integration**: Sends detected gestures as text.

---

## How It Works
1. The system initializes and checks for calibration values stored in EEPROM.
2. Sensors capture data:
   - Flex sensor values are mapped and constrained between 0–1000.
   - Accelerometer and gyroscope data refine gesture recognition.
3. The code processes this data to identify gestures based on predefined conditions.
4. Recognized gestures are sent via Bluetooth to a mobile device.

---

## Gestures Detected
- **Thumbs Up**
- **Victory**
- **Thank You**
- **Sorry**
- **I Love You**
- ...and more!

---

## Setup Instructions
1. **Assemble the hardware**:
   - Attach flex sensors to the glove.
   - Connect MPU6050 and HC-05 as per wiring diagram.
2. **Upload Code**:
   - Use Arduino IDE to upload the provided code to the Arduino Nano.
   - Ensure required libraries (Adafruit_MPU6050, SoftwareSerial) are installed.
3. **Calibrate Sensors**:
   - On the first run, the system calibrates flex sensors. Follow the serial output for instructions.
4. **Test Gestures**:
   - Wear the glove and perform gestures to see text output on the connected mobile device.

---

## Wiring Diagram
![Screenshot 2025-01-09 115334](https://github.com/user-attachments/assets/593008e9-9d82-4af3-9e39-3cccf9b59c4b)
![Screenshot 2025-01-09 115535](https://github.com/user-attachments/assets/b7b9eb67-828a-4d95-a8a7-b7d807148acc)
![Screenshot 2025-01-09 115929](https://github.com/user-attachments/assets/edf80a38-bbd3-450a-b9f9-3d6221de67c7)

- Flex sensors are connected to **A2, A6, A7**.
- MPU6050 is interfaced via I2C.
- HC-05 Bluetooth module is connected to **D7 (RX)** and **D8 (TX)**.

---
## Acknowledgments
- Inspired by the [Sensor Glove for Sign Language Translation](https://projecthub.arduino.cc/ayooluwa98).
