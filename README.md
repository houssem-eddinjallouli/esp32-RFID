ESP32/RFID Door Unlock System
Unlock your door using an RFID tag and an ESP32. This project involves wiring an RFID reader to an ESP32 microcontroller and using a relay to control a door lock. Follow the steps below to set up the system.

Steps to Set Up
1. Wiring the RFID RC522 to ESP32
Connect the RFID RC522 reader to the ESP32 as follows:

SDA (SS): Connect to GPIO 22 (or another available GPIO pin)
SCK (CLK): Connect to GPIO 19
MOSI: Connect to GPIO 23
MISO: Connect to GPIO 25
IRQ: Not connected (optional)
GND: Connect to GND
RST: Connect to GPIO 27
3.3V: Connect to 3.3V (VCC)
2. Wiring the Relay to ESP32
Connect the relay to the ESP32 as follows:

GND: Connect to GND
In1: Connect to GPIO 5
VCC: Connect to 3.3V (VCC)
Then, wire the relay to your door lock or any other device you want to control.

3. Software Setup
Install the Arduino IDE.
Install the ESP32 board package in the Arduino IDE.
Install the MFRC522 library for the RFID reader.
4. Programming the ESP32
Use the first provided code, reader-code, to get the UID of each RFID card.
Replace the placeholder UIDs in the second code, system-code, with the UIDs you want to register.
Upload the system-code to the ESP32 to enable the system to open the relay when a registered card is detected.