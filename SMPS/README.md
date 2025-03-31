# Switch mode power supply for RC-TANK
Switch mode power supply should be able to generate all the necessery voltages for use in the tank. That are 7.4V for DC motor, 5V for controll logic, 6V for servomechanisms and 12V for additional devices such as DC fans. Additionally it should feature a wide range of input voltages for instance 12.5V - 35V. On top of that power supply should have shortcircuit protection, undervoltage protection and overtemperature protection. Moreover, in order order to limit inrush current for the circuit I decided to use high-side mosfet as softstart.

Tab.1.1 Voltages and current requirements

| Voltage | Maximum current | Maximum power|
|-----------|--------|---------|
| 7.4 [V]   | 40 [A] | 296 [W] |
| 12 [V]    | 20 [A] | 240 [W] |
| 6 [V]     | 20 [A] | 120 [W] |
| 5 [V]     | 5 [A]  | 25 [W]  |
| Total     | 85 [A] | 681 [W] |

When designing switch mode power supply it is advised to choose the right topology depending on power output. That's why, I have decided to use half-bridge topology for sections 7.4V and 12V and buck topology for sections 5V and 6V.

Tab.1.2 Design requirements for section 7.4V

| Voltage | Maximum power|
|-----------|---------|
| Topology| Half-Bridge |
| Output voltage | 7.4 [V]|
| Output current | 40 [A]|
| Working frequency | 500 [kHz] |
| Coil inductance min. | 16 [uH] |
| Coil core material | T130-52 |
| Coil wire diameter | 2.36 [mm] |
| Switching transistors | IXTH94N20X4 |
| Conduction and switching losses per transistor | 22.5 [W] |
| Total power losses| 45 [W]|
| PWM Controller | TL3843 |
| Mosfet driver | IRS2008 |

Tab.1.3 Design requirements for section 12V

| Voltage | Maximum power|
|-----------|---------|
| Topology| Half-Bridge |
| Output voltage | 12 [V]|
| Output current | 20 [A]|
| Working frequency | 500 [kHz] |
| Coil inductance min. | 16 [uH] |
| Coil core material | T106-26B |
| Coil wire diameter | 1.60 [mm] |
| Switching transistors | STP60NF06 |
| Conduction and switching losses per transistor | 16.6 [W]|
| Total power losses | 33.2 [W]|
| PWM Controller | TL3843 |
| Mosfet driver | IRS2008 |

Tab.1.4 Design requirements for section 6V

| Voltage | Maximum power|
|-----------|---------|
| Topology| Buck |
| Output voltage | 6.0 [V]|
| Output current | 20 [A]|
| Working frequency | 500 [kHz] |
| Coil inductance min. | 16 [uH] |
| Coil core material | T106-26B |
| Coil wire diameter | 1.60 [mm] |
| Switching transistor | STP60NF06 |
| Freewheeling diode| RHRP3060|
| Conduction and switching losses in transistors | 16.6 [W] |
| Conduction losses in freewheeling diode| 14 [W]|
| Total power losses | 30.6 [W]|
| PWM Controller | TL3843 |
| Mosfet driver | IRS20752 |

Tab.1.5 Design requirements for section 5V

| Voltage | Maximum power|
|-----------|---------|
| Topology| Buck |
| Output voltage | 5 [V]|
| Output current | 5 [A]|
| Working frequency | 500 [kHz] |
| Coil inductance min. | 16 [uH] |
| Coil core material | T72-52 |
| Coil wire diameter | 0.80 [mm] |
| Switching transistor | STP60NF06 |
| Freewheeling diode| SB560 |
| Conduction and switching losses in transistors | 2.95 [W] |
| Conduction losses in freewheeling diode| 2.8 [W]|
| Total power losses | 5.75 [W]|
| PWM Controller | TL3843 |
| Mosfet driver | IRS20752 |

Tab.1.6 Design requirements for input section

| Voltage | Maximum power|
|-----------|---------|
| Input voltage | 12.5 - 35 [V]|
| Input current | 85 [A]|
| Softstart transistor | IRF100P218AKMA1 |
| Conduction and switching losses in transistors | 9.25 [W] |

Mosfet power losses were calculated using online calculator https://www.heatsinkcalculator.com/mosfet-power-loss-calculator.html   
Gate charge losses were negligible that is why they are not included

Overall simplified schematic of whole SMPS will look similiar to that:

<picture>
 <source media="(prefers-color-scheme: dark)" srcset="SMPS/SMPS_Simplified.PNG">
 <source media="(prefers-color-scheme: light)" srcset="SMPS/SMPS_Simplified.PNG">
 <img alt="YOUR-ALT-TEXT" src="SMPS/SMPS_Simplified.PNG">
</picture>

Current project of PCB board is a proof of concept which will allow to test the following:
1. Input MOSFET with RC circuit softstart   
2. TL3843 - PWM Controller   
3. IRS20752 - High side MOSFET DRIVER with bootstraping   
4. Output voltages   
5. Step-up conveter for gate of input MOSFET