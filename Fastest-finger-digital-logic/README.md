# Fastest Finger Quiz System Using Digital Logic ICs

A fully hardware-based **Fastest Finger Quiz System** designed and implemented using standard digital logic ICs, without any microcontroller or software programming.

## Project Overview

This project is intended for quiz competitions where identifying the fastest participant is essential. The system detects the **first player** to press their button, locks all remaining inputs, displays the responding player number, and manages timeout automatically.

The system consists of two main sections:

- **Timing and Counting Unit**
- **Player Response Control Unit**

---

## Features

- 0–9 response timer using decade counter
- First player response detection
- Automatic input lockout after first valid response
- Player number display (1–4)
- Green LED for successful response
- Red LED for timeout indication
- Manual reset for next round
- Fully hardware-based implementation

---

## Components Used

- NE555 Timer
- 74LS90 Decade Counter
- 74LS48 BCD to 7-Segment Decoder
- 7476 JK Flip-Flop
- 7408 AND Gate
- 7432 OR Gate
- 7402 NOR Gate
- 7404 NOT Gate
- 7400 NAND Gate
- 7413 Quad NAND
- 7-Segment Displays
- Push Buttons
- LEDs
- Resistors
- Capacitors
- Breadboard

---

## Simulation

The complete system was first designed and tested using **Proteus Design Suite**.

---

## Project Structure

```bash
fastest-finger-system-digital-logic/
│
├── report/
├── proteus_simulation/
├── circuit_diagrams/
├── hardware_photos/
├── datasheets/
└── README.md
```

---

## Authors

- **Yeasir Arafat Siju**
- **Sabikunnahar Sabira**

Department of Electronics and Communication Engineering  
Khulna University of Engineering & Technology (KUET)

---

## License

This project is shared for educational purposes.
