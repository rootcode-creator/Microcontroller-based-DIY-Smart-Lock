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
- [📁 Project structure](#-project-structure)
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

## 📁 Project structure

```txt
Microcontroller-based-DIY-Smart-Lock/
├── CSE323_PROJECT/
│   └── CSE323_PROJECT.ino
├── HARDWARE SETUP/
├── LICENSE
└── README.md
```

### Project setup

#### Pin diagram

The following Arduino Mega 2560 pin diagram shows the main board connections and pin layout used during the hardware setup.

<img src="pinout-Arduino-Mega2560__1.png" alt="Arduino Mega 2560 pin diagram" width="100%" />

### Demonstration

Watch the project demonstration video below to see the smart lock in action.

<iframe width="100%" height="420" src="https://www.youtube.com/embed/GOO84CGBPz8" title="Smart Lock Demonstration" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

## 📄 License

This project is licensed under the MIT License. See the `LICENSE` file for details.
