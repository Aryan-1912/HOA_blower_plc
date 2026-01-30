# HOA Blower Control System

A Hand-Off-Auto (HOA) blower control system developed using RSLogix Micro Starter Lite for Allen-Bradley MicroLogix PLCs.

## Overview

This project implements a standard industrial HOA selector switch control scheme for a blower motor. HOA controls are widely used in industrial environments including HVAC systems, pumps, fans, and conveyor motors.

## Operating Modes

| Mode | Function |
|------|----------|
| **Hand** | Manual override - blower runs continuously regardless of process signals |
| **Off** | Safe shutdown - blower is de-energized |
| **Auto** | Automatic control - blower operation driven by process conditions |

## Hardware Requirements

- Allen-Bradley MicroLogix PLC (or compatible)
- 3-position HOA selector switch
- Blower motor with appropriate starter/contactor
- 24V DC power supply for I/O

## Software Requirements

- RSLogix Micro Starter Lite (or RSLogix 500)

## I/O Configuration

### Inputs
| Address | Description |
|---------|-------------|
| I:0/0 | Hand position |
| I:0/1 | Auto position |
| I:0/2 | Process signal (for Auto mode) |

### Outputs
| Address | Description |
|---------|-------------|
| O:0/0 | Blower motor output |

## Ladder Logic

The control logic follows standard HOA implementation:
- Hand mode energizes the output directly
- Off mode (neither Hand nor Auto selected) keeps output de-energized
- Auto mode enables output based on process signal input

## File Structure

```
├── HOA_blower_prj.RSS    # RSLogix project file
└── README.md
```

## How to Use

1. Open `HOA_blower_prj.RSS` in RSLogix Micro Starter Lite
2. Configure communication settings for your PLC
3. Download program to PLC
4. Test each mode of operation

## Applications

- Industrial blower/fan control
- Pump station controls
- HVAC systems
- Conveyor motor control
- Any application requiring manual override capability

## Author

Aryan  
Computer Engineering Technology - Sheridan College

## License

This project is available for educational purposes.
