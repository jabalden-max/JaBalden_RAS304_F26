---
title: Component Selection
---

*Table 1: High-Side Current Sense Amplifier & Shunt (Power Subsystem)*

**High-Side Current Sense Amplifier & Shunt (Power Subsystem)**

| **Solution** | **Pros** | **Cons** |
| --- | --- | --- |
| ![INA180A1IDBVR](ina180a1idbvr.png)<br>Option 1.<br> INA180A1IDBVR Current Sense Amp<br>$0.85/each<br>[Digi-Key product page: INA180A1IDBVR](https://www.digikey.com/en/products/detail/texas-instruments/INA180A1IDBVR/8132986) · [TI datasheet](https://www.ti.com/lit/ds/symlink/ina180.pdf) | \* Wide common-mode input range (2.7V to 26V) independent of supply<br>\* High accuracy with low offset voltage (150 µV max)<br>\* Compact SOT-23-5 package saves PCB space | \* Requires precise, low-value external current shunt resistor<br>\* Fixed gain variant must be selected at purchase. |
| ![MAX44284EAUT+T](max44284eaut.png)<br>Option 2.<br> MAX44284EAUT+T Current Sense Amp<br>$1.42/each<br>[Analog Devices product page: MAX44284](https://www.analog.com/en/products/max44284.html) · [datasheet](https://www.analog.com/media/en/technical-documentation/data-sheets/max44284.pdf) | \* Ultra-low supply current consumption (21 µA)<br>\* Extremely low input offset voltage for high precision<br>\* Wide dynamic operating range | \* Higher unit cost compared to Texas Instruments alternatives<br>\* Potential supply chain lead time fluctuations |

**Choice:** Option 1: INA180A1IDBVR Current Sense Amp

**Rationale:** The INA180 offers an optimal balance of cost, high common-mode voltage handling, and factory-trimmed gain accuracy. Using a dedicated current-sense IC avoids the CMRR degradation common with discrete differential amplifier circuits while keeping the board layout compact.

*Table 2: Voltage Regulators (Power Subsystem)*

**Voltage Regulators (Power Subsystem)**

| **Solution** | **Pros** | **Cons** |
| --- | --- | --- |
| ![LM7805CT](images/lm7805ct.png)<br>Option 1.<br> LM7805CT Linear Regulator<br>$0.65/each<br>[Digi-Key product page: LM7805CT/NOPB](https://www.digikey.com/en/products/detail/texas-instruments/LM7805CT-NOPB/3901929) · [TI datasheet](https://www.ti.com/lit/ds/symlink/lm7800.pdf) | \* Simple implementation requiring minimal external capacitors<br>\* Robust internal thermal overload and short-circuit protection<br>\* Through-hole package is easy to prototype and solder | \* Low efficiency when stepping down from higher voltages (high thermal dissipation)<br>\* Fixed 5V output voltage only. |
| ![TPS54302DDCR](images/tps54302ddcr.png)<br>Option 2.<br> TPS54302DDCR Step-Down Buck Regulator<br>$1.10/each<br>[Digi-Key product page: TPS54302DDCR](https://www.digikey.com/en/products/detail/texas-instruments/TPS54302DDCR/6572466) · [TI datasheet](https://www.ti.com/lit/ds/symlink/tps54302.pdf) | \* High power conversion efficiency (up to 95%) minimizing heat dissipation<br>\* Supports continuous output currents up to 3A<br>\* Adjustable output voltage via feedback resistors | \* Requires external inductor and filter capacitors (larger layout)<br>\* Surface-mount thermal pad requires careful soldering |

**Choice:** Option 2: TPS54302DDCR Step-Down Buck Regulator

**Rationale:** Switching buck regulators like the TPS54302 are essential for our handheld system to prevent excessive power loss and thermal buildup compared to linear regulators, especially when dropping battery voltage down to logic and sensor levels.

*Table 3: Protection / Power Switch (Power Subsystem)*

**Protection / Power Switch (Power Subsystem)**

| **Solution** | **Pros** | **Cons** |
| --- | --- | --- |
| ![Rocker power switch](images/d101j12s215dqa.png)<br>Option 1.<br> Rocker Power Switch (12V/10A)<br>$1.20/each<br>[Littelfuse / C&K rocker switch datasheet](https://www.littelfuse.com/assetdocs/littelfuse-c-k-rocker-d-series-datasheet?assetguid=8731c953-f4bd-4993-b6ef-d4e1e9d52f9c) | \* High current handling capacity (>10A safely)<br>\* Clear tactile feedback for physical on/off user status<br>\* Panel-mount design secure against mechanical shock | \* Manual electromechanical switch (cannot be toggled via software)<br>\* Bulkier physical footprint on enclosure. |
| ![MAX17613](images/max17613.png)<br>Option 2.<br> MAX17613 High-Voltage Overvoltage Protector IC<br>$2.15/each<br>[Analog Devices product page: MAX17613](https://www.analog.com/en/products/max17613a) | \* Automatic electronic overvoltage and reverse-polarity protection<br>\* Integrated low-resistance MOSFET switch<br>\* Compact IC package | \* Higher component unit cost<br>\* Does not provide a physical mechanical disconnect |

**Choice:** Option 1: Rocker Power Switch (12V/10A)

**Rationale:** A robust mechanical power switch provides an unmistakable master disconnect for the handheld battery pack, ensuring safety during transport and servicing while easily handling total system startup surge currents.                                               |

**Choice:** Option 1: Rocker Power Switch (12V/10A)

**Rationale:** A robust mechanical power switch provides an unmistakable master disconnect for the handheld battery pack, ensuring safety during transport and servicing while easily handling total system startup surge currents.
