# Transmission Gate Logic 1-bit Full Adder
1 - bit Full Adder design using Transmission Gate Logic and Conventional Inverter - 28nm Technology.
  * [Abstract](#abstract)
  * [Truth Table](#truth-table)
  * [Reference Circuit Details](#reference-circuit-details)
  * [Reference Diagram](#reference-diagram)
  * [Expected Waveform](#expected-waveform)
  * [Tools Used](#tools-used)
 
  
- [Simulation in Synopsys Custom Compiler](#simulation-in-synopsys)

  * [Schematic](#schematic)
  * [Symbol](#symbol)
  * [Input Parameters](#test-bench-schematic)
  * [Transient Simulation Settings](#transient-settings)
  * [Output Waveform](#output-waveform)
  * [Generated Netlist](#generated-netlist)
  * [Acknowledgement](#acknowledgement)
  * [Author](#author)
  * [References](#references)

## Abstract
Conventional CMOS design employs pull-up and pull-down resistors to implement a logic function. While it is fast, it has more number of transistors than the equivalent Transmission Gate Implementation. In addition, the conventional CMOS design has pull-up and pull-down resistors. While the transmission gate logic has fewer gates, it lacks driving capability.

In this design, a 1-bit full adder is designed using conventional CMOS inverters and transmission gate. This results in fewer gates and lesser power dissipation.

## Truth Table
<img src="https://github.com/NAvi349/trans-full-adder/blob/main/images/truth_table.jpg" width="25%" height="25%">

## Reference Circuit Details
The following is the Boolean expression for the sum and carry out functions.
sum = a ^ b ^ cin;
cout = ((a ^ b) & cin) | (a & b);
Efficient implementation of XOR is possible with fewer gates using the Transmission Gate Logic. The full adder in the design is implemented using NOR, NAND and majority NOT gates. The carry output is the complement of the majority NOT gate whose inputs are A, B, Cin.
The expected timing diagram is generated using ModelSim – Altera.

## Reference Diagram
<img src="https://github.com/NAvi349/trans-full-adder/blob/main/images/Reference%20Circuit.jpg" alt="" title="" width="50%" height="50%">

## Expected Waveform
<img src="https://github.com/NAvi349/trans-full-adder/blob/main/images/Waveform.jpeg" alt="" title="" width="50%" height="50%">

## Tools Used
* ModelSim - Altera - for simulation waveform generation
* Synopsys Custom Compiler - for design
* PrimeWave - for actual waveform generation

## Simulation in Synopsys
## Schematic
<img src="https://github.com/NAvi349/trans-full-adder/blob/main/images/Schematic.jpg" alt="" title="" width="50%" height="50%">

## Symbol
<img src="https://github.com/NAvi349/trans-full-adder/blob/main/images/Symbol.jpeg" alt="" title="" width="25%" height="25%">

## Test Bench Schematic
<img src="https://github.com/NAvi349/trans-full-adder/blob/main/images/Test_Circuit.jpg" alt="" title="" width="50%" height="50%">

## Transient Settings
<img src="https://github.com/NAvi349/trans-full-adder/blob/main/images/Transient_settings.jpg" alt="" title="" width="50%" height="50%">

## Output Waveform
<img src="https://github.com/NAvi349/trans-full-adder/blob/main/images/Output_Waveform.jpg" alt="" title="" width="75%" height="75%">

## Generated Netlist
<a href = https://github.com/NAvi349/trans-full-adder/blob/main/netlist/netlist.txt> Netlist </a>

## Acknowledgement
1. Kunal Ghosh, Co-founder, VSD Corp. Pvt. Ltd.
2. Synopsys India
3. <a href = https://www.iith.ac.in/events/2022/02/15/Cloud-Based-Analog-IC-Design-Hackathon/>Cloud Based Analog IC Design Hackathon </a>

## Author
Navinkumar K is a student of PTU, Puducherry of 2023 Batch. He is a student of Electronics and Communication Engineering.

## References
[1] Khare, Kavita & Shukla, Krishna. (2010). Design A 1Bit Low Power Full Adder Using Cadence Tool. AIP Conference Proceedings. 1324. 373-376. 10.1063/1.3526237.
