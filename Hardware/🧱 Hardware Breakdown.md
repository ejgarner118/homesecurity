This document outlines the hardware used in the **Modular ESP32S3 Security Camera Network** project.

Each **Camera Node** consists of a Seeed Studio XIAO ESP32S3 Sense microcontroller with an OV2640 camera module, a micro servo motor for panning, and basic supporting components. A **Raspberry Pi** serves as the central hub/server.

---

## 📦 Bill of Materials (BOM)

### 🧠 Microcontroller Units

| Item                                    | Qty | Description                                                                  | Link         |
| --------------------------------------- | --- | ---------------------------------------------------------------------------- | ------------ |
| Seeed Studio XIAO ESP32S3 Sense         | 3+  | ESP32S3 board with 8MB PSRAM, 8MB Flash, USB-C, camera connector, BLE, Wi-Fi | Product Page |
| OV2640 Camera Module (comes with Sense) | 3+  | 2MP camera sensor for XIAO Sense                                             | Included     |
| ~~XIAO Expansion Board (optional)~~         | ~~3+~~  | ~~Adds Grove connectors and microSD slot~~                                       | ~~Seeed~~        |

---

### 🔧 Motion / Servo

|Item|Qty|Description|Link|
|---|---|---|---|
|SG90 Micro Servo|3+|9g micro servo motor, ~180° range, runs on 5V|[Amazon](https://www.amazon.com/s?k=sg90+servo) / Adafruit|
|Servo Mount or Bracket|3+|3D printed or off-the-shelf mount for secure rotation base|Custom / Print|

---

### ⚡ Power

| Item                    | Qty | Description                              | Link            |
| ----------------------- | --- | ---------------------------------------- | --------------- |
| USB-C Power Adapter     | 3+  | 5V 1–2A USB power brick                  | Anker / Generic |
| USB-C Cable             | 3+  | Power/data for XIAO board                | —               |
| ~~(Optional) LiPo Battery~~ | ~~0–3~~ | ~~Backup power via XIAO’s onboard charging~~ | ~~Seeed LiPo~~      |

---

### 🧠 Hub / Server

|Item|Qty|Description|Link|
|---|---|---|---|
|Raspberry Pi 4 Model B (or 3B+)|1|Central hub for viewing and managing streams|Raspberry Pi|
|16–32 GB microSD Card|1|For OS and software|—|
|Pi Power Supply (5V 3A)|1|Stable power for Pi|—|
|USB Keyboard/Mouse/HDMI (setup only)|1 set|For initial setup (or use SSH)|—|

---

### 📡 Networking

| Item                                   | Qty | Description                         | Notes               |
| -------------------------------------- | --- | ----------------------------------- | ------------------- |
| Existing Home Wi-Fi Network            | 1   | For ESP32 nodes and Pi connectivity | 2.4GHz preferred    |
| ~~Wi-Fi Extender or Mesh Node (optional)~~ | ~~0–2~~ | ~~If some cameras are out of range~~    | ~~TP-Link, Eero, etc.~~ |

---



## 📋 Estimated Cost Breakdown (per camera node)

|Component|Cost (USD)|
|---|---|
|XIAO ESP32S3 Sense|$13–18|
|SG90 Micro Servo|$2–4|
|USB-C Cable + Power Adapter|$5–8|
|(Optional) Mount/enclosure|$1–3|
|**Total per node**|**~$20–30**|

**Raspberry Pi Hub:** ~$35–70 depending on model and what you already have.

---

## 📝 Notes

- All ESP32S3 cameras are powered via USB — no solar needed for v1.
    
- Future BOM add-ons may include PIR sensors, door/window switches, or I2C expansion boards.
    
- Try to buy extras of critical parts (e.g., XIAOs, servos) to have backups or expand quickly.