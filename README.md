# PLC Ride Control System

A PLC-based amusement ride control simulation developed in CODESYS using IEC 61131-3 Ladder Logic.

The project is being developed incrementally to explore industrial control concepts used in automated and ride-control systems, including safety permissives, interlocks, sequential control, timers, sensor feedback, and vehicle state tracking.

## Current Features

- Ride-ready logic using multiple operating and safety permissives
- Gate and restraint interlocks
- E-stop and stop-button permissives
- Vehicle-in-station detection
- Operator dispatch control
- Latched dispatch sequence
- 3-second pre-dispatch warning using a TON timer
- Warning horn and drive command sequencing
- Course entry and exit sensor simulation
- Latched vehicle course-state tracking
- Course entry validation requiring a valid drive command
- Failure testing for loss of safety permissives during dispatch

## Current Control Sequence

1. Vehicle is detected in the station.
2. Required safety conditions are verified.
3. Operator initiates dispatch.
4. Dispatch command is latched while safety permissives remain valid.
5. A 3-second warning sequence activates.
6. Drive command is enabled after the warning timer completes.
7. Course entry sensor detects the departing vehicle.
8. The PLC stores the vehicle's course state after the entry sensor clears.
9. Course exit detection clears the stored course state.

## Tools & Technologies

- CODESYS V3.5
- IEC 61131-3 Ladder Logic
- PLC simulation
- TON timers
- Boolean logic
- Interlocks and permissives
- Sequential control

## Project Status

**In Development**

Current development is focused on expanding vehicle movement and sensor-based sequence control. Future iterations will introduce additional ride states, fault handling, automatic sequencing, and operator monitoring.

## Disclaimer

This project is an educational simulation intended for learning PLC and industrial control concepts. It is not intended for use as a safety-rated control system or on an actual amusement ride.
