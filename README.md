# MasterPlex_Preamp
Schematics &amp; Build information for MasterPlex, echoplex emulator Preamp PCB

![image](https://user-images.githubusercontent.com/53580358/202931932-c536fd57-5e68-476b-8332-cc7ba6249164.png)


## Build Notes

### JFET Selection
Notes found regarding FET Selection:
"The TIS58 FETs used in the original EP-3 are nearly impossible to find.
Even if you did find some they won’t help you too much:
FET manufacturing is notoriously inaccurate and you’ll find an enormous variance even
within one part number.
Not surprisingly, some original EP-3 units just didn’t have the “it” factor.
The preamp is such a simple circuit that the FET really does make it or break it."

"The best way to ensure that the FETs give the proper response is to test their IDSS value.
ClinchFX EP-Pre sorts his FETs and only uses ones that fall inside certain parameters.
I would recommend using his values as targets when selecting your own FETs.

Using a 9.6V wall wart supply and the circuit here
Q1 (the 2N5484) had an IDSS of 2.89mA, and Vp measured -1.32V.
Q2 (the 2N5485) had an IDSS of 7.62mA and  Vp measured -2.70V.

Fortunately, these values fall right about in the middle of the specified
ranges for both parts, meaning it should be easy to find ones that will work. 

Order maybe five of each of them and select the one that most
closely matches the above values.
You can even use other FETs as long as they measure the correct value.
In other test builds a 2N5952 for was used for Q1 and it sounds identical to a 
2N5484 with the same measurements.
J201 also might work"

## PCB Layout

![image](https://user-images.githubusercontent.com/53580358/202931970-8fb96bfd-4a22-4884-992b-a1703984af00.png)

## BOM

This is the best estimate of the required parts for each version, anything marked `YES` Should be included for this version of the build.
Alternative values are noted in the column for the other versions. Any part marked `Jumper` should be shorted together with jumper wires or 0 ohm resistors.
Components marked `omit` should not be placed. Other values and notes, or blank spaces are left to the builders discretion, especially if attempting to copy the origional Echoplex circuit as closely as possible, as this accounts for only the first half of the circuit, the 2nd active stage must be made up from the other versions.

 ref           | value5        | Echoplex  | Madbean/EP      | F.Briggs  | Aion       |
| ------------- | ------------- | --------- | --------------- | --------- | ---------- |
| Bias1         | 50k           | omit      | YES             | omit      | omit       |
| Boost1        | C10k          | choice    | YES             | YES       | 1M fixed   |
| C1            | 100n          | YES       | omit            | omit      | YES        |
| C2            | 22n           | Jumper    | Jumper          | Jumper    | YES        |
| C3            | 10n           | omit      | omit            | YES       | omit       |
| C4            | 3n3           | guess     | YES             | omit      | 220p       |
| C5            | 47n           | YES       | YES             | YES       | Jumper     |
| C6            | 22n           | Jumper    | Jumper          | Jumper    | YES        |
| C7            | 470n          |           | omit            | omit      | YES        |
| C8            | 100p          | YES       | omit            | omit      | 200p       |
| C9            | 100n          | YES       | YES             | YES       | YES        |
| D1            | 1N5817        | jumper    | if 18v          | if not    | jumper     |
| D2            | LEDA          | YES       | YES             | YES       | YES        |
| D3            | 1N5817        | jumper    | if 18v          | if not    | jumper     |
| EC1           | 10u           | omit      | YES             | YES       | omit       |
| EC2           | 10u           |           | YES             | YES       | omit       |
| EC3           | 10u           | choice    | YES             | YES       | 22u        |
| EC4           | 100u          | choice    | YES             | choice    | 47u        |
| EC5           | 47u           | YES       | YES             | YES       | YES        |
| EC6           | 10u           | if 18v    | if 18v          | if 18v    | if 18v     |
| EC7           | 100u          | YES       | YES             | YES       | YES        |
| FootswitchQC1 | BypassQC      | YES       | YES             | YES       | YES        |
| H1            | BoardQConnect |           |                 |           |            |
| IC1           | ICL7660S      |           | if 18v , if not | jumper    | pin 2&3    |
| M1            | SND           |           |                 |           |            |
| M9            | Vin           |           |                 |           |            |
| Q1            | 2N5457        |           |                 | See notes | See notes  |
| Q2            | 2N5088-       |           | YES             |           |            |
| Q3            | 2N5457        | see notes | see notes       | see notes | see notes  |
| R1            | 15k           |           | omit            | Jumper    | YES        |
| R10           | 33k           | 100k      | YES             | YES       | 100k       |
| R11           | 100k          |           | Omit            | Omit      | YES        |
| R12           | 3k3           |           | omit            | YES       | 10k        |
| R13           | 10k           |           | YES             | omit      | omit       |
| R14           | 1M            | Omit      | YES             | YES       | 4m7        |
| R15           | 1M            | YES       | YES             | YES       | YES        |
| R16           | 470k          | omit      | omit            | omit      | YES        |
| R17           | 4k7           | 3k3       | YES             | YES       | 3k3        |
| R18           | 47k           |           | YES             | omit      | omit       |
| R19           | 100r          | YES       | 100r            | 100r      | 60r        |
| R2            | 1M            | guess     | YES             | YES       | omit       |
| R20           | CLR           | CLR       | CLR             | CLR       | CLR        |
| R21           | 10k           | YES       | YES             | YES       | YES        |
| R22           | 10k           | YES       | YES             | YES       | YES        |
| R3            | 8k2           | 22k4      | omit            | YES       | 22k        |
| R4            | 470r          | 100k      | 1k              | 470r      | 100k       |
| R5            | 15k           | guess     | YES             | Jumper    | Jumper     |
| R6            | 220k          | Jumper    | Jumper          | Jumper    | YES        |
| R7            | 220k          | omit      | omit            | omit      | YES        |
| R8            | 22k           |           | 100r            | Jumper    | YES        |
| R9            | 1M            | guess     | omit            | omit      | YES        |
| SW1           | SPDT          | guess     | YES             | omit      | omit       |
| SW2           | SPDT          | choice    | YES             | choice    | on off on  |
| SW3           | 3PDT          | YES       | YES             | YES       | YES        |
| Tone1         | B10k          | Jumper    | Jumper          | YES       | Jumper     |
| Trim1         | LED           | YES       | YES             | YES       | YES        |
| Vol1          | B500k         | omit      | omit            | omit      | YES        |
| Vol2          | B100k         |           | choice          | YES       | short 2 &3 |

## PCB Render - Fully Populated

![image](https://user-images.githubusercontent.com/53580358/202931998-1b29e478-aa47-4bac-915d-d5d785dd77f6.png)


