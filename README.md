<h1 align="center">Microcontroller based DIY Smart Lock</h1>

<p align="center"><i>DIY Smart Lock with Arduino and RFID</i></p>

<p align="center">
    <img src="https://img.shields.io/badge/PROJECT-DIY%20SMART%20LOCK-E11D48?style=for-the-badge&logo=homeassistant&logoColor=white&labelColor=7F1D1D" alt="DIY Smart Lock" />
    <img src="https://img.shields.io/badge/BOARD-ARDUINO%20MEGA%202560-14B8A6?style=for-the-badge&logo=arduino&logoColor=white&labelColor=0F766E" alt="Arduino Mega 2560" />
    <img src="https://img.shields.io/badge/ACCESS-RFID%20MFRC522-8B5CF6?style=for-the-badge&logo=nfc&logoColor=white&labelColor=4C1D95" alt="RFID MFRC522" />
    <img src="https://img.shields.io/badge/TYPE-EMBEDDED%20SYSTEM-0EA5E9?style=for-the-badge&logo=microchip&logoColor=white&labelColor=1E3A8A" alt="Embedded System" />
</p>

<p align="center">
    <a href="#-project-intro"><img src="https://img.shields.io/badge/EXPLORE-PROJECT%20INTRO-6366F1?style=for-the-badge&logo=gitbook&logoColor=white&labelColor=4F46E5" alt="Project intro" /></a>
    <a href="#-components"><img src="https://img.shields.io/badge/VIEW-COMPONENTS-14B8A6?style=for-the-badge&logo=files&logoColor=white&labelColor=0F766E" alt="Components" /></a>
    <a href="#-project-structure"><img src="https://img.shields.io/badge/OPEN-PROJECT%20STRUCTURE-A855F7?style=for-the-badge&logo=readme&logoColor=white&labelColor=7E22CE" alt="Project structure" /></a>
</p>

## Table of Contents

- [🚀 Project intro](#-project-intro)
- [🧩 Components](#-components)
- [Features](#features)
- [Requirements](#requirements)
- [📁 Project structure](#-project-structure)
- [How to setup the project](#how-to-setup-the-project)
- [Troubleshooting](#troubleshooting)
- [📄 License](#-license)

## 🚀 Project intro

In this project, I have used an RFID reader (MFRC522), Arduino microcontroller (Mega 2560), Arduino programming language and other components to create an RFID-based smart lock. This lock is a small version of an automated RFID-based smart lock, an important component of an automated home.

## 🧩 Components

- Arduino. I've used a Mega 2560, though any Arduino board or clone will suffice.
- 3 x 220 ohm resistors
- 1 x 10k ohm resistor
- Logic-level N channel MOSFET
- MFRC522 module with at least two cards
- Red, blue, and green LEDs
- 12v Solenoid ($2)
- 12v power supply
- Breadboard and hook up wires

## Features

- RFID-based access control using the MFRC522 reader
- Master card programming for adding or removing authorized users
- EEPROM storage for saved RFID IDs so access records are retained after power loss
- Visual feedback through red, green, and blue LEDs
- Relay/MOSFET-controlled solenoid lock for door unlock action
- Wipe mode to clear stored RFID records when needed

## Requirements

### Hardware

- Arduino Mega 2560
- MFRC522 RFID module
- 12V solenoid lock or lock actuator
- Logic-level MOSFET/relay driver circuit
- LEDs and resistors
- 12V power supply
- Breadboard and jumper wires

### Software

- Arduino IDE
- MFRC522 library
- SPI and EEPROM libraries (already included with the Arduino core)
- Serial Monitor set to 9600 baud for debugging and setup

## 📁 Project structure

```txt
Microcontroller-based-DIY-Smart-Lock/
├── CSE323_PROJECT/
│   └── CSE323_PROJECT.ino
├── HARDWARE SETUP/
│   └── CSE323 Project Hardware Circuit setup.pdf
├── Delay-Timer-Circuit-using-IRFZ44N.jpg
├── Introduction-to-IRFZ44N_3.png.png
├── LICENSE
├── pinout-Arduino-Mega2560__1.png
├── pinout-Arduino-Mega2560__2.png
├── ProjectCode.zip
└── README.md
```

### Project setup

#### 📌 Pin diagram

The following Arduino Mega 2560 pin diagram shows the main board connections and pin layout used during the hardware setup.

<img src="pinout-Arduino-Mega2560__1.png" alt="Arduino Mega 2560 pin diagram" width="92%" style="display:block; margin:0 auto; max-height:280px; object-fit:contain;" />

### How to setup the project

Use the files in this repository in this order:

1. Open the hardware setup guide in `HARDWARE SETUP/CSE323 Project Hardware Circuit setup.pdf` to wire the Arduino Mega 2560, MFRC522 reader, LEDs, relay/MOSFET, and 12V solenoid correctly.
2. Open `CSE323_PROJECT/CSE323_PROJECT.ino` in the Arduino IDE and make sure the required libraries are available: `SPI.h`, `EEPROM.h`, and `MFRC522.h`.
3. Upload the sketch to the Arduino Mega 2560 using the pin mapping defined in the code:
   - MFRC522 RST → pin 5
   - MFRC522 SDA/SS → pin 53
   - SPI MOSI → pin 51
   - SPI MISO → pin 50
   - SPI SCK → pin 52
   - LEDs → pins 6, 8, and 10
   - Relay/MOSFET control → pin 11
   - Wipe button → pin 33
4. Power the circuit with the 12V supply and then open the Serial Monitor at 9600 baud to follow the setup process.
5. Scan a tag to define it as the master card, then use other RFID cards to grant or deny access. Press and hold the wipe button to clear stored RFID records if needed.

This setup is based on the main sketch, the hardware circuit guide, and the Arduino Mega pin diagram files included in the project folder.

### ⚙️ How it works

1. The Arduino boots and initializes the SPI communication with the MFRC522 reader.
2. The system waits for an RFID tag to be scanned.
3. If the scanned card matches the stored master card, the device enters programming mode.
4. In programming mode, new cards can be added or removed from EEPROM memory.
5. In normal mode, authorized tags unlock the solenoid for a short time, while unknown tags trigger the denied signal.
6. The wipe button can erase the stored access records when you want to reset the system.

### Troubleshooting

- If the MFRC522 reader is not detected, check the SPI wiring and ensure the correct SS/RST pins are connected.
- If the relay or solenoid does not respond, verify the MOSFET/relay driver circuit and the 12V supply.
- If the serial monitor shows no output, confirm that the board is connected and the baud rate is set to 9600.
- If cards are not being recognized, re-scan the master card and confirm the RFID library is installed correctly.

### 🎥 Demonstration

Watch the project demonstration video below to see the smart lock in action.

<p align="center">
  <a href="https://www.youtube.com/watch?v=GOO84CGBPz8" target="_blank" rel="noopener noreferrer">
    <img src="https://img.youtube.com/vi/GOO84CGBPz8/maxresdefault.jpg" alt="Smart Lock Demonstration" width="100%" style="max-width: 820px; border-radius: 12px;" />
  </a>
</p>

> Click the image above to open the YouTube video in a new tab.

## 📄 License

This project is licensed under the MIT License. See the `LICENSE` file for details.
