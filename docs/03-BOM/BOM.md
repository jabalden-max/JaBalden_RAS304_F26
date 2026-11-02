---
title: Bill of Materials
tags:
- BOM
- power board
- TEST_304
---

## Overview
This page lists every part on the power board schematic (`TEST_304.kicad_sch`): input protection, an LM7805 logic rail, a TPS54302 5 V buck for the motor supply, low-side current sense, the PIC18F57Q43 Curiosity Nano, UART ribbon, spare GPIO headers, debug LEDs and test points. The BOM was exported from KiCad (`bom_csv_grouped_by_value`); all parts are ordered from **Digi-Key**. Table 1 covers the PCB parts with 1 spare, and Table 2 adds a breadboard-compatible (through-hole or breakout) version of each part so the circuit can be tested before moving to the PCB. Unit prices are estimates at quantity 1 and will be confirmed at checkout; rows marked "(verify)" need the exact part number confirmed.

## Bill of Materials

*Table 1: PCB parts (final board + spares)*

| **Part Name/Description** | **Qty** | **Unit Cost** | **Total Cost** | **Manufacturer** | **Manufacturer #** | **Vendor Link** | **Datasheet Link** | **Schematic Reference Designators** |
|:--------------------|:----|:---------------|:-----|:--------|:-----|:-----|:----|:-----|
| 0.1uF 50V X7R 0805 | 6 | $0.10 | $0.60 | Samsung | CL21B104KBCNNNC | [DigiKey](https://www.digikey.com/en/products/result?keywords=CL21B104KBCNNNC) | see vendor page | C1 |
| 0.1uF 16V X7R 0805 | 6 | $0.10 | $0.60 | Samsung | CL21B104KOCNNNC | [DigiKey](https://www.digikey.com/en/products/result?keywords=CL21B104KOCNNNC) | see vendor page | C3, C4, C7, C10 |
| 1uF 16V X7R 0805 | 2 | $0.10 | $0.20 | Samsung | CL21B105KOFNNNG | [DigiKey](https://www.digikey.com/en/products/result?keywords=CL21B105KOFNNNG) | see vendor page | C2 |
| 0.33uF 50V X7R 0805 | 2 | $0.15 | $0.30 | Samsung | CL21B334KBFNNNE (verify) | [DigiKey](https://www.digikey.com/en/products/result?keywords=0.33uF+50V+0805+X7R) | see vendor page | C5 |
| 10uF 50V X7R 1210 | 2 | $0.60 | $1.20 | Samsung | CL32B106KBJNNNE | [DigiKey](https://www.digikey.com/en/products/result?keywords=CL32B106KBJNNNE) | see vendor page | C6 |
| 22uF 10V X5R 1210 | 3 | $0.45 | $1.35 | Samsung | CL32A226MPJNNNE | [DigiKey](https://www.digikey.com/en/products/result?keywords=CL32A226MPJNNNE) | see vendor page | C8, C9 |
| 330 ohm 1% 0805 | 3 | $0.10 | $0.30 | Yageo | RC0805FR-07330RL | [DigiKey](https://www.digikey.com/en/products/result?keywords=RC0805FR-07330RL) | see vendor page | R1, R2 |
| 10k 1% 0805 | 5 | $0.10 | $0.50 | Yageo | RC0805FR-0710KL | [DigiKey](https://www.digikey.com/en/products/result?keywords=RC0805FR-0710KL) | see vendor page | R3, R7, R11 |
| 1k 1% 0805 | 4 | $0.10 | $0.40 | Yageo | RC0805FR-071KL | [DigiKey](https://www.digikey.com/en/products/result?keywords=RC0805FR-071KL) | see vendor page | R5, R6, R8 |
| 100k 1% 0805 | 2 | $0.10 | $0.20 | Yageo | RC0805FR-07100KL | [DigiKey](https://www.digikey.com/en/products/result?keywords=RC0805FR-07100KL) | see vendor page | R9 |
| 73.2k 1% 0805 (buck FB) | 2 | $0.10 | $0.20 | Yageo | RC0805FR-0773K2L | [DigiKey](https://www.digikey.com/en/products/result?keywords=RC0805FR-0773K2L) | see vendor page | R10 |
| 0.1 ohm 2W 2512 shunt | 1 | $0.55 | $0.55 | TBD (verify) | 2512 0.1R 2W (verify) | [DigiKey](https://www.digikey.com/en/products/result?keywords=2512+0.1+ohm+2W+current+sense) | see vendor page | R4 |
| LED red 0805 | 2 | $0.30 | $0.60 | Lite-On | LTST-C171KRKT | [DigiKey](https://www.digikey.com/en/products/result?keywords=LTST-C171KRKT) | see vendor page | D1 |
| LED yellow 0805 | 2 | $0.30 | $0.60 | Lite-On | LTST-C171KSKT | [DigiKey](https://www.digikey.com/en/products/result?keywords=LTST-C171KSKT) | see vendor page | D2 |
| LED green 0805 (power) | 2 | $0.30 | $0.60 | Lite-On | LTST-C171KGKT | [DigiKey](https://www.digikey.com/en/products/result?keywords=LTST-C171KGKT) | see vendor page | D4 |
| 1N5822 3A 40V Schottky, DO-201AD (through-hole, also breadboard-safe) | 2 | $0.55 | $1.10 | onsemi | 1N5822RLG | [DigiKey](https://www.digikey.com/en/products/result?keywords=1N5822RLG) | see vendor page | D3 |
| 3A hold polyfuse 16V 1812 | 1 | $0.60 | $0.60 | Littelfuse | 1812L300/16 (verify) | [DigiKey](https://www.digikey.com/en/products/result?keywords=1812+polyfuse+3A+hold+16V) | see vendor page | F1 |
| 10uH >=4A sat, 7x7mm shielded | 1 | $1.20 | $1.20 | Bourns | SRP7028A-100M | [DigiKey](https://www.digikey.com/en/products/result?keywords=SRP7028A-100M) | see vendor page | L1 |
| Barrel jack 2.1mm, horizontal | 1 | $1.10 | $1.10 | CUI Devices | PJ-002A | [DigiKey](https://www.digikey.com/en/products/result?keywords=PJ-002A) | see vendor page | J1 |
| JST XH 2-pos header | 4 | $0.15 | $0.60 | JST | B2B-XH-A(LF)(SN) | [DigiKey](https://www.digikey.com/en/products/detail/jst-sales-america-inc/B2B-XH-A-LF-SN/1651045) | [datasheet](https://www.jst-mfg.com/product/pdf/eng/eXH.pdf) | J4, J5, J6 |
| JST XH 2-pos housing | 4 | $0.10 | $0.40 | JST | XHP-2 | [DigiKey](https://www.digikey.com/en/products/result?keywords=XHP-2) | [datasheet](https://www.jst-mfg.com/product/pdf/eng/eXH.pdf) | J4, J5, J6 (mating) |
| JST XH crimp contacts | 12 | $0.05 | $0.60 | JST | SXH-001T-P0.6 | [DigiKey](https://www.digikey.com/en/products/result?keywords=SXH-001T-P0.6) | [datasheet](https://www.jst-mfg.com/product/pdf/eng/eXH.pdf) | J4, J5, J6 (mating) |
| 1x40 male header 2.54mm (snap to length) | 3 | $0.60 | $1.80 | Sullins | PRPC040SAAN-RC | [DigiKey](https://www.digikey.com/en/products/result?keywords=PRPC040SAAN-RC) | see vendor page | J2, J3, J7, J8 |
| 2x4 IDC shrouded header 2.54mm | 1 | $0.70 | $0.70 | TBD (verify) | 2x4 IDC shrouded header (verify) | [DigiKey](https://www.digikey.com/en/products/result?keywords=2x04+shrouded+header+2.54mm) | see vendor page | J9 |
| SPDT slide switch | 1 | $0.90 | $0.90 | Nidec Copal | CAS-120A1 | [DigiKey](https://www.digikey.com/en/products/result?keywords=CAS-120A1) | see vendor page | SW1 |
| Test point SMD pad | 7 | $0.45 | $3.15 | Keystone | Keystone 5019 | [DigiKey](https://www.digikey.com/en/products/result?keywords=5019) | see vendor page | TP1-TP7 |
| LM7805 TO-220 (through-hole, also breadboard-safe) | 2 | $0.60 | $1.20 | STMicroelectronics | L7805CV | [DigiKey](https://www.digikey.com/en/products/result?keywords=L7805CV) | [datasheet](https://www.st.com/resource/en/datasheet/l78.pdf) | U1 |
| MCP6002 dual op amp SOIC-8 | 2 | $0.45 | $0.90 | Microchip | MCP6002-I/SN | [DigiKey](https://www.digikey.com/en/products/result?keywords=MCP6002-I%2FSN) | see vendor page | U2 |
| TPS54302 5V buck, SOT-23-6 | 2 | $0.95 | $1.90 | Texas Instruments | TPS54302DDCR | [DigiKey](https://www.digikey.com/en/products/detail/texas-instruments/TPS54302DDCR/6572466) | [datasheet](https://www.ti.com/lit/ds/symlink/tps54302.pdf) | U3 |
| PIC18F57Q43 Curiosity Nano (breadboard-ready with headers) | 1 | $10.19 | $10.19 | Microchip | DM164150 | [DigiKey](https://www.digikey.com/en/products/detail/microchip-technology/DM164150/11586705) | [datasheet](https://www.microchip.com/en-us/development-tool/DM164150) | U4 |
| 1x28 female header 2.54mm (Nano socket) | 2 | $1.20 | $2.40 | TBD (verify) | 1x28 female header (verify) | [DigiKey](https://www.digikey.com/en/products/result?keywords=1x28+female+header+2.54mm) | see vendor page | U4 (sockets) |

**PCB subtotal: $36.94**

*Table 2: Breadboard-compatible versions (one per schematic instance)*

| **Part Name/Description** | **Qty** | **Unit Cost** | **Total Cost** | **Manufacturer** | **Manufacturer #** | **Vendor Link** | **Datasheet Link** | **Schematic Reference Designators** |
|:--------------------|:----|:---------------|:-----|:--------|:-----|:-----|:----|:-----|
| 0.1uF 50V X7R radial through-hole | 5 | $0.25 | $1.25 | Kemet | C315C104K5R5TA (verify) | [DigiKey](https://www.digikey.com/en/products/result?keywords=C315C104K5R5TA) | see vendor page | C1, C3, C4, C7, C10 (BB) |
| 1uF 50V X7R radial through-hole | 1 | $0.40 | $0.40 | Kemet | C322C105K5R5TA (verify) | [DigiKey](https://www.digikey.com/en/products/result?keywords=C322C105K5R5TA) | see vendor page | C2 (BB) |
| 0.33uF 50V X7R radial through-hole | 1 | $0.40 | $0.40 | Kemet | C322C334K5R5TA (verify) | [DigiKey](https://www.digikey.com/en/products/result?keywords=C322C334K5R5TA) | see vendor page | C5 (BB) |
| 10uF 50V electrolytic radial | 1 | $0.25 | $0.25 | Nichicon | UVR1H100MDD (verify) | [DigiKey](https://www.digikey.com/en/products/result?keywords=UVR1H100MDD) | see vendor page | C6 (BB) |
| 22uF 25V electrolytic radial | 2 | $0.20 | $0.40 | Nichicon | UVR1E220MDD (verify) | [DigiKey](https://www.digikey.com/en/products/result?keywords=UVR1E220MDD) | see vendor page | C8, C9 (BB) |
| 330 ohm 5% 1/4W axial | 2 | $0.10 | $0.20 | Yageo | CFR-25JB-52-330R | [DigiKey](https://www.digikey.com/en/products/result?keywords=CFR-25JB-52-330R) | see vendor page | R1, R2 (BB) |
| 10k 5% 1/4W axial | 3 | $0.10 | $0.30 | Yageo | CFR-25JB-52-10K | [DigiKey](https://www.digikey.com/en/products/result?keywords=CFR-25JB-52-10K) | see vendor page | R3, R7, R11 (BB) |
| 1k 5% 1/4W axial | 3 | $0.10 | $0.30 | Yageo | CFR-25JB-52-1K | [DigiKey](https://www.digikey.com/en/products/result?keywords=CFR-25JB-52-1K) | see vendor page | R5, R6, R8 (BB) |
| 100k 5% 1/4W axial | 1 | $0.10 | $0.10 | Yageo | CFR-25JB-52-100K | [DigiKey](https://www.digikey.com/en/products/result?keywords=CFR-25JB-52-100K) | see vendor page | R9 (BB) |
| 73.2k 1% 1/4W axial (sets 5V, keep 1%) | 1 | $0.10 | $0.10 | Yageo | MFR-25FRF52-73K2 (verify) | [DigiKey](https://www.digikey.com/en/products/result?keywords=MFR-25FRF52-73K2) | see vendor page | R10 (BB) |
| 0.1 ohm 2W axial shunt | 1 | $0.90 | $0.90 | TBD (verify) | 0.1 ohm 2W axial (verify) | [DigiKey](https://www.digikey.com/en/products/result?keywords=0.1+ohm+2W+axial+resistor) | see vendor page | R4 (BB) |
| LED 5mm red | 1 | $0.25 | $0.25 | Kingbright | WP7113ID (verify) | [DigiKey](https://www.digikey.com/en/products/result?keywords=WP7113ID) | see vendor page | D1 (BB) |
| LED 5mm yellow | 1 | $0.25 | $0.25 | Kingbright | WP7113YD (verify) | [DigiKey](https://www.digikey.com/en/products/result?keywords=WP7113YD) | see vendor page | D2 (BB) |
| LED 5mm green | 1 | $0.25 | $0.25 | Kingbright | WP7113GD (verify) | [DigiKey](https://www.digikey.com/en/products/result?keywords=WP7113GD) | see vendor page | D4 (BB) |
| 3A hold polyfuse radial through-hole | 1 | $0.50 | $0.50 | Bourns | MF-R300-0-99 (verify) | [DigiKey](https://www.digikey.com/en/products/result?keywords=MF-R300-0-99) | see vendor page | F1 (BB) |
| 10uH 4A radial through-hole inductor | 1 | $1.50 | $1.50 | Bourns | 2100LL-100-H-RC (verify) | [DigiKey](https://www.digikey.com/en/products/result?keywords=2100LL-100-H-RC) | see vendor page | L1 (BB) |
| Breadboard-friendly 2.1mm barrel jack | 1 | $1.00 | $1.00 | Adafruit | 373 (verify) | [DigiKey](https://www.digikey.com/en/products/result?keywords=373) | see vendor page | J1 (BB) |
| SPDT slide switch, through-hole | 1 | $0.70 | $0.70 | E-Switch | EG1218 (verify) | [DigiKey](https://www.digikey.com/en/products/result?keywords=EG1218) | see vendor page | SW1 (BB) |
| MCP6002 dual op amp DIP-8 | 1 | $0.55 | $0.55 | Microchip | MCP6002-I/P | [DigiKey](https://www.digikey.com/en/products/result?keywords=MCP6002-I%2FP) | see vendor page | U2 (BB) |
| SOT-23-6 to DIP-6 adapter (for TPS54302) | 1 | $3.00 | $3.00 | Chip Quik | SMD-SOT236 (verify) | [DigiKey](https://www.digikey.com/en/products/result?keywords=SMD-SOT236) | see vendor page | U3 (BB) |

**BB subtotal: $12.60**

**Estimated total: $49.54** 

## Notes
* The Curiosity Nano, 1N5822, LM7805 and 1x40 headers are already breadboard-compatible. XH connectors, IDC header and test points use plain 2.54 mm header pins on the breadboard (from the 1x40 strips).
* The TPS54302 is SMD only; the SOT-23-6 adapter lets it be soldered onto a breadboard-friendly DIP footprint.
* Items likely stocked in TECH 162 (resistors, capacitors, LEDs, headers, fuses) can be removed from the order after checking the parts closet.
* Datasheets are to be saved in the repository's `datasheets/` folder.



