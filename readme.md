# Firmware Demo English Version
This demo version only displays limited features.

### 💎 Full Version
Obtained through user registration.
1. After registration, proceed with the license payment according to the applicable terms.
2. Once the payment is verified, you will receive an activation code.
3. Enter the code into the firmware to unlock all features.

**Contact for Full Version & Activation:**  
📞 [WhatsApp: 0813-1970-7919](https://wa.me)

> [!IMPORTANT]  
> Please also read the file `ManualEggIncubator V.2.03.docx`

---

## 🛠 Combinations & Environment
| Property | Value |
| :--- | :--- |
| **Version** | 2.3.2 |
| **Date** | 2024-02-20 |
| **Board** | ESP32 by Espressif System (v2.0.14) |
| **Copyright** | © 2025 Arduino SA |

### 📚 Libraries Used
- Adafruit Bus IO (v1.17.4)
- Adafruit Unified Sensor (v1.1.15)
- Arduinojson by Benoit B (v7.4.2)
- [AsyncTCP](https://github.com/ESP32Async/AsyncTCP) (v3.4.10)
- [DHT-sensor-library](https://github.com/adafruit/DHT-sensor-library) (v3.4.6)
- [ESPAsyncWebServer](https://github.com/ESP32Async/ESPAsyncWebServer) (v3.9.5)
- [MD_MAX72XX](https://github.com/MajicDesigns/MD_MAX72XX) (v3.5.1)
- [MD_Parola](https://github.com/MajicDesigns/MD_Parola) (v3.7.5)
- [RTClib](https://github.com/adafruit/RTClib) (v2.1.4)

### ⚙️ Arduino Tools Setting
```cpp
Board             : "ESP32-DEV-MODULE"
Upload Speed      : "115200"
Flash Size        : 4MB (32Mb)
Partition Schema  : "Huge APP (3MB No OTA 1MB LittleFS)"
Events Run On     : "Core 0"
Arduino Runs On   : "Core 1"

// Pin Mapping
#define CLK_PIN       18
#define CS_PIN         5
#define DATA_PIN      23
#define myBuzzer      26 
#define myHeater      27
#define myFan         19
#define myHumidifier  17
#define myEggTurner   16
#define LedBuiltIn     2 
Use code with caution.

📑 Important Summary from Arduino IDE Log
Board: ESP32
Flash Size: 4MB
Partition scheme: huge_app
LittleFS start address: 👉 0x310000 (CRITICAL)
Flash mode/freq: dio / 80m
⚙️ Flash Download Tool Settings
Configuration Layout (v3.9.9_R2):
SPI MODE: DIO
SPI SPEED: 80MHz
FLASH SIZE: 4MB
Baudrate: 115200
🔹 File List Setup (Addresses)
File Name	Address
bootloader.bin	0x1000
partitions.bin	0x8000
firmware.ino.bin	0x10000
littlefs.bin	0x310000
🚀 Flashing Process Guide
Initial Mode: Select Chip Type: ESP32 & WorkMode: Develop.
Erase Flash: Enable (recommended for first time).
Press START: If stuck, hold the BOOT button on ESP32 until flashing begins.
Finish: Wait for FINISH / SUCCESS status.
✅ Signs of Success
No red error messages.
ESP32 resets automatically.
Web / LittleFS accessible.
🧠 Troubleshooting
404 / Blank Page: LittleFS address is wrong (must be 0x310000).
Boot Loop: Firmware & partition mismatch.
Connection Failed: Hold BOOT button during START.
🖥 Debug Output
text
LittleFS mount Success...
📂 Files already exist, not writing default.
Init RTC Success!
DHT sensor Normal...
Connecting to WiFi: Smart-Router
...........
✅ Connected to WiFi!
IP: 192.168.1.109
WiFi mode active: STA
Ready to serve...
✅ Activation code stored
Use code with caution.

Dashboard Status: Registered @Isokunitech
