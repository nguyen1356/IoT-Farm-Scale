# IoT-Farm-Scale
IoT Smart Farm Scale: Solar-optimized, automatic Big Data collection, and remote Tare/Calib via MQTT.


## 📝 Project Overview
This project focuses on building a smart electronic scale for high-tech agriculture. It automatically collects weight data from afar and is highly energy-efficient, making it perfect for off-grid farms.

## 🎯 Objectives
* **Automation:** Reduces manual measuring work by sending data directly to the Cloud.
* **Off-Grid Operation:** Uses solar power and power-saving modes to run reliably for a long time.
* **Big Data Collection:** Provides accurate, periodic data to help analyze crop growth trends.

## 🛠 Key Features

### 1. Smart Power Management
* **Hybrid Power:** Combines a 2Ah Lithium battery with a Solar Panel.
* **Deep Sleep:** Optimizes the ESP8266 microcontroller to "wake up" only when it needs to measure and send data.
* **Peripheral Control:** Automatically cuts off power to the HX711 sensor when not in use to save battery.

### 2. Dual Operating Modes
* **Continuous Mode:** Real-time tracking via Web/App, useful when you need to monitor quick weight changes.
* **Interval Mode:** Wakes up every 15 minutes between 6:00 AM and 6:00 PM. This is the main mode for collecting Big Data.

### 3. Reliability & Fail-Safe
* **WiFiManager:** Easy network setup via a Web interface without modifying the code.
* **Fail-Safe Logic:** Automatically goes to sleep after 10-15 seconds if it can't connect to WiFi or MQTT, preventing battery drain.
* **NVS Storage:** Saves calibration settings (Calibration factor/Offset) to the Flash memory, keeping it accurate even after a restart.

### 4. High Efficiency
* **Protocol:** Uses MQTT with lightweight JSON data format.
* **Fast Processing:** A complete working cycle takes only 8 to 15 seconds, which is excellent for battery-powered IoT devices.

## 🔄 System Flowchart
The chart below shows the complete cycle of the system: from starting up, checking the mode, measuring, sending data, to going into deep sleep to save power.

*(Bạn hãy thay `ten-file-anh.jpg` bằng tên ảnh lưu đồ thực tế mà bạn đã upload vào mục images nhé)*
![System Flowchart](images/ten-file-anh.jpg)

## ✅ Project Results
* **Outstanding Energy Savings:** By reducing the active time to just 8-15 seconds per cycle and cutting power to the sensor, the system runs smoothly for days even with low sunlight.
* **Fail-Safe Protection:** The device detects network loss and safely goes to sleep, preventing system crashes or wasted energy.
* **Easy Remote Management:** Essential controls like resetting to zero (Tare) or adjusting accuracy (Calib) can be done directly from the Dashboard without physically touching the device.
* **Standardized Data:** Data is packed in standard JSON format and sent stably to the Server, making it ready for Big Data analysis.

## 🚀 Future Plans
* Upgrade from the current prototype to a complete custom PCB (using SMD ESP8266 chips).
* Develop an advanced Data Analytics Dashboard to predict crop yields based on the collected data.
