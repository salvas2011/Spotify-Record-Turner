# Physical Spotify Player (RFID-Based)

A physical Spotify player inspired by the RFID Record Player project by fatihak.

This project keeps the original idea of controlling Spotify playback using RFID tags, but focuses heavily on a complete hardware redesign, internal optimization, and a full software rewrite for the ESP32-S3 platform.

## Overview

This device enables physical interaction with Spotify through RFID tags.

Each tag represents an album, a playlist, or a specific playback action. When a tag is placed on the reader, the ESP32-S3 detects it and triggers the corresponding Spotify playback.

The goal of this version is to create a cleaner, more compact, and professionally organized implementation.

## ESP32-S3

This project is built around the ESP32-S3-WROOM1, replacing the original Raspberry Pi approach with a more compact and power-efficient microcontroller platform.

Custom 3D models are designed specifically for this board. The internal structure, PCB, and wiring layout are all adapted to the ESP32-S3 form factor.

The software has been rewritten in C++ to run natively on the ESP32-S3, communicating directly with the Spotify Web API over WiFi.

## Hardware Redesign

This is not simply a rebuild of the original project. It is a hardware-focused redesign.

The enclosure has been completely redesigned with optimized internal space dedicated to the ESP32-S3 form factor.

The internal layout has been reorganized to improve component placement, cable routing, and overall maintainability.

A custom PCB is being developed to centralize connections, reduce loose wiring, improve electrical reliability, and create a more modular structure.

The wiring system is optimized to reduce clutter and create a more compact and refined internal assembly.

## Hardware Components

- ESP32-S3-WROOM1 (44 Pin, 16MB Flash, 8MB PSRAM)
- RC522 RFID Reader
- A3144 Hall Effect Sensor
- 28BYJ-48 Stepper Motor with ULN2003 driver

## Goals

The main objective is to improve hardware organization, create a compact and refined physical device, rewrite the software for the ESP32-S3 platform, and deliver a more polished and maintainable version of the project.

## Bill of Materials (BOM)

| Component | Quantity | Notes |
|-----------|----------|-------|
| ESP32-S3-WROOM1 (44 Pin, 16MB Flash, 8MB PSRAM) | 1 | Main controller |
| RC522 RFID Reader | 1 | Reads RFID tags representing albums or playlists |
| RFID Tags / Cards | Several | Used to trigger playback |
| A3144 Hall Effect Sensor | 1 | Detects the presence/position of the record |
| 28BYJ-48 Stepper Motor | 1 | Used for platter rotation |
| ULN2003 Stepper Motor Driver | 1 | Driver board for the stepper motor |
| 5V Power Supply | 1 | Power via USB-C |
| Custom PCB | 1 | Organizes connections between components |
| 3D Printed Parts | 1 set | Custom enclosure and internal structure |
| Jumper Wires / Connectors | As needed | Internal wiring |
| Magnets | 1-2 | Used for Hall sensor position detection |
