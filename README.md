#  RFID Record Player — ESP32-S3

> A modern record player that uses RFID-tagged vinyl coasters to control Spotify playback, powered by an ESP32-S3 and a custom PCB.

---

## How it works

Place a tagged vinyl coaster on the platter. The RFID reader identifies the tag, looks up the mapped Spotify URI, and starts playback. A Hall effect sensor detects when the platter is spinning — remove the record and the music pauses automatically. A stepper motor keeps the platter spinning for the full vinyl experience.

---

## PCB

<p align="center">
  <img src="IMG/Captura de ecrã 2026-06-04 003256.png" alt="KiCad Schematic" width="48%"/>
  &nbsp;
  <img src="IMG/Captura de ecrã 2026-06-04 000926.png" alt="PCB Layout" width="48%"/>
</p>

<p align="center">
  <em>Left: KiCad schematic &nbsp;·&nbsp; Right: PCB layout</em>
</p>

---

## Components

| Component | Purpose |
|---|---|
| ESP32-S3-DEV-KIT-N8R8 | Main microcontroller, Wi-Fi |
| RC522 RFID Reader | Reads RFID/NFC tags |
| 28BYJ-48 + ULN2003 | Stepper motor for spinning platter |
| A3144 Hall Effect Sensor | Detects platter rotation |
| NTAG213 NFC Tags | Attached to vinyl coasters |

---

## Wiring

### RC522 RFID (SPI)

| ESP32 GPIO | RC522 Pin |
|---|---|
| GPIO11 | MOSI |
| GPIO13 | MISO |
| GPIO12 | SCK |
| GPIO10 | CS (SDA) |
| GPIO9 | RST |
| 3.3V | 3.3V |
| GND | GND |

### ULN2003 Stepper Motor

| ESP32 GPIO | ULN2003 Pin |
|---|---|
| GPIO4 | IN1 |
| GPIO5 | IN2 |
| GPIO6 | IN3 |
| GPIO7 | IN4 |
| 5V (external) | VCC |
| GND | GND |

### A3144 Hall Effect Sensor

| ESP32 GPIO | Sensor Pin |
|---|---|
| GPIO38 | OUT |
| 3.3V | VCC |
| GND | GND |

### Power

5V 2A via barrel jack wired directly to the ESP32-S3 5V and GND pins.

---

## Pin notes

- GPIO35, 36, 37 are reserved internally on the N8R8 variant (Octal PSRAM) — do not use
- GPIO0 and GPIO46 are strapping pins — avoid for general use
- GPIO19/20 are USB D-/D+ — avoid if using native USB

---


## License

MIT
