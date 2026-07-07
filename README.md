# Home Voltage & Current Protection System

Final Year Project · B.E. Electronics & Communication Engineering

An Arduino-based safety device that continuously watches household mains voltage and appliance current, cuts power automatically before a fault becomes a short circuit, and alerts the homeowner's phone by SMS — all without manual intervention.

**Author:** Vanjimuthu, B.E. ECE
**Project support:** Sankar and D.Sathiyan.

## What it does

- Monitors AC mains voltage and appliance current in real time using a **ZMPT101B** voltage sensor and an **ACS712** current sensor
- The moment a reading crosses a safe threshold, an **Arduino Uno** trips a relay and cuts appliance power in under a second — before a short circuit can occur
- Sounds a local buzzer and sends an **SMS alert** via a SIM800L GSM module, so the homeowner knows even when no one is home
- Power stays off until someone presses the manual reset button **and** the fault has actually cleared, preventing repeated damage

## Repository contents

| File | Description |
|---|---|
| `home_vi_protection_portfolio.html` | Interactive project portfolio — problem statement, system diagram, components table, core logic, and a live in-browser simulation with an animated building model (windows/fan power on and off with the simulated fault) |
| `README.md` | This file |

## Live demo

Open `home_vi_protection_portfolio.html` in any browser — no build step or server needed. Scroll to **Live demo** to:

1. Click **Start monitoring** to power the simulated building
2. Adjust the voltage/current sliders, or click **Inject overvoltage** / **Inject overcurrent** to simulate a fault
3. Watch the relay trip, the building's lights and fan cut out, and the SMS alert banner appear
4. Click **Reset system** to restore power

## Hardware components

| Part | Role |
|---|---|
| Arduino Uno | Reads sensors, applies threshold logic, drives outputs |
| ZMPT101B | Isolated AC voltage sensing module |
| ACS712 | Hall-effect current sensing module |
| 5V relay module | Switches appliance mains power on/off |
| SIM800L GSM module | Sends SMS alert to the homeowner's phone |
| Buzzer | Local audible alarm on fault |
| Push button | Manual reset once the fault has cleared |

## Safety note

This project senses and switches real 230V mains. It was built and demonstrated under faculty supervision using isolated, certified sensor modules and an enclosed relay stage. Do not attempt to wire mains-voltage circuits without proper training, isolation, and supervision.

## Skills demonstrated

Embedded C / Arduino · Analog signal processing · RMS measurement · Sensor calibration · Relay & power switching · GSM / AT commands · Fault-tolerant system design · Electrical safety practice
