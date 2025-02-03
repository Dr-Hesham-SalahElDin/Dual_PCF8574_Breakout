# PCF8574 Dual I/O Expander Breakout Board

## Overview
This project is a **breakout board for two PCF8574 I/O expanders**, providing **16 digital I/O pins** (8 per expander) via **I²C communication**.  
The board allows users to configure the I²C addresses using **0Ω resistors**, making it flexible for different applications.

## Features
- **Dual PCF8574 ICs** providing **16 GPIOs**
- **I²C interface** for simple microcontroller integration
- **Configurable I²C addresses** using **0Ω resistors**
- **Onboard pull-up resistors** for I²C stability

## I²C Address Configuration
Each **PCF8574** has a **7-bit address**, where the lower 3 bits (`A2, A1, A0`) are user-configurable using **0Ω resistors**.

- **To set a bit to `0` (GND):** Solder the **0Ω resistor** between the address pin and **GND**.
- **To set a bit to `1` (VCC):** Solder the **0Ω resistor** between the address pin and **VCC**.

### Example Address Configurations
| A2 | A1 | A0 | I²C Address |
|----|----|----|------------|
| 0  | 0  | 0  | `0x20` |
| 0  | 0  | 1  | `0x21` |
| 0  | 1  | 0  | `0x22` |
| 0  | 1  | 1  | `0x23` |
| 1  | 0  | 0  | `0x24` |
| 1  | 0  | 1  | `0x25` |
| 1  | 1  | 0  | `0x26` |
| 1  | 1  | 1  | `0x27` |
