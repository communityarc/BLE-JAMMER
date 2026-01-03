```txt
     ██╗ █████╗ ███╗   ███╗███╗   ███╗███████╗██████╗
     ██║██╔══██╗████╗ ████║████╗ ████║██╔════╝██╔══██╗
     ██║███████║██╔████╔██║██╔████╔██║█████╗  ██████╔╝
██   ██║██╔══██║██║╚██╔╝██║██║╚██╔╝██║██╔══╝  ██╔══██╗
╚█████╔╝██║  ██║██║ ╚═╝ ██║██║ ╚═╝ ██║███████╗██║  ██║
 ╚════╝ ╚═╝  ╚═╝╚═╝     ╚═╝╚═╝     ╚═╝╚══════╝╚═╝  ╚═╝

```

## BLE Jammer Firmware (ESP32 + nRF24L01)

Professional embedded firmware for **ESP32** utilizing **dual nRF24L01 transceivers** to perform controlled BLE interference research in a lab environment.  
Designed with a clean architecture, deterministic hardware mapping, and push‑button control.

> ⚠️ **Legal Notice:** Radio jamming and intentional interference may be illegal in many regions.  
> This project is intended **strictly for educational, defensive research, and controlled laboratory testing** on equipment you own or are explicitly authorized to test.

---

## ✨ Key Characteristics

- Dual **nRF24L01** radios (HSPI + VSPI)
- ESP32-based architecture
- Deterministic SPI pin mapping
- Push-button controlled operation
- Modular, hardware-focused firmware design
- Suitable for BLE security research and RF experimentation

---

## 🧠 System Overview

The firmware initializes **two independent SPI buses** on the ESP32 to control two nRF24L01 modules simultaneously.  
A physical push button is used to trigger operational logic, allowing deterministic testing workflows without serial interaction.

This architecture enables:
- Parallel RF operations
- Stable timing behavior
- Reduced bus contention
- Clean separation of hardware responsibilities

---

## 🔧 Hardware Requirements

| Component | Description |
|--------|------------|
| Microcontroller | ESP32 |
| RF Module | nRF24L01 × 2 |
| Input | Push Button |
| Power | Stable 3.3V (external regulator recommended) |

---

## 🔌 Pin Configuration

### nRF24L01 – HSPI Bus
| Signal | GPIO |
|------|------|
| SCK  | 14 |
| MISO | 12 |
| MOSI | 13 |
| CS   | 15 |
| CE   | 16 |

### nRF24L01 – VSPI Bus
| Signal | GPIO |
|------|------|
| SCK  | 18 |
| MISO | 19 |
| MOSI | 23 |
| CS   | 21 |
| CE   | 22 |

### Control Input
| Component | GPIO |
|--------|------|
| Push Button | 33 |

---

## ⚙️ Software Platform

- Arduino framework for ESP32
- SPI-based RF control
- Hardware‑oriented firmware structure

---

## 🧪 Intended Research Use

- BLE resilience testing
- RF interference analysis
- Wireless protocol research
- Embedded systems experimentation
- Defensive security validation

---

## 🚫 Ethical & Legal Disclaimer

This firmware **must not** be used:
- In public RF environments
- Against third‑party devices
- In violation of local laws or regulations

The author assumes **no responsibility** for misuse.

---

## 📄 License

MIT License  
Use, modify, and distribute with attribution.

---

## 👤 Author

**ARC – BLE Jammer Project**  
Focused on low‑level RF research and embedded system design.
