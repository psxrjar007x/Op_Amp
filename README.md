# Op_Amp
This is the detailed report about the design of operational amplifier. This design was done during Cloud based Analog IC Hackathon conducted by IIT-Hyderabad and VSD Corp.

## Contents
* [Introduction](https://github.com/psxrjar007x/Op_Amp/blob/main/README.md#introduction)
* [Circuit Implementation](https://github.com/psxrjar007x/Op_Amp/blob/main/README.md#circuit-implementation)
* [Tools Used]()
* [Schematics]()
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
* [Gain stage]
* [Output stage]

### Differential stage
This stage has two sub stages an [inverting](https://github.com/psxrjar007x/Op_Amp/blob/main/README.md#inverting) and an actual differential pair stages.
#### Inverting
This stage has a small signal voltage gain equals to negative one

### Gain & Output stage 
A common source mode with active load is used to produce necessary gain and for output stage i.e. to get very low output impedance, an nmos transistor was biased using current mirror and the expected output is taken from the source of the nmos transistor.
