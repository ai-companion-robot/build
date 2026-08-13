# AI-Integrated Companion Robot

**Status:** Early Design & Research Phase  
**Team:** 1 industry mentor (System Architect, Google) + 3 mentees  
**Started:** July 2026

---

## Overview

A small autonomous companion robot that can navigate a room, avoid obstacles, detect edges and drops, and interact with users through voice and camera input – driven by an AI model that interprets sensor data and makes decisions in real time rather than executing fixed pre-programmed behaviors.

This project was initiated by our industry mentor and is being developed collaboratively as a structured learning and build experience. This repository is the central hub for all design documentation, research, BOMs, and CAD as the project develops.

---

## Project Goals

- Build a functional AI-integrated robot from the ground up – hardware and software
- Use an AI model as the decision-making "brain" rather than hardcoded logic
- Develop capabilities incrementally: mobility first, then obstacle/edge detection, then voice and camera interaction
- Gain experience across the full design cycle: concept, CAD, component selection, fabrication, and integration

---

## Current Status

The project is in the early design and research phase. Current work includes:

- Researching and selecting core hardware components (compute, sensing, actuation)
- Developing initial CAD models with block components and basic dimensioning
- Defining software and hardware requirements for target functionality
- Building out the BOM with cost and trade-off analysis across component options
- Evaluating compute architecture – split between a Raspberry Pi (AI/camera/voice) and ESP32 microcontroller (low-level driving and obstacle avoidance) to keep AI response latency from blocking real-time motion control

---

## System Architecture (Planned)

| Subsystem | Approach | Status |
|---|---|---|
| Compute – AI | Raspberry Pi | Researching |
| Compute – Motion | ESP32 microcontroller | Researching |
| Drive | 2-wheel drive + caster ball wheels | Researching |
| Obstacle avoidance | Onboard sensors + ESP32 | Researching |
| Edge / fall detection | Onboard sensor + ESP32 | Researching |
| Voice interaction | Microphone + Raspberry Pi | Researching |
| Vision | Camera + AI model | Researching |
| Power | TBD | Researching |

---

## Design Rationale

**Split compute architecture**  
Separating the AI processing (Raspberry Pi) from the real-time motion control (ESP32) means the robot doesn't have to wait for an AI inference cycle before responding to an obstacle. The ESP32 handles fast, reactive behaviors while the Raspberry Pi handles higher-level perception and decision-making.

**2-wheel drive + casters**  
Simpler to build and control at this scale than tank treads, and gives adequate maneuverability for indoor navigation. Easier to iterate on than a tracked system if the chassis needs changes.

---

## Repository Structure

```
/
├── bom/          # Bills of materials and component trade studies
├── cad/          # SolidWorks and other CAD files
├── docs/         # Design documents and meeting notes
├── research/     # Component datasheets, notes, and reference material
└── README.md
```

*Folders will be populated as the project progresses.*

---

## Next Steps

- [ ] Finalize core component selections (compute, sensors, drive motors)
- [ ] Complete initial BOM with cost estimates
- [ ] Develop CAD model beyond block layout to actual component geometry
- [ ] Define software architecture and identify libraries/frameworks
- [ ] Order initial components and begin bench testing
- [ ] Establish first functional milestone (basic mobility + obstacle stop)
