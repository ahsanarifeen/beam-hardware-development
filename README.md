# BEAM by Fyrefly - Hardware Development Log

This repository tracks the physical architecture, enclosure design iterations, and hardware validation history for BEAM: a desk-native parametric speaker system using phased-array ultrasonic beamforming to create individualized, headphone-free acoustic spaces.

## Overview
Because BEAM is a highly specialized hardware product utilizing directional audio arrays, this repository functions primarily as a physical versioning log and a repository for non-proprietary structural files (such as outer enclosure dimensions). Core firmware architecture and raw electrical manufacturing files (Gerbers) are kept private to protect internal intellectual property.

_________________________________

## Hardware Iteration History

### Phase 0.1 - Initial Transducer Array Concept (Archived)
* **Objective:** Test early component density and geometric spacing for the ultrasonic transducers.
* **Architecture:** Initial layout configurations focused on general transducer footprints.
* **Outcome:** Acoustic testing revealed potential node interference and routing inefficiencies. This geometry was deprecated to rebuild the trace architecture from first principles. Visual layout configurations are archived internally.

### Phase 0.2 - Current Modular Prototype Array (In Progress)
* **Objective:** Create a highly flexible, testable validation board to refine beamforming accuracy.
* **Form Factor:** Focused on a compact 100x75mm array structure hosting a honeycomb pattern of 18–20 transducers.
* **Design Optimization:** Modified the layout design to incorporate female header pins. This makes the transducers entirely hot-swappable, allowing us to rapidly replace components and iterate on physical layout configurations without printing entirely new boards.
* **Firmware Integration:** Microcontroller logic (ESP32/Arduino) is being structured alongside external engineering support to handle automated presence detection and ambient soundscape delivery loops.

_________________________________

## Repository Structure Overview

* `/hardware/enclosure/`: Contains external physical design files and outer dimension models (`.obj` / `.stl`) mapping how the device natively positions itself under standard workspace monitors.
* `/hardware/documentation/`: Contains non-proprietary block diagrams outlining basic power routing and systems logic flows.
