# Roark for HP-71B Calculator
Roarks's Formula for Stress and Strain
http://materiales.azc.uam.mx/gjl/Clases/MA10_I/Roark%27s%20formulas%20for%20stress%20and%20strain.pdf

## Shear, moment, slope, and deflection formulas for elastic straight beams (Table 8.1)

### Concentrated intermediate load
Case 1a to 1f are implemented

### Partial distributed load
Case 2a to 2f are implemented

## Usage
The program asks for the inputs. The variable names are the same as defined in the Roark's.

## Outputs
The program computes:
- The reaction forces at beam supports
- The bending moment at beam supports
- The maximum bending moment
- The maximum deflection
- The deflection along the beam for a given range

## Requirements
This program uses the Math Rom.
If you follow the instruction below for installation, you also need the Math Rom installed in EMU71.
See EMU71 help for How to install the Rom into the emulator.

## Installation
There are several methods to copy the program to the HP71B Calculator.
The one described below uses the PILBOX http://www.jeffcalc.hp41.eu/hpil/ and EMU71 http://www.jeffcalc.hp41.eu/emu71/.
The description below is derived from http://www.namirshammas.com/HP71B/EMU71.htm.

1. Copy the code, renaming it to emu_in.dat, to Emu71's home directory.
2. Enter this small program in Emu71.
```bas

10 DIM A$[100]
15 INPUT "FILENAME? ";F$
20 CREATE TEXT F$
30 ASSIGN #1 TO F$
40 ENTER :DOSLINK;A$
50 DISP A$ ! just to follow the process, you can omit it
60 PRINT #1;A$
70 GOTO 40
```
3. Run the program in EMU71. The program prompts for a name. It will be the name of the ROARK program in EMU71.
4. Close the file by executing from the keyboard:
```bas
        ASSIGN #1 to *
```
5. The text file is now in the emulated HP-71B file system, as a proper 71B TEXT file, with the name you chose. You can now transform it from its text form to a BASIC program by executing from the keyboard (replace ROARK with the name you chose):
```bas
         TRANSFORM ROARK INTO BASIC
```
6. You can now copy the file to HDRIVE1 by executing from the keyboard (replace ROARK with the name you chose):
```bas
         COPY ROARK TO ":HDRIVE1"
```
7. The file HDRIVE1.dat is now able to be used to transfer directly its content with the PILBOX. Replace the HDRIVE1.dat file from ILPER with the one from EMU71, Connect you HP-71B to the PILBOX, run ILPER, and execute the following command on your (real) HP71B:
```bas
         COPY "ROARK:HDRIVE1"
```

## Thanks

Many thanks to Jean-Francois Garnier, Namir Shammas and Valentin Albillo
