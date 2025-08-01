---
title: "UNIT Relay Module"
version: "1.0"
modified: "2025-05-02"
output: "relay_module"
subtitle: "This dual-channel relay module safely interfaces microcontrollers with higher-voltage or high-current loads by separating control from power."
copy_files:
  - source: "../../hardware/unit_sch_v_0_0_1ue0082_modulo_rele_g6k_.pdf"
    destination: "../../docs/"
    link_name: "unit_sch_v_0_0_1ue0082_modulo_rele_g6k_.pdf"
---

<!--
# README_TEMPLATE.md
Este archivo sirve como entrada para generar un PDF técnico estilo datasheet.
Edita las secciones respetando el orden, sin eliminar los encabezados.
-->
 <!-- logo -->

# UNIT Relay Module

![Relay Module](../../hardware/resources/img/relay_module.png)

## Introduction

This dual-channel relay module isolates high-power operations from sensitive MCU logic. It supplies a dedicated 5V rail (JDVCC) for relay coils while using the VCC pin to match the MCU’s operating voltage (3.3V or 5V). A digital high on the IN pin triggers an optocoupler that switches the NO, NC, and COM contacts. LED indicators provide immediate feedback on power and control status.


## Functional Description

- The module includes two independent electromechanical relays, each controlled through optocouplers for complete electrical isolation between control logic and relay coil voltage.
- A dedicated power rail (JDVCC) provides 5V specifically to energize the relay coils, while a separate VCC pin supplies 3.3V or 5V to the optocoupler input stage.
- Each relay channel is triggered via an active-high digital input signal (IN1, IN2) from the microcontroller.
- The relay outputs provide access to a set of contacts: Normally Open (NO), Normally Closed (NC), and Common (COM).
- When triggered, the relay switches the contacts, allowing control of external AC/DC loads while protecting the MCU from high-voltage transients.
- LED indicators (LED PWR and LED IN) provide immediate visual feedback of power and activation status.

## Electrical Characteristics & Signal Overview

- Operating voltage (logic side): 3.0 V – 5.5 V (via VCC pin)
- Relay coil voltage: 5 V nominal (via JDVCC)
- Trigger current per channel: 2–15 mA depending on input logic level
- Contact rating: Up to 0.3 A - 125 VAC or 1 A - 30 VDC
- Optocoupler logic threshold: Compatible with 3.3 V and 5 V logic

## Applications

- Home Automation
- IoT Projects
- Automated Irrigation
- Testing & Laboratory
- Robotics & Mechatronics
- Smart Agriculture
- Security & Alarm Systems
- Education & Demos



## Features

- Dual-channel electromechanical relay outputs
- Optical isolation between control and power stages
- Dedicated 5V relay coil supply (JDVCC)
- 3.3V or 5V logic compatibility (VCC)
- LED indicators for control signal and power presence
- Breakout access to NO, NC, and COM terminals per channel


## Pin & Connector Layout

| Signal  | Description                                                       |
|---------|-------------------------------------------------------------------|
| JDVCC   | +5V supply to energize relay coils                                |
| VCC     | MCU logic voltage (3.3V or 5V) for the optocoupler/driver circuit     |
| IN      | MCU input to activate relay channel 1                             |
| NO1     | Relay 1 normally open contact                                       |
| COM1    | Relay 1 common terminal                                             |
| NC1     | Relay 1 normally closed contact                                     |
| NO2     | Relay 2 normally open contact                                       |
| COM2    | Relay 2 common terminal                                             |
| NC2     | Relay 2 normally closed contact                                     |
| LED PWR | Indicator LED for power (active when JDVCC is present)              |
| LED IN  | Indicator LED showing active input from the MCU                     |



## Settings

### Interface Overview

### Interface Overview

| Interface  | Signals / Pins                  | Typical Use                                     |
|------------|----------------------------------|-------------------------------------------------|
| Power      | JDVCC, VCC, GND                  | Power relay coils and optocoupler driver circuit|
| Control    | IN1, IN2                         | Trigger signals from MCU                        |
| Output     | NO1, COM1, NC1 / NO2, COM2, NC2  | Switching terminals for AC/DC load             |
| Indicators | LED (PWR), LED (IN)                  | Visual status of power and input activation     |




### Supports

| Symbol | I/O   | Description                                 |
|--------|-------|---------------------------------------------|
| JDVCC  | Input | 5V supply input for relay coil energization |
| VCC    | Input | Logic voltage input (3.3V or 5V)            |
| GND    | Input | Shared ground for logic and relay power     |
| IN1    | Input | Control signal to activate relay 1          |
| IN2    | Input | Control signal to activate relay 2          |
| NOx    | Output| Normally open contact (connected when active) |
| NCx    | Output| Normally closed contact (disconnected when active) |
| COMx   | Output| Common terminal for relay switching          |


## Block Diagram

![Function Diagram](../../hardware/resources/unit_pinout_v_0_0_1_ue0082_relay_en.png)

## Dimensions

![Dimensions](../../hardware/resources/unit_dimension_v_0_0_1ue0082_modulo_rele_g6k_.png)

## Usage

Works with:

- Arduino AVR
- Raspberry Pi RP2040
- STM32
- PY32


## Downloads

- [Schematic PDF](https://github.com/UNIT-Electronics-MX/unit_relay_module_g6k_2g_y_tr_dc5/blob/main/hardware/unit_sch_v_0_0_1ue0082_modulo_rele_g6k_.pdf)

- [Board Dimensions](https://github.com/UNIT-Electronics-MX/unit_relay_module_g6k_2g_y_tr_dc5/tree/main/hardware#dimensions)


## Purchase

- [Buy from UNIT Electronics](https://www.uelectronics.com)
