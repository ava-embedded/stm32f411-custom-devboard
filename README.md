# STM32F411CEU6 Custom Development Board (Black Pill)

Custom-designed development board for the STM32F411CEU6 microcontroller,
built as a fully functional alternative to the standard Black Pill —
with integrated measurement and control capabilities.

## Why I Built This
I needed a development platform that exposed all GPIOs and peripherals
of the STM32F411CEU6, while also integrating sensing and power control
into a single board — instead of wiring external modules every time.

## Hardware Features
- Full STM32F411CEU6 minimum system (crystals, decoupling capacitors,
  reset circuit)
- USB-C connector for power and communication
- Integrated ST-Link programmer — no external programmer needed
- Integrated ammeter and voltmeter via op-amp circuits and precision
  resistor arrays
- Power stage with MOSFET for water pump control (high-load switching)
- Ultrasonic sensor input for automatic water level detection
- WiFi module connector (AP mode) for real-time web dashboard

## Firmware Features
- PWM control of MOSFET based on ultrasonic sensor distance
- Real-time display via WiFi AP web interface:
  → Water level (ultrasonic distance)
  → PWM duty cycle applied to MOSFET
  → Current and voltage readings
- Simultaneous serial output of all the same data

## Tech Stack
- Firmware: C++ (STM32CubeIDE)
- PCB Design: EasyEDA
- Web Interface: HTML / JavaScript
- Communication: UART serial + WiFi AP mode

## Files
- `/hardware` — Schematic (PDF), PCB layout, Gerber files
- `/firmware` — C++ source code
- `/photos` — PCB assembled and system running

## Author
Adrian Valle Araujo
Embedded Systems Engineering Student — Universidad Politécnica de Yucatán
linkedin.com/in/adrianvalle-388920389
