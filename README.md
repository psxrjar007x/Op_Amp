# Operational Amplifier
This is the detailed report about the design of operational amplifier. This design was done during Cloud based Analog IC Hackathon conducted by IIT-Hyderabad and VSD Corp.

## Contents
* [Introduction](https://github.com/psxrjar007x/Op_Amp/blob/main/README.md#introduction)
* [Circuit Implementation](https://github.com/psxrjar007x/Op_Amp/blob/main/README.md#circuit-implementation)
* [Reference Circuit & output waveform](https://github.com/psxrjar007x/Op_Amp/blob/main/README.md#reference-circuit--output-waveform)
* [Tools Used](https://github.com/psxrjar007x/Op_Amp/blob/main/README.md#tools-used)
* [Schematics & Symbols](https://github.com/psxrjar007x/Op_Amp/blob/main/README.md#schematics--symbols)
* [Circuit Prameters](https://github.com/psxrjar007x/Op_Amp/blob/main/README.md#circuit-prameters)
* [Simulation & Waveform](https://github.com/psxrjar007x/Op_Amp/blob/main/README.md#simulation--waveform)
* [Netlist](https://github.com/psxrjar007x/Op_Amp/blob/main/README.md#netlist)
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

## Reference Circuit & output waveform

### Circuit 

<img width="1349" alt="Screenshot 2022-02-27 at 11 12 12 PM" src="https://user-images.githubusercontent.com/100516989/155893436-9e21fdd8-61b6-4b7e-b0be-f7bf4b47b13d.png">

### Waveform

<img width="393" alt="Screenshot 2022-02-27 at 11 23 44 PM" src="https://user-images.githubusercontent.com/100516989/155893786-a9cfa4ea-1353-453e-a385-7058a0de1d85.png">

## Tools Used
   * Synopsys Custom Compiler : A design environment which used for full-custom analog, custom digital, and mixed-signal IC design.
   * Synopsys Primewave : For simulating the designed circuits under different conditions and time scales.
   * Synopsys 28 nm PDK : A process design kit which has a comprehensive collection of 28nm transistor sets and libraries.

## Schematics & Symbols
   The schematics and symbols for the [differential stage](https://github.com/psxrjar007x/Op_Amp/blob/main/README.md#differential-stage-1), [gain stage](https://github.com/psxrjar007x/Op_Amp/blob/main/README.md#gain-stage) and [Output stage](https://github.com/psxrjar007x/Op_Amp/blob/main/README.md#output-stage) circuits were designed separately using the Synopsys’ PrimeSim™ HSPICE® powered schematic editor and the to complete the actual [opamp](https://github.com/psxrjar007x/Op_Amp/blob/main/README.md#opamp-circuit-schematic).

### Differential Stage

   This stage was designed as a schematic and then implemented as a symbol for later integration into the final circuit of the opamp.

#### Inverting Circuit Schematic

<img width="1440" alt="Screenshot 2022-02-27 at 6 52 00 PM" src="https://user-images.githubusercontent.com/100516989/155888924-bddce70d-8369-4cae-aba5-39d03cbd24af.png">

#### Inverting Circuit Symbol

<img width="1440" alt="Screenshot 2022-02-27 at 6 52 13 PM" src="https://user-images.githubusercontent.com/100516989/155888986-272e506e-955c-491b-9d8f-d523e68cf03b.png">

#### Differential Amplifier Circuit Schematic

<img width="1440" alt="Screenshot 2022-02-27 at 10 41 50 PM" src="https://user-images.githubusercontent.com/100516989/155892454-4d5b4585-017e-4346-8285-28d9d337a2e9.png">


#### Differential Amplifier Circuit Symbol

<img width="1440" alt="Screenshot 2022-02-27 at 6 53 10 PM" src="https://user-images.githubusercontent.com/100516989/155889044-816356e9-aa0f-4b0a-89c8-93f674ef9726.png">

### Gain Stage

   This stage was designed as a schematic and then implemented as a symbol for later integration into the final circuit of the opamp.

#### Gain stage Circuit Schematic

<img width="1440" alt="Screenshot 2022-02-27 at 6 54 22 PM" src="https://user-images.githubusercontent.com/100516989/155889094-7fb0dad1-7357-4c92-a6d0-8c13644d835e.png">

#### Gain stage Circuit Symbol

<img width="1440" alt="Screenshot 2022-02-27 at 6 54 29 PM" src="https://user-images.githubusercontent.com/100516989/155889108-5d5f45db-0a3c-4d88-94a9-959d7cfc8ed1.png">

### Output Stage

   This stage was designed as a schematic and then implemented as a symbol for later integration into the final circuit of the opamp.

#### Output stage Circuit Schematic

<img width="1440" alt="Screenshot 2022-02-27 at 6 55 38 PM" src="https://user-images.githubusercontent.com/100516989/155889146-be0d22c7-32fb-4d0d-838a-a5bd9f106258.png">

#### Output stage Circuit Symbol

<img width="1440" alt="Screenshot 2022-02-27 at 6 55 52 PM" src="https://user-images.githubusercontent.com/100516989/155889157-646593fe-1a5e-49d2-9d87-334faf8e45ea.png">

### OpAmp Circuit Schematic 

   All the symbols from the previous stage and other active and passive elements along with bias voltages and test input sinusoidal signal were connected to get the required opamp circuit

<img width="1440" alt="Screenshot 2022-02-27 at 6 50 24 PM" src="https://user-images.githubusercontent.com/100516989/155889233-ff47f052-c183-44f1-9db6-e93f318d3186.png">

## Circuit Prameters

   This circuit design has no influence in the mos parameters, so everything was set to default; except at the [gain stage](https://github.com/psxrjar007x/Op_Amp/blob/main/README.md#gain-stage) where the M18 nmos has 4 times the width compared to other transistors to get 1/4th of the current used in other stages.

   Voltage dividers were designed using resistors to get DC 1.25v at the gate of M2 & M3 nmos in [differential stage](https://github.com/psxrjar007x/Op_Amp/blob/main/README.md#differential-stage-1).
   
   Capacitance of the capacitors were chosen as 10μF.
   
   Input test signal is choosed as a sinusoidal wave with 2.5mV Vpeak and 100KHz frequency.
 
## Simulation & Waveform

The simulation of the opamp circuit was obtained through PrimeWave™ Design Environment using its TestSuite and Waveform viewer.

### Testbench Settings

   * Go to tools > primesim
   * In primesim select the model file (/PDK/SAED_PDK32nm/hspice).
   * Select the type of analysis;
         * Analysis type -> tran
         * Start time -> 0
         * Stop time -> 0.05ms
   * Select the nodes to diplay
         * v(Ninput)
         * v(Noutf)

<img width="1440" alt="Screenshot 2022-02-27 at 6 50 33 PM" src="https://user-images.githubusercontent.com/100516989/155891423-1cbae780-8956-4ef6-b1ae-5788ca11370a.png">

### Output

   * Simulation > netlist&run

<img width="1440" alt="Screenshot 2022-02-27 at 6 51 06 PM" src="https://user-images.githubusercontent.com/100516989/155891451-2e4c6566-0e97-46bf-99f2-d9446e25e3e4.png">
  
## Netlist

<img width="1440" alt="Screenshot 2022-02-27 at 7 00 40 PM" src="https://user-images.githubusercontent.com/100516989/155893921-4b24d5b6-8def-4686-8d47-dc7b5a07f93e.png">

### netlist.txt

>\*  Generated for: PrimeSim
>\*  Design library name: Abishek
>\*  Design cell name: opamp
>\*  Design view name: schematic
>\.lib 'saed32nm.lib' TT
>\
>\*Custom Compiler Version S-2021.09
>\*Sun Feb 27 13:27:46 2022
>\
>\.global gnd! vdd!
>\********************************************************************************
>\* Library          : Abishek
>\* Cell             : inv
>\* View             : schematic
>\* View Search List : hspice hspiceD schematic spice veriloga
>\* View Stop List   : hspice hspiceD
>\********************************************************************************
>\.subckt inv v1 vdd vss cin nv1 vt_bulk_n_gnd!
>\xm4 net11 cin vss vt_bulk_n_gnd! n105 w=0.1u l=0.03u nf=1 m=1
>\xm3 nv1 v1 net11 vt_bulk_n_gnd! n105 w=0.1u l=0.03u nf=1 m=1
>\xm2 net8 gnd! net11 vt_bulk_n_gnd! n105 w=0.1u l=0.03u nf=1 m=1
>\xm1 vdd vdd nv1 vt_bulk_n_gnd! n105 w=0.1u l=0.03u nf=1 m=1
>\xm0 vdd vdd net8 vt_bulk_n_gnd! n105 w=0.1u l=0.03u nf=1 m=1
>\r7 v1 gnd! r=1k
>\r6 vdd v1 r=3k
>\.ends inv
>\
>\********************************************************************************
>\* Library          : Abishek
>\* Cell             : diff
>\* View             : schematic
>\* View Search List : hspice hspiceD schematic spice veriloga
>\* View Stop List   : hspice hspiceD
>\********************************************************************************
>\.subckt diff v1 vdd vss cin diff_vout nv1 vt_bulk_n_gnd! vt_bulk_p_vdd!
>\xm1 net7 net7 vdd vt_bulk_p_vdd! p105 w=0.1u l=0.03u nf=1 m=1
>\xm0 diff_vout net7 vdd vt_bulk_p_vdd! p105 w=0.1u l=0.03u nf=1 m=1
>\xm4 diff_vout nv1 net15 vt_bulk_n_gnd! n105 w=0.1u l=0.03u nf=1 m=1
>\xm3 net15 cin vss vt_bulk_n_gnd! n105 w=0.1u l=0.03u nf=1 m=1
>\xm2 net7 v1 net15 vt_bulk_n_gnd! n105 w=0.1u l=0.03u nf=1 m=1
>\r6 v1 gnd! r=1k
>\r5 vdd v1 r=3k
>\.ends diff
>\
>\********************************************************************************
>\* Library          : Abishek
>\* Cell             : gain_stage
>\* View             : schematic
>\* View Search List : hspice hspiceD schematic spice veriloga
>\* View Stop List   : hspice hspiceD
>\********************************************************************************
>\.subckt gain_stage cin vdd vin vss voutt vt_bulk_n_gnd! vt_bulk_p_vdd!
>\xm2 net11 net11 vdd vt_bulk_p_vdd! p105 w=1u l=0.05u nf=1 m=1
>\xm0 voutt net11 vdd vt_bulk_p_vdd! p105 w=0.1u l=0.03u nf=1 m=1
>\xm18 net11 cin vss vt_bulk_n_gnd! n105 w=0.4u l=0.03u nf=1 m=1
>\xm6 voutt vin gnd! vt_bulk_n_gnd! n105 w=0.1u l=0.03u nf=1 m=1
>\.ends gain_stage
>\
>\********************************************************************************
>\* Library          : Abishek
>\* Cell             : output
>\* View             : schematic
>\* View Search List : hspice hspiceD schematic spice veriloga
>\* View Stop List   : hspice hspiceD
>\********************************************************************************
>\.subckt output cin vdd vin vout vss vt_bulk_n_gnd! vt_bulk_p_vdd!
>\xm3 net13 net13 vdd vt_bulk_p_vdd! p105 w=0.1u l=0.03u nf=1 m=1
>\xm0 net7 net13 vdd vt_bulk_p_vdd! p105 w=0.1u l=0.03u nf=1 m=1
>\xm4 net13 cin vss vt_bulk_n_gnd! n105 w=0.1u l=0.03u nf=1 m=1
>\xm2 net7 vin vout vt_bulk_n_gnd! n105 w=0.1u l=0.03u nf=1 m=1
>\.ends output
>\
>\********************************************************************************
>\* Library          : Abishek
>\* Cell             : opamp
>\* View             : schematic
>\* View Search List : hspice hspiceD schematic spice veriloga
>\* View Stop List   : hspice hspiceD
>\********************************************************************************
>\xi0 vinput net35 net14 net41 net23 gnd! inv
>\xi1 vinput net35 net14 net41 net25 net22 gnd! vdd! diff
>\xi2 net41 net35 net24 net14 net27 gnd! vdd! gain_stage
>\xi3 net41 net35 net26 net29 net14 gnd! vdd! output
>\c7 voutf net29 c=10u
>\c6 net26 net27 c=10u
>\c5 net24 net25 c=10u
>\c4 net22 net23 c=10u
>\xm17 net45 net45 net41 gnd! n105 w=0.1u l=0.03u nf=1 m=1
>\xm16 net35 net35 net45 gnd! n105 w=0.1u l=0.03u nf=1 m=1
>\xm8 net41 net41 net14 gnd! n105 w=0.1u l=0.03u nf=1 m=1
>\v11 gnd! net14 dc=5
>\v10 net35 gnd! dc=5
>\v14 vinput gnd! dc=0 sin ( 0 2.5m 100k 0 0 0 )
>\
>\
>\
>\
>\
>\
>\
>\
>\.tran '0.001*(0.05m-0)' '0.05m' name=tran
>\
>\.option primesim_remove_probe_prefix = 0
>\.probe v(*) i(*) level=1
>\.probe tran v(vinput) v(voutf)
>\
>\.temp 25
>\
>\
>\
>\.option primesim_output=wdf
>\
>\
>\.option parhier = LOCAL
>\
>\
>\
>\
>\
>\
>\.end
