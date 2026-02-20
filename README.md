# Physical Spotify Player (RFID-Based)

A physical Spotify player inspired by the RFID Record Player project by fatihak.

This project keeps the original idea of controlling Spotify playback using RFID tags, but focuses heavily on a complete hardware redesign and internal optimization.

##  Overview

This device enables physical interaction with Spotify through RFID tags.

Each tag represents an album, a playlist, or a specific playback action. When a tag is placed on the reader, the Raspberry Pi detects it and triggers the corresponding Spotify playback.

The goal of this version is to create a cleaner, more compact, and professionally organized hardware implementation.

##  Raspberry Pi Compatibility

The project can be built using either a Raspberry Pi 5 or a Raspberry Pi Zero 2 W.

Custom 3D models are designed specifically for each Raspberry Pi version. The internal structure is adapted depending on the selected board, and the PCB and wiring layout are designed to support both configurations.

This allows you to choose between the higher performance of the Raspberry Pi 5 or the smaller size and lower power consumption of the Raspberry Pi Zero 2 W, without changing the overall experience of the device.

##  Hardware Redesign

This is not simply a rebuild of the original project. It is a hardware-focused redesign.

The enclosure has been completely redesigned with optimized internal space and dedicated versions for each Raspberry Pi model.

The internal layout has been reorganized to improve component placement, cable routing, and overall maintainability.

A custom PCB is being developed to centralize connections, reduce loose wiring, improve electrical reliability, and create a more modular structure.

The wiring system is optimized to reduce clutter and create a more compact and refined internal assembly.

## Hardware Components

Raspberry Pi 5 or Raspberry Pi Zero 2 W
RC522 RFID Reader
A3144 Hall Effect Sensor
28BYJ-48 Stepper Motor with ULN2003 driver

## Goals

The main objective is to improve hardware organization, create a compact and refined physical device, maintain compatibility with the original software concept, and deliver a more polished and maintainable version of the project.
