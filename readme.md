Firmware Demo English version: 
Please also read the file ManualEggIncubator V.2.03.docx

Combinations that are already Run ON:

Aeduino IDE Version: 2.3.2

Date: 2024-02-20T10:04:35.814Z

CLI Version: 0.35.3

Copyright © 2025 Arduino SA

Board: esp32 by Espressif System Versi 2.0.14

Library:

Adafruit Bus IO Versi 1.17.4

Adafruit Unified Sensor Versi 1.1.15

Arduinojson by Benoit B Versi 7.4.2

https://github.com/ESP32Async/AsyncTCP Versi 3.4.10

https://github.com/adafruit/DHT-sensor-library Versi 3.4.6

https://github.com/ESP32Async/ESPAsyncWebServer Versi 3.9.5

https://github.com/MajicDesigns/MD_MAX72XX Versi 3.5.1

https://github.com/MajicDesigns/MD_Parola  Versi 3.7.5

https://github.com/adafruit/RTClib Versi 2.1.4

Arduino Tools Setting :

Board             : "ESP32-DEV-MODULE"

Upload Speed      : "115200"

Flash Size        : 4MB (32Mb)

Partition Schema  : "Huge APP (3MB No OTA 1MB LittleFS)"

Events Run On     : "Core 0"

Arduino Runs On   : "Core 1"

#define CLK_PIN  18

#define CS_PIN    5

#define DATA_PIN 23

#define myBuzzer     26 

#define myHeater     27

#define myFan        19

#define myHumidifier 17

#define myEggTurner  16

#define LedBuiltIn    2 


Important Summary from Arduino IDE Log

From the log:

Board: ESP32

Flash Size: 4MB

Partition scheme: huge_app

LittleFS start address: 👉 0x310000 (THIS IS THE MOST IMPORTANT)

Flash mode: dio

Flash freq: 80m

Crystal: 80MHz

⚙️ Flash Download Tool Settings (Must Match Arduino)

In flash_download_tool_3.9.9_R2.exe:

ChipType: ESP32

SPI MODE: DIO

SPI SPEED: 80MHz

FLASH SIZE: 4MB

COM Port: COM5

Baudrate: 115200

✔️ Check all files to be flashed

✅ Safe Flashing Order

Erase Flash (if switching from another firmware)

Flash bootloader

Flash partition

Flash firmware (.ino.bin)

Flash littlefs.bin

Complete Guide:

🧩 flash_download_tool_3.9.9_R2.exe Configuration Layout

🔹 1. Initial Mode Selection

Chip Type: ESP32

WorkMode: Develop

Click OK

🔹 2. File List Setup (Middle Section)

Check ✔️ and set the addresses EXACTLY as follows:

[✔] EggIncubator_ESP32_V203_DHT22_DS3231_en.ino.bootloader.bin   → 0x1000

[✔] EggIncubator_ESP32_V203_DHT22_DS3231_en.ino.partitions.bin   → 0x8000

[✔] EggIncubator_ESP32_V203_DHT22_DS3231_en.ino.bin              → 0x10000

[✔] EggIncubator_ESP32_V203_DHT22_DS3231_en.ino.littlefs.bin     → 0x310000

⚠️ IMPORTANT

LittleFS MUST be at 0x310000 (according to huge_app)

Do NOT change the address order

🔹 3. Flash Settings (Right Section)

Must match Arduino IDE:

SPI MODE: DIO

SPI SPEED: 80MHz

FLASH SIZE: 4MB

COM: COM5 (change it to your port)

BAUDRATE: 115200

🔹 4. Additional Options (Recommended)

✔️ Erase Flash → enable (only once, especially when changing firmware)

❌ DoNotChgBin → DO NOT check

▶️ 5. Flashing Process

Press START

If not connected:

Press and hold the BOOT button on the ESP32

Release it when flashing starts

Wait until the status shows FINISH / SUCCESS

✅ Signs of SUCCESSFUL Flashing

No red error messages

ESP32 resets automatically

Web / LittleFS accessible normally

No reboot loop


🧠 Troubleshooting Tips

Blank web page / 404 → LittleFS address is incorrect

Continuous reset → firmware & partition mismatch

Connection failed → press & hold BOOT while clicking START

Slow / failed flashing → lower baudrate to 74880 or 115200


Debug Output:

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

Dashboard Display (Bottom Section):

Status: Registered @Isokunitech
==========================================================================================
This demo version only displays limited features.

Full Version:

Obtained through user registration.

After registration, proceed with the license payment according to the applicable terms.

Once the payment is verified, you will receive an activation code. Enter the code into the firmware to unlock all features.

Contact for Full Version & Activation: langgengbintoro@gmail.com






