# Gasifier Curriculum

**THRONE-GEMINI: Dual-Phase Biomass Reactor Control System**

Part of the NODE-ZERO microgrid project. This subsystem connects to the [inverter-curriculum](https://github.com/PawelSroczynski/inverter-curriculum) for complete off-grid power generation.

---

## Overview

THRONE-GEMINI is an autonomous Waste-to-Energy system that performs two-stage thermochemical conversion in a single reactor vessel:

```
┌─────────────────────────────────────────────────────────────────┐
│                                                                 │
│   PHASE 1: PYROLYSIS (TLUD)          PHASE 2: GASIFICATION     │
│   ─────────────────────────          ──────────────────────     │
│                                                                 │
│   Input:  Biomass/Waste              Input:  Biochar (from P1) │
│   Output: Heat (CWU) + Biochar       Output: Syngas (CO + H₂)  │
│   Duration: 2-4 hours                Duration: 1-2 hours        │
│                                                                 │
│   Uses: Domestic hot water           Uses: Engine fuel for     │
│         heating                            electricity gen     │
│                                                                 │
└─────────────────────────────────────────────────────────────────┘
```

## Architecture

- **Topology:** Stationary docking head + mobile reactor vessels on turntable ("Revolver")
- **Controller:** SmartBOB (ESP32-based PLC) via ESPHome
- **Integration:** Home Assistant for monitoring and control
- **Connection:** Syngas output feeds to inverter system's generator

## System Integration

```
┌──────────────────┐      ┌──────────────────┐      ┌──────────────┐
│                  │      │                  │      │              │
│  GASIFIER        │─────►│  ENGINE          │─────►│  INVERTER    │
│  (this repo)     │syngas│  (generator)     │ AC   │  (DC-coupled)│
│                  │      │                  │      │              │
└──────────────────┘      └──────────────────┘      └──────────────┘
         │                                                  │
         │              ┌──────────────────┐               │
         └─────────────►│  SmartBOB        │◄──────────────┘
              control   │  (ESP32 PLC)     │    control
                        │  Home Assistant  │
                        └──────────────────┘
```

## Documentation

| File | Description |
|------|-------------|
| `THRONE_GEMINI_SPEC_v2.md` | Complete engineering specification |

### Specification Contents

- Physical architecture diagram
- 4-state finite state machine
- I/O mapping for ESP32/SmartBOB
- Safety interlocks and emergency procedures
- Process chemistry reference
- PID control parameters

## State Machine

```
STATE 0: IDLE ──────► STATE 1: PYROLYSIS ──────► STATE 2: TRANSITION
    ▲                     (Heat Mode)                    │
    │                                                    │
    │                                                    ▼
    └──────────────────────────────────────── STATE 3: GASIFICATION
                                                  (Power Mode)
```

## Status

- [x] Physics analysis and critical review
- [x] State machine design (v2)
- [x] Safety interlocks defined
- [ ] ESPHome YAML configuration
- [ ] Home Assistant dashboard
- [ ] Test bench simulation
- [ ] Hardware build

## Related Projects

- [inverter-curriculum](https://github.com/PawelSroczynski/inverter-curriculum) - DIY inverter and microgrid education
- NODE-ZERO - Complete off-grid power system

## License

MIT
