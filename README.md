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

![image](https://user-images.githubusercontent.com/53580358/202931998-1b29e478-aa47-4bac-915d-d5d785dd77f6.png)


