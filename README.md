# AC to DC Power Supply — 220V to 24V DC Conversion

A regulated DC power supply system designed at Helwan National University, 
Robotics and Mechatronics Department. The system converts 220V AC mains 
input to a stable, adjustable 24V DC output using a bridge rectifier, 
LC filtering, MOSFET switching, and an LM317T voltage regulator.

## How It Works
AC input is stepped down via transformer, full-wave rectified by a 1N4007 
bridge, filtered through bulk capacitors, switched by a PWM-controlled 
MOSFET (IRF9530N) via IR2112 gate driver, passed through an LC filter, 
and regulated by an LM317T with potentiometer-based voltage adjustment. 
Arduino Uno reads output voltage via a resistor divider and controls 
PWM duty cycle accordingly.

## Components
- Transformer (220V → 24V)
- Bridge Rectifier (1N4007)
- Bulk Capacitors: 2800µF, 6800µF, 1nF
- MOSFET: IRF9530N (P-channel, high-side switch)
- Gate Driver: IR2112
- Inductor: 100µH
- Output Capacitors: 2× 680µF
- Voltage Regulator: LM317T (adjustable)
- Potentiometer: 1000Ω (output voltage control)
- Feedback Resistors: 1kΩ, 220Ω
- Arduino Uno (ATmega328P) — PWM generation & voltage sensing

## Key Pin Connections
| Signal | Arduino Pin |
|---|---|
| PWM to MOSFET gate (via R1 100Ω) | D9 |
| Voltage feedback (R2/R3 divider) | A0 |

## Technologies
`Arduino` `C Programming` `PWM Control` `LM317T` `MOSFET Switching` 
`Bridge Rectifier` `LC Filter` `Power Electronics` `Proteus Simulation`

## Repository Contents
- `/code` — Arduino sketch (.ino)
- `/schematics` — Proteus circuit diagram
- `/report` — Full project report (PDF)

## Team
Helwan National University — Robotics & Mechatronics, April 2025
Supervised by: Dr. Abdalla Mohamed & Eng. Ahmed Abdelaal
Students: Mohamed Magdy, Omar Abdelsalam, Mohamed Yasser, 
John Botros, Amr Sherif, Mark Emad
