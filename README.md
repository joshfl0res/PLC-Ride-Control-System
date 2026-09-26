# PLC Ride Control System

A PLC-based amusement ride control simulation developed in CODESYS using IEC 61131-3 Ladder Logic.

The project is being developed incrementally to explore industrial control concepts used in automated and ride-control systems, including safety permissives, interlocks, sequential control, timers, sensor feedback, vehicle state tracking, and PLC scan behavior.

## Current Features
- Ride-ready logic using multiple operating and safety permissives
- Gate and restraint interlocks
- E-stop and stop-button permissives
- Vehicle-in-station detection
- Operator dispatch control
- Latched dispatch sequence
- 3-second pre-dispatch warning using a TON timer
- Warning horn and drive command sequencing
- Pre-dispatch safety monitoring that cancels dispatch if a required permissive is lost
- Vehicle departure detection using station sensor feedback
- Latched vehicle departure state
- Course entry and exit sensor simulation
- Latched course-entry state tracking
- Course entry validation requiring a valid drive command
- Course completion detection and memory
- PLC network execution-order handling for course completion logic
- Failure testing for loss of safety permissives during dispatch

## Current Control Sequence
1. Vehicle is detected in the station.
2. Required safety conditions are verified.
3. Operator initiates dispatch.
4. Dispatch command is latched while safety permissives remain valid.
5. A 3-second warning sequence activates.
6. Drive command is enabled after the warning timer completes.
7. Loss of the station sensor after a valid drive command records that the vehicle has departed.
8. Course entry sensor detects the vehicle entering the course.
9. The PLC retains the course-entry state after the entry sensor clears.
10. Course exit detection records that the vehicle completed the course.
11. The course-entry state clears while the completed state remains latched until reset.

## Tools & Technologies
- CODESYS V3.5
- IEC 61131-3 Ladder Logic
- PLC simulation
- TON timers
- Boolean logic
- Interlocks and permissives
- Latching / seal-in logic
- Sequential control
- Sensor-based state tracking
- PLC scan-cycle and execution-order troubleshooting

## Project Status
**In Development**

The current system supports a tested station dispatch sequence and sensor-based vehicle tracking from station departure through course completion.

Current development includes:
- Station safety and ride-ready permissives
- Operator dispatch and dispatch latching
- Timed pre-dispatch warning
- Drive command sequencing
- Vehicle departure tracking
- Course entry tracking
- Course completion tracking
- Safety-interlock failure testing

Future development will focus on modular PLC program organization, automatic ride sequencing, additional vehicle states, fault handling, operator monitoring, and eventual state-machine-based control.

## Disclaimer
This project is an educational simulation intended for learning PLC and industrial control concepts. It is not intended for use as a safety-rated control system or on an actual amusement ride.