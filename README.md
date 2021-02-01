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

## Installation
There are several methods to copy the program to the HP71B Calculator.
The one described below uses the PILBOX http://www.jeffcalc.hp41.eu/hpil/ and EMU71 http://www.jeffcalc.hp41.eu/emu71/.
The description below is copied from http://www.namirshammas.com/HP71B/EMU71.htm

1. Copy the code, renaming it to emu_in.dat, to Emu71's home directory.
2. Enter this small program in Emu71
```basic
10 DIM A$[100]
15 INPUT "FILENAME? ";F$
20 CREATE TEXT F$
30 ASSIGN #1 TO F$
40 ENTER :DOSLINK;A$
50 DISP A$ ! just to follow the process, you can omit it
60 PRINT #1;A$
70 GOTO 40
```
The program prompts for a name. It will be the name of the program in EMU71.

Enter this small program in Emu71 (where MYTEXT is any legal name you want to give your PC text file when stored in the emulated 71B file system) exactly as written and RUN it:

## Thanks

Many thanks to Jean-Francois Garnier, Namir Shammas and Valentin Albillo
