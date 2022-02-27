# Operational Amplifier
This is the detailed report about the design of operational amplifier. This design was done during Cloud based Analog IC Hackathon conducted by IIT-Hyderabad and VSD Corp.

## Contents
* [Introduction](https://github.com/psxrjar007x/Op_Amp/blob/main/README.md#introduction)
* [Circuit Implementation](https://github.com/psxrjar007x/Op_Amp/blob/main/README.md#circuit-implementation)
* [Tools Used](https://github.com/psxrjar007x/Op_Amp/blob/main/README.md#tools-used)
* [Schematics & Symbols](https://github.com/psxrjar007x/Op_Amp/blob/main/README.md#schematics--symbols)
* [Simulation & Waveform]()
* [Conclusion]()
* [Author]()
* [Acknowledgement]()
* [References]()

## Introduction
An operational amplifier was designed using 28nm process.Focusing on single input single output and minimising noise. The minimum input voltage swing may be in the order of millivolts and is the output is expected (theoretically) in few volts.

## Circuit Implementation
The circuit mainly consists of three main stages;
* [Differential stage](https://github.com/psxrjar007x/Op_Amp/blob/main/README.md#differential-stage)
    * Inverting 
    * Differential pair
* [Gain stage](https://github.com/psxrjar007x/Op_Amp/blob/main/README.md#gain--output-stage)
* [Output stage](https://github.com/psxrjar007x/Op_Amp/blob/main/README.md#gain--output-stage)

### Differential stage
This stage has two sub stages an [inverting](https://github.com/psxrjar007x/Op_Amp/blob/main/README.md#inverting) and an actual differential pair stages.
#### Inverting
This stage has a small signal voltage gain equals to negative one

### Gain & Output stage 
A common source mode with active load is used to produce necessary gain and for output stage i.e. to get very low output impedance, an nmos transistor was biased using current mirror and the expected output is taken from the source of the nmos transistor.

## Tools Used
* Synopsys Custom Compiler : A design environment which used for full-custom analog, custom digital, and mixed-signal IC design.
* Synopsys Primewave : For simulating the designed circuits under different conditions and time scales.
* Synopsys 28 nm PDK : A process design kit which has a comprehensive collection of 28nm transistor sets and libraries.

## Schematics & Symbols
The schematics and symbols for the [differential stage](https://github.com/psxrjar007x/Op_Amp/blob/main/README.md#differential-stage), [gain stage](https://github.com/psxrjar007x/Op_Amp/blob/main/README.md#gain--output-stage) and [Output stage](https://github.com/psxrjar007x/Op_Amp/blob/main/README.md#gain--output-stage) circuits were designed using the Synopsys’ PrimeSim™ HSPICE® powered schematic editor.

### Differential Stage

This stage was designed as a schematic and then implemented as a symbol for later integration into the final circuit of the opamp.

#### Inverting Circuit

<img width="1440" alt="Screenshot 2022-02-27 at 6 52 00 PM" src="https://user-images.githubusercontent.com/100516989/155888924-bddce70d-8369-4cae-aba5-39d03cbd24af.png">
