# Design-of-CMOS-AND-Gate
This repositry presents the design of a CMOS AND Gate using Synopsys Custom Compiler on a 28nm PDK.

## Contents

1.[Introduction](#Introduction)
2.[Working](#Working)
3. Reference Circuit
4. Implementation
5. Simulation 
6. Netlist
7. References
8. Acknowledgements
9. Author

## Introduction
Digital Gates are one of the most fundamental building blocks of digital cirucits and nowadays digital circuits are present everywhere. This repositry presents the design, analysis and simulation of a CMOS AND Gate using Synopsys Custom Compiler on a 28nm PDK. An AND Gate is a digital logic gate which accepts 2 inputs and outputs a high if and only if both the inputs are high.CMOS is a specific fabrication technology where both NMOS and PMOS transistors used. Digital circuits implemented in CMOS technology are known for their effective use of electric power. They primarily only use power when switching from one state to another. 

## Working
The CMOS AND Gate is implemented by combining the CMOS NAND Gate and the CMOS inverter. The CMOS NAND Gate is implemented using a pull-up network consisting of 2 PMOS transistors in parallel and a pull-down network consisting of 2 NMOS transistors in series. Even if one of the 2 inputs to the NAND Gate become low one of the 2 PMOS transistors in parallel become on and they pull the output to logic high. On the other hand if both the inputs to the NAND Gate are high then the pull-down network becomes active and pulls to output to a logic low. The CMOS inverter outputs a high for a low input and a low for a high input. If we now feed the output of the CMOS NAND Gate to the CMOS inverter then the final output becomes high only if both the inputs to the circuit are high. Hence we have successfully implemented a CMOS AND Gate.

## Reference Circuits
### CMOS INVERTER Schematic
![CMOS INVERTER](/CMOS_Inverter.png)
### CMOS NAND Gate Schematic
![CMOS NAND Gate](/CMOS_NAND_Gate.png)
### CMOS AND Gate Schematic
![CMOS AND Gate](/AND_Gate.png)

## Tools Used
- Synopsys Custom Compiler
- Synopsys Primewave
- Synopsys 28nm PDK

## Implementation
- Total number of transistors used : 6
- Number of NMOS transistors used: 3
- Number of PMOS transistors used: 3
- The MOSFET model that has been chosen is the TT model from the 28nm PDK 
- The W/L ratio of the NMOS transistor in the inverter: 0.12um/0.03um
- The W/L ratio that has been chosen for the NMOS transistors in the NAND Gate: 0.24u/0.03u
- The W/L ratio that has been chosen for the PMOS transistor in the inverter: 0.24u/0.03u
- The W/L ratio that has been chosen for the PMOS transistors in the NAND Gate: 0.24u/0.03u

![CMOS AND Gate Schematic](/CMOS_AND_Gate_Schematic.jpg)

## Simulation
![CMOS AND Gate Simulation](/CMOS_AND_Gate_simulation.jpg)
**From the above plots we can clearly see that the output is high if and only if both inputs are high**

## Netlist
![NETLIST](/Netlist.png)

## Author
V.Adithyaa, 3rd year B.Tech Instrumentation and Control Engineering student at National Institute of Technology Trichy

## Acknowledgements
* Kunal Ghosh, Co-founder, VSD Corp.Pvt.Ltd
* Synopsys India
* IIT Hyderabad
* Sumanto Kar, IIT Bombay
* Chinmaya Panda, IIT Hyderabad

## References
Digital Integrated Circuits : A Design Perspective (Jan Rabaey and Anantha Chandrakasan)








