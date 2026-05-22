# Op-Amp Based Function Generator

## Project Overview
This project presents the **design and implementation of an analog function generator** using **LM741 operational amplifiers**. The system is capable of generating:

- Square Wave
- Triangle Wave
- Sine Wave

The project was developed as part of the course:

- **Course No:** ECE 2102  
- **Course Title:** Analog Electronics-II Laboratory  
- **Department:** Electronics and Communication Engineering  
- **Institution:** :Khulna University of Engineering & Technology (KUET)

---

## Team Members

| Name | Roll |
|------|------|
| Khondoker Khalid Hasan Kaif | 2309056 |
| Tasfia Tohura | 2309057 |
| Yeasir Arafat Siju | 2309058 |
| Sabikunnahar Sabira | 2309059 |
| Shithi Hazra | 2309060 |

---

# Abstract

A function generator is an important electronic instrument used for generating standard waveforms for testing and educational purposes. Commercial function generators are often expensive, so this project focuses on developing a **low-cost analog function generator** using simple Op-Amp circuits.

The system uses:

- Schmitt Trigger Oscillator → Square Wave
- Integrator Circuit → Triangle Wave
- Wave Shaping Circuit → Sine Wave

The entire design was simulated in **Proteus Design Suite** using LM741 Op-Amps.

---

# Objectives

## General Objectives
- Design a multi-wave analog function generator
- Generate square, triangle, and sine waves
- Use low-cost electronic components

## Specific Objectives
- Design a Schmitt trigger oscillator
- Generate triangle wave using an integrator
- Convert triangle wave into sine wave
- Analyze waveform characteristics
- Study LM741 limitations
- Improve practical analog electronics knowledge

---

# System Design

## Functional Block Diagram

```text
Schmitt Trigger → Integrator → Sine Shaping Circuit
     ↓                ↓                ↓
 Square Wave     Triangle Wave     Sine Wave
