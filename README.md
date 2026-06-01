# BEAM by Fyrefly - Hardware Development Log

This repository tracks the physical architecture, enclosure design iterations, and development history for BEAM: a desk-native parametric speaker system creating invisible acoustic infrastructure for B2B knowledge-work environments.

## Overview
Because BEAM utilizes proprietary phased-array ultrasonic beamforming, core firmware logic and raw electrical manufacturing files (Gerbers) are kept internal to protect intellectual property. This public repository functions as a physical versioning log and a host for non-proprietary structural enclosure assets and historical layout screenshots.

---

## Iteration History & Learning Log

Our engineering path has been defined by rapid iteration, testing, and pivoting based on hardware constraints and market research.

### Phase 0.1 - Initial Home Theater Concept (Archived)
* **Architecture:** First iteration main board and array featuring 1 HDMI port and no Bluetooth connectivity.
* **Target:** Initially designed for home theater settings.
* **Learning:** Market research and user discovery revealed a much more urgent need in the workspace. The home theater market was crowded, fundamentally different and in my opinion pretty boring when viewed from the acoustic focus problem knowledge workers face. Visuals of this early Gerber routing are archived in `/pcb-history/`.

### Phase 0.2 - HDMI Passthrough Iteration (Archived)
* **Architecture:** Second iteration main board adding a Bluetooth chip and 2 HDMI ports for passthrough capabilities.
* **Learning:** While functionally richer, I realized that HDMI passthrough introduced massive, unnecessary inefficiencies at this development stage. It complicated the board without serving our core goal: projecting an isolated acoustic zone. We scrapped this approach entirely to simplify the architecture.

### Phase 0.3 - Current V0 Prototype Array (Active Validation)
* **Pivot:** Fully refocused from consumer entertainment to B2B workspace infrastructure
* **Form Factor:** Stripped out the HDMI bloat. Now utilizing a compact 100x75mm array structure hosting a honeycomb pattern of 18–20 transducers.
* **Design Optimization:** Modified the layout to incorporate female header pins, making the transducers entirely hot-swappable. This allows us to rapidly replace components and iterate on physical layout configurations without printing entirely new boards.
* **Firmware Integration:** Microcontroller logic (ESP32/Arduino) is actively being structured alongside external engineering support to handle automated presence detection.

### What's next 
* **Refine firmware** to include improved AM modulation (might move into other forms if it improves the bass frequency)
* **Build out feature set** Intend to implement auracast function for hearing aid compatibility alongside presence detection for seamless use.

---

## Directory Structure

* 📁 `/enclosure/` — Contains `.obj` files demonstrating the physical form factor and how the device positions itself under standard workspace monitors.
* 📁 `/pcb-history/` — Contains our visual hardware changelog:
  * `/phase-0.1-hometheater/` — Screenshots of the initial 1-HDMI / no-Bluetooth board routing.
  * `/phase-0.2-passthrough/` — Screenshots of the 2-HDMI / Bluetooth passthrough board routing.
