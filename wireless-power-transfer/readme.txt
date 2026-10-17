# Wireless Power Transfer: Short-Range Inductive Mobile Charging System

A low-power wireless power transfer prototype developed as an open-ended project for **ECE 2200: Electronic Circuits Design Laboratory** at **Khulna University of Engineering & Technology (KUET)**.

The project demonstrates how electrical energy can be transferred over a short air gap using electromagnetic induction, followed by rectification, filtering, and voltage regulation to obtain a nominal 5 V DC output.

## Project Information

| Item | Details |
|---|---|
| Project Title | Wireless Power Transfer: Short-Range Inductive Mobile Charging System |
| Course | ECE 2200: Electronic Circuits Design Laboratory |
| Department | Electronics and Communication Engineering |
| Institution | Khulna University of Engineering & Technology (KUET) |
| Project Type | Open-Ended Project |
| Estimated Component Cost | BDT 840 |

## Team Members

- **Md Baized Al Nur** (2309033)
- **Abdullah Al Araf Emon** (2309048)
- **Yeasir Arafat Siju** (2309058)

### Project Supervisors

- Asst. Prof. Shafrin Sultana
- Asst. Prof. Nawaz Talukder Sanglap

## Project Overview

Wireless power transfer allows electrical energy to move from a transmitter to a receiver without a direct electrical connection. This project uses two coils and a changing magnetic field to demonstrate the principle of inductive power transfer.

The transmitter uses a KA3525A PWM controller and two IRFZ44N MOSFETs to drive a center-tapped transmitter coil. The changing magnetic field induces an AC voltage in the receiver coil. A Schottky diode bridge, filter capacitors, and a 7805 voltage regulator are used to convert the received energy into a nominal 5 V DC output.

The prototype demonstrated wireless power transfer over an approximate distance of **2.5 cm**, under the tested conditions.

## Main Objectives

- Design and build a short-range wireless power transfer system.
- Study electromagnetic induction and LC resonance.
- Calculate the required circuit parameters and component values.
- Implement the transmitter and receiver circuits.
- Measure voltage and current and investigate power-transfer efficiency.
- Study the effects of coil spacing, alignment, orientation, operating frequency, and load.
- Test the circuit on a breadboard and implement the design on a PCB.

## Block Diagram

```text
             TRANSMITTER
    +----------------------------+
    |                            |
    |  12 V DC Power Supply      |
    |           |                |
    |  Input Protection          |
    |           |                |
    |  KA3525A PWM Controller    |
    |           |                |
    |  2 x IRFZ44N MOSFETs        |
    |           |                |
    |  Transmitter Coil          |
    +-------------+--------------+
                  |
          Alternating Magnetic
                Field
                  |
             Air Gap
                  |
    +-------------v--------------+
    |       RECEIVER              |
    |                             |
    |  Receiver Coil              |
    |           |                 |
    |  Compensation Capacitor     |
    |           |                 |
    |  Schottky Bridge Rectifier  |
    |           |                 |
    |  Filter Capacitors          |
    |           |                 |
    |  7805 Voltage Regulator     |
    |           |                 |
    |  Nominal 5 V DC Output      |
    +-----------------------------+
```

## Working Principle

### 1. PWM Generation

The KA3525A generates alternating control signals for the transmitter switching stage. Its timing components determine the switching frequency.

### 2. MOSFET Switching

Two IRFZ44N MOSFETs switch current through the two halves of the center-tapped transmitter coil. This produces a changing magnetic field around the coil.

### 3. Electromagnetic Induction

The changing magnetic field links with the receiver coil and induces an AC voltage according to Faraday's law:

\[
\varepsilon=-N\frac{d\Phi}{dt}
\]

Where:

- \(\varepsilon\) = induced electromotive force
- \(N\) = number of turns in the receiver coil
- \(\Phi\) = magnetic flux through the coil

### 4. Resonance

A compensation capacitor is used with the coil to form an LC resonant circuit. The theoretical resonant frequency is:

\[
f_r=\frac{1}{2\pi\sqrt{LC}}
\]

The actual operating and resonant frequencies should be verified experimentally because component tolerances, coil losses, and coupling affect the circuit.

### 5. Rectification and Filtering

Four 1N5819 Schottky diodes form a full-wave bridge rectifier. Filter capacitors reduce the ripple in the rectified voltage.

### 6. Voltage Regulation

A 7805 linear regulator is used to provide a nominal 5 V DC output when its input voltage and thermal conditions are suitable.

## Main Components

| Component | Quantity | Purpose |
|---|---:|---|
| KA3525A PWM controller | 1 | Switching signal generation |
| IRFZ44N MOSFET | 2 | Transmitter switching |
| Transmitter coil | 1 | Generates the alternating magnetic field |
| Receiver coil | 1 | Receives energy through magnetic coupling |
| 1N5819 Schottky diode | 4 | AC-to-DC bridge rectification |
| 7805 voltage regulator | 1 | 5 V output regulation |
| Polypropylene film capacitors | As required | Resonance and switching circuits |
| Electrolytic capacitors | As required | Filtering |
| Ceramic capacitors | As required | Bypass and noise reduction |
| Resistors and Zener diodes | As required | Timing, gate control, and protection |
| Fuse | 1 | Input protection |
| USB Type-C output interface | 1 | Output connection |

The estimated total component cost was **BDT 840**, based on the project's initial budget.

## Coil Specifications

| Parameter | Transmitter | Receiver |
|---|---|---|
| Coil diameter | Approximately 5 cm | Approximately 5 cm |
| Number of turns | 6-0-6 turns | 18–20 turns |
| Measured inductance | Approximately 14.4 µH (full winding) | Approximately 40.5 µH |
| Compensation capacitance | 300 nF | 100 nF |

The reported theoretical resonant frequencies are approximately:

- **Transmitter:** 76.5 kHz
- **Receiver:** 79.1 kHz

These are calculated values for the specified inductance and capacitance, not guaranteed measured operating frequencies.

## Experimental Results

The prototype was assembled, tested, and transferred from breadboard implementation to a PCB.

| Parameter | Reported result |
|---|---|
| Wireless transfer distance | Approximately 2.5 cm |
| Receiver rectification | Four-diode Schottky bridge |
| Output regulation | 7805 linear regulator |
| Intended output | Nominal 5 V DC |
| Estimated component cost | BDT 840 |

The experiment demonstrated short-range wireless energy transfer. The received power depends on coil separation, alignment, orientation, switching frequency, and load.

**Note:** Detailed measurements of output current, output power, efficiency, output stability, and component temperature are still needed for a complete performance evaluation.

## Tools and Testing Equipment

- Proteus for circuit simulation
- Digital multimeter
- Oscilloscope
- Breadboard and PCB
- Soldering tools
- Load resistors

## Challenges and Limitations

- Magnetic coupling decreases as the distance between the coils increases.
- Coil misalignment reduces the received voltage and power.
- Switching losses and coil resistance reduce efficiency.
- The 7805 regulator can produce significant heat under unsuitable input-voltage and load conditions.
- The prototype has not been certified or tested as a commercial mobile phone charger.

The USB Type-C output interface provides a physical output connection, but a regulated 5 V supply alone does not guarantee full USB-C charging compatibility.

## Future Improvements

- Measure input power, output power, and transfer efficiency.
- Investigate the effects of different coil gaps and alignments.
- Improve coil coupling and output stability.
- Reduce switching and rectification losses.
- Evaluate a suitable switching regulator to reduce regulator heating.
- Test the circuit under different loads and operating conditions.

## Repository Structure

```text
Wireless-Power-Transfer/
├── README.md
├── WPT_poster.pdf
├── project_Report.pdf
├── circuit/
│   └── Add circuit diagrams here
├── simulation/
│   └── Add Proteus simulation files here
└── images/
    └── Add prototype and PCB photos here
```

The folders shown above are suggested. Keep only the folders and files that are actually present in the repository.

## Learning Outcomes

This project provided practical experience with:

- Electromagnetic induction and mutual inductance
- LC resonance and coil parameter calculations
- PWM controllers and MOSFET switching
- High-frequency rectification and DC filtering
- Linear voltage regulation
- Circuit simulation, troubleshooting, and PCB implementation
- Technical documentation and teamwork

## Conclusion

This project demonstrated short-range wireless power transfer through electromagnetic induction. It combined PWM control, MOSFET switching, transmitter and receiver coils, rectification, filtering, and voltage regulation in a single educational prototype.

The project helped connect electronic circuit theory with practical design and testing. Further work is needed to quantify efficiency, improve output stability, and evaluate performance under different operating conditions.

---

**Academic Project:** ECE 2200, Electronic Circuits Design Laboratory  
**Institution:** Khulna University of Engineering & Technology (KUET)  
**Department:** Electronics and Communication Engineering

*Developed as an educational prototype. Not a certified commercial fast charger.*
