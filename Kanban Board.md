---

kanban-plugin: board

---

## 🦾In Progress

- [ ] Procure hardware (XIAO ESP32S3, SG90 servos, Pi, cables, power, etc.)
- [ ] Design Camera Base
- [ ] Assemble each camera node (connect camera + servo to XIAO)


## 🛠️ Epic 1: Hardware Setup and Wiring

- [ ] Power decision: finalize USB vs. solar (stick with USB for now)
- [ ] Setup Raspberry Pi (install Raspberry Pi OS, enable SSH, update)
- [ ] Validate hardware (servo sweep test, camera cable seated properly)


## 🌐 Epic 2: Networking Architecture

- [ ] Evaluate home Wi-Fi vs. mesh vs. dedicated subnet
- [ ] Finalize network setup (use home Wi-Fi initially)
- [ ] Assign static IPs or use mDNS for each node
- [ ] Test Wi-Fi signal strength at install locations
- [ ] Confirm ESP32 nodes can ping the Pi


## 🎥 Epic 3: Node Firmware – Camera + Servo

- [ ] Setup Arduino IDE / PlatformIO for XIAO ESP32S3
- [ ] Configure camera pins for OV2640 on XIAO (via `camera_pins.h`)
- [ ] Implement MJPEG video stream server (`/stream`)
- [ ] Control SG90 servo via PWM (test pan from sketch)
- [ ] Add HTTP endpoints for panning (`/pan?dir=left`, `/pan?angle=90`)
- [ ] Connect node to Wi-Fi and serve its stream
- [ ] Add optional OTA firmware update functionality
- [ ] Flash and deploy to all camera nodes


## 💻 Epic 4: Raspberry Pi Dashboard

- [ ] Choose backend: Python + Flask
- [ ] Design stream aggregation (proxy or embed ESP streams)
- [ ] Build web UI to view all streams + control each servo
- [ ] Create REST API to send servo pan commands to nodes
- [ ] Map camera names to their IPs or hostnames
- [ ] Test dashboard locally (all 3 streams + servo control)


## 🔐 Epic 5: Hosting & Security

- [ ] Add login system (basic auth or Flask login)
- [ ] Decide on HTTPS setup (self-signed or Let's Encrypt)
- [ ] Harden Pi (change SSH port, enable firewall, strong passwords)
- [ ] Enable remote access (VPN or Tailscale recommended)
- [ ] Test security (access control, open ports, HTTPS test)


## ✅ Epic 6: Testing & Deployment

- [ ] Functional testing: all 3 cams stream and move
- [ ] Run 24-hour test to check stability
- [ ] Test camera Wi-Fi signal from install spots
- [ ] Install nodes in final locations
- [ ] Write deployment docs (IP map, access info, update process)


## 🧱 Epic 7: Future Expandability

- [ ] Add motion detection (OpenCV on Pi or PIR sensors on XIAO)
- [ ] Enable Pi to capture snapshot on motion
- [ ] Save clips or photos to Pi (file system or USB drive)
- [ ] Add door/window sensor node (reed switch to ESP32C3)
- [ ] Send alerts (email, Pushover, etc.)
- [ ] Explore mobile app or PWA version of dashboard
- [ ] Add more cameras and test performance
- [ ] Research RTSP/WebRTC options for higher efficiency
- [ ] Integrate with Home Assistant (use MJPEG URL or custom component)


## Blocked



## Done





%% kanban:settings
```
{"kanban-plugin":"board","list-collapse":[null,false,false,false]}
```
%%