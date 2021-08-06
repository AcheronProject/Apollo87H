# Acheron Apollo87H

## Introduction

Apollo is a tenkeyless (TKL) keyboard Printed Circuit Board (PCB) which main feature is the per-key RGB lighting. This particular variant, 87H, features an 87-key layout with Kailh hotswap sockets. Additionally, 87H supports a "default" TKL layout, with a 6.25 units spacebar, no split backspace or right shift, and ANSI-only.

Both Apollo and Athena line of PCBs were designed to be "universal" TKL PCBs, that is, designed to fit a wide variety of custom mechanical keyboards. The compatibility list is being built as more people check and test. See the **Keyboard compatibility** section of this README for the available list.

## Technical information (latest release)

- Layout size: tenkeykess (TKL)
- Compatible switches: MX-like only, features hotswap sockets
- Lighting: per-key RGB through IS31FL3741A intelligent chip and common-annode RGB LEDs
- Support for WS2812 RGB underglow through 4-pin JST
- Microcontroller: multi-chip ARM compatibility including:
  * STM32F411 (CEU6/CET6)
  * STM32F072 (CBT6/C8T6/CBU6/C8U6)
  * STM32F303 (CBT6/CBU6/CCT6/C8T6/C6T6)
- Connector: detachable USB Type C on the top side and JST connector for daughterboard support
- Firmware compatibility: QMK (with VIA support)
- Protection hardware:
  * USB data lines and power rail ESD suppressing
  * USB power overvoltage protection
  * Enclosure grounding pad
  * Overcurrent protection
  * LDO crowbar diode
  * EMI suppression (shielding ferrite bead)
- Current release: pre-release Gamma (has not been prototyped yet)
- Designer: Gondolindrim
- License: Acheron Open-Source Hardware License version 1.3

## Preliminary renders

![image](https://github.com/Gondolindrim/file_hosting/blob/main/apollo87h_v3_renders.png?raw=true)

## Keyboard compatibility

## Known compatibilities

- **Geonworks F1-8X and F1-6X:** confirmed by Geon, who tested the PCB 3D files against the case 3D files; live testing into a machined case confirms compatibility.

### Known incompatibilities

- **ai03 KBD8X MKII**: ai03 open-sourced the PCB files for his KBD8X. Alghtough Apollo's edges do fit inside the original PCB's, its connector is more protruded then the original PCB's.

- **PrismA18**: different layouts on the function row.

## Acknowledgements

- The first prototypes of this PCB were paid for and tested by KeebsForAll, who also intends to make units of this PCB available for purchase.

- Geon, who kindly spent time helping design this PCB to fit his keyboards.

- Xelus, who kindly volunteered to help write the QMK firmware.

## Releases

- **Alpha**: uses SK6812-mini-E LEDs for the per-key LEDs. Does not support RGB underglow, removable USB connector or daughterboard.

- **Beta**: uses a more sophisticated IS31FL3741 RGB controller with common-anode RGB LEDs. Full-featured. **Warning**: revision beta did not go past pre-release since mid-prototyping the factory changed constraints;

- **Gamma**: same features as **Beta**; PCB constraints were changed to fit Elecrow's updated factory requirements.

## Copyright notice

This project is released under the Acheron Open-Hardware License V1.3. For the license, please refer to the LICENCE.md file.

The "apollo sun face" logo was licensed through purchase from the EnvatoMarket website; the source file and licensing proof can be found in ``./resources/apollo_logo``. The license was obtained in march 27, 2021 and allows the AcheronProject to redistribute the logo as open-source and allows anyone to sell the PCBs commercially, but it does not allow for reproduction, meaning that if you want to use the logo for your designs or products you will have to buy a license yourself.
