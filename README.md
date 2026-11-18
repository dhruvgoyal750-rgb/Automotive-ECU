# Automotive ECU Design

A conceptual automotive Electronic Control Unit (ECU) design created in
**EasyEDA Standard** as an educational electronics and PCB-design
portfolio project.

> **Disclaimer:** This is a learning/demo project only. It has not been
> validated for use in a real vehicle. Do not connect it to a vehicle or
> rely on it for safety-critical functions.

## Project Overview

This project demonstrates the design of a microcontroller-based ECU
concept with a CAN communication interface and regulated power rails.

### Main features

-   STM32F103C8T6 microcontroller
-   SN65HVD230 CAN transceiver
-   CANH and CANL interface
-   Conceptual 12V input and 5V / 3.3V regulation stages
-   Reset, BOOT0, crystal-clock and SWD programming/debug connections
-   Schematic capture and PCB layout in EasyEDA Standard

## System Architecture

``` text
12V DC Input
    |
    v
LM2596S-5.0 (5V regulator)
    |
    v
AMS1117-3.3 (3.3V regulator)
    |
    +------> STM32F103C8T6
    |
    +------> SN65HVD230 CAN Transceiver
                    |
                    v
                 CANH / CANL
```

## Components

  Reference / Part          Description
  ------------------------- ------------------------------------------
  STM32F103C8T6             Main microcontroller
  SN65HVD230                CAN bus transceiver
  LM2596S-5.0               5V buck regulator
  AMS1117-3.3               3.3V regulator
  8 MHz crystal             MCU clock source
  TVS / protection parts    Conceptual input and CAN protection
  Connectors and passives   Power, CAN, SWD and supporting circuitry

Component values, footprints, pin assignments and protection details
should be checked against the final EasyEDA design and the relevant
manufacturer datasheets.

## Repository Structure

``` text
Automotive-ECU-Design/
├── README.md
├── BOM.csv
├── LICENSE
├── docs/
│   ├── design-notes.md
│   └── pin-mapping.md
├── hardware/
│   └── README.md
└── images/
    └── README.md
```

Add your exported EasyEDA schematic, PCB screenshots, project source and
fabrication outputs to suitable folders when available. Do not upload
generated Gerber files as proof of electrical or automotive validation.

## Tools Used

-   EasyEDA Standard --- schematic capture and PCB layout
-   GitHub --- project documentation and version control

## Design Workflow

1.  Create the circuit schematic in EasyEDA.
2.  Assign footprints to components.
3.  Convert the schematic into a PCB layout.
4.  Place components and route tracks.
5.  Review design-rule-check results.
6.  Export project files and document the design.

A successful PCB design-rule check only checks the configured PCB layout
rules; it does not prove that the circuit is electrically correct or
safe for automotive use.

## Learning Outcomes

-   Understanding a basic MCU-based ECU architecture
-   Learning CAN transceiver interfacing
-   Practising regulated power-rail planning
-   Schematic-to-PCB workflow
-   PCB placement, routing and design documentation
-   Using GitHub to present an engineering project

## Author

**Dhruv Goyal**\
B.Tech --- Electronics and Communication Engineering

## License

This project is shared under the MIT License. See [LICENSE](LICENSE).
