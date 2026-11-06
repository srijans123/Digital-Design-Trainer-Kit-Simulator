# Digital Design Lab Trainer Kit Simulator (Physitech PHY-1002)

A browser-based, pin-accurate simulation of the **Physitech PHY-1002 Universal Digital Lab Trainer Kit**, designed for the **BITS Pilani, Hyderabad Campus** Digital Design course (`CS F215 / ECE F215 / EEE F215 / INSTR F215`) based on the official [BITS Pilani Digital Design F215 Course Handout](https://www.scribd.com/document/1054436513/Cs-f215-Digital-Design-Handout).

---

## Overview

In physical electronics labs, wiring 74-series TTL logic chips on breadboards often leads to loose patch cords, burnt IC pins, and tedious troubleshooting. This simulator allows students and engineers to wire and verify digital circuits directly in the browser with realistic hardware behavior.

- **Zero-dependency, native architecture**: Runs completely in pure HTML5, CSS3, Vanilla JS, and WebGL with zero bundlers, npm dependencies, or remote compilation required.
- **Physical kit accuracy**: Faithful reproduction of the Physitech PHY-1002 dual-board layout, breadboard turret sockets, toggle input switches, LED monitors, and 7-segment decoders.

---

## Key Features

### 1. Patch-Cord Wiring & Turret Pin Graph
- Click-to-connect jumper cord engine with automatic pin-to-pin signal propagation.
- Multi-color wire selection and real-time wire removal/clearing.
- Live **Wire Connection Diagram** detailing every active jumper, connected pins, and signal states (`HIGH` / `LOW`).

### 2. 74-Series TTL Logic Library
Accurate behavioral and pinout logic models for standard 14-pin and 16-pin DIP ICs:
- **Basic & Universal Gates**: 7400 (NAND), 7402 (NOR), 7404 (NOT), 7408 (AND), 7432 (OR), 7486 (XOR)
- **Arithmetic & Comparison**: 7483 (4-bit Binary Full Adder), 7485 (4-bit Magnitude Comparator), 74181 (4-bit ALU)
- **Multiplexers & Decoders**: 74138 (3-to-8 Decoder), 74151 (8-to-1 MUX), 74153 (Dual 4-to-1 MUX), 7447 (BCD to 7-Segment Decoder)
- **Flip-Flops & Registers**: 7474 (Dual D Flip-Flop), 7476 (Dual J-K Flip-Flop), 74194 (4-bit Bidirectional Universal Shift Register)
- **Counters**: 7490 (Decade Counter), 7493 (4-bit Binary Counter), 74163 (Synchronous 4-bit Binary Counter)

### 3. Preloaded F215 Lab Experiments
Instant preset loading with complete wiring maps for all standard lab experiments:
1. Basic & Universal Logic Gates Verification (7400, 7402, 7404, 7408, 7432, 7486)
2. Half Adder & Full Adder Realization using Basic Gates
3. 2's Complement 4-Bit Adder/Subtractor with Overflow Detection (7483)
4. 4:1 Multiplexer Function Implementation & Expansion (74153)
5. BCD to 7-Segment Display Decoding (7447)
6. J-K Flip-Flop Truth Table & Toggle Mode Verification (7476)
7. 4-Bit Asynchronous Ripple Counter (7493)
8. 4-Bit Magnitude Comparator (7485)

### 4. Interactive Instrumentation & Analysis
- **Office-Style Ribbon Tabs**: Structured navigation (`[Wiring & Power]`, `[Lab Experiments]`, `[Analysis & Truth Table]`, `[IC Library & Photos]`, `[Print & Export]`).
- **Automated Truth Table Generator**: Automatically cycles through all input switch combinations ($2^N$), evaluates the logic graph, and highlights output states.
- **Timing Scope Canvas**: Live multi-channel digital waveform visualization.
- **Print & Screenshot Mode**: One-click printable lab record generation with circuit telemetry.

---

## Getting Started

Because the simulator uses pure native web technologies, no build tools or package managers are required.

### Quick Start
1. Clone the repository:
   ```bash
   git clone https://github.com/<your-username>/dd-simulator.git
   cd dd-simulator
   ```
2. Open `index.html` directly in any modern web browser (Chrome, Edge, Firefox, Safari).

Alternatively, serve locally with any static HTTP server:
```bash
# Using Python
python -m http.server 8000

# Using Node.js
npx serve .
```

---

## File Structure

```
├── Assets/                                 # Video loops and macro kit photography
│   ├── demo-waveform-7seg-loop.mp4
│   ├── demo-wiring-loop.mp4
│   ├── hero-liquid-orb-loop.mp4
│   ├── hero-liquid-core.jpg
│   ├── logic-waveform-3d.jpg
│   └── trainer-kit-pcb-macro.jpg
├── index.html                              # Interactive landing page with WebGL 3D wave shader
├── physitech_phy_1002_simulator_fixed.html # Full Physitech PHY-1002 digital design trainer kit simulator
└── README.md
```

---

## License

MIT License. Designed for academic and educational use for the BITS Pilani Digital Design curriculum.

