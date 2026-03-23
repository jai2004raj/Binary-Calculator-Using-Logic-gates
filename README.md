4-Bit Binary Adder-Subtractor Simulator

Binary Calculator Using Logic GatesA comprehensive Project Based Learning (PBL) application that simulates a 4-bit Arithmetic Logic Unit (ALU) component. This project demonstrates how binary arithmetic is implemented at the hardware level using cascaded logic gates.

Overview

This project provides a hardware-accurate simulation of a 4-bit ripple carry adder-subtractor. It bridges the gap between high-level programming and low-level digital logic by implementing logic gate algorithms in two environments:

1. Interactive Web App: A tactile, breadboard-style simulator built with HTML5, CSS3, and Vanilla JS.
   
2. MATLAB Implementation: A command-line script for algorithmic verification and mathematical analysis.
  
Key Features

Dual-Mode Operation: Seamlessly toggle between Addition and Subtraction using a single circuit.

Hardware-Level Emulation: Accurate implementation of XOR conditional inverters and Full Adder blocks.

Dual Interpretation: Real-time conversion to Unsigned Decimal (0 to 15) and Signed 2’s Complement (-8 to +7).

Advanced Diagnostics: Automatic Signed Overflow Detection ($V = C_3 \oplus C_4$) and Carry-out analysis.

Dynamic Schematic: An interactive SVG diagram that updates to show signal flow through the gates.

Step-by-Step Debugging: A logic-trace feature that explains how carries propagate through each bit stage. 

How It Works

1. XOR Gates for Conditional Inversion

The circuit uses the XOR gate as a programmable inverter.

Mode 0 (Add): $B \oplus 0 = B$ (Input B remains unchanged).

Mode 1 (Sub): $B \oplus 1 = \bar{B}$ (Input B is inverted to 1’s complement).

2. Cascaded Full Adders

Four Full Adders are linked where the Carry Out of one bit becomes the Carry In of the next.

$$Sum = A \oplus B' \oplus C_{in}$$$$C_{out} = (A \cdot B') + (C_{in} \cdot (A \oplus B'))$$

3. Subtraction via 2's Complement

When in Subtraction mode, the circuit performs $A + (\bar{B} + 1)$. The "$+1$" is achieved by feeding the Mode signal (1) into the Carry In of the first bit ($C_0$).

Learning Outcomes 
By interacting with this simulator, the following concepts are mastered:

Ripple Carry Propagation: Visualizing the time delay ($T_{pd}$) and carry flow from LSB to MSB.

Arithmetic Circuits: Understanding how a single hardware unit handles two distinct mathematical operations.

Data Representation: Differentiating between how a machine stores bits and how humans interpret them (Signed vs. Unsigned).

Error Handling: Identifying when a mathematical result exceeds the hardware bit-width (Overflow).
