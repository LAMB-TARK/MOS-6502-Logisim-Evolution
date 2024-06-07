# MOS-6502-Logisim-Evolution

<img align="right" src="[https://picsum.photos/100/100](https://github.com/LAMB-TARK/MOS-6502-Logisim-Evolution/assets/152881313/cf76c921-c6a3-4ee0-a79a-d778ddf6ceae)">
![image](https://github.com/LAMB-TARK/MOS-6502-Logisim-Evolution/assets/152881313/cf76c921-c6a3-4ee0-a79a-d778ddf6ceae)


![image](https://github.com/LAMB-TARK/MOS-6502-Logisim-Evolution/assets/152881313/30777a2d-d3a5-49cf-b147-b985a71c33eb)

This repository contains a fully-functional open source rebuild of the classic 6502 microprocessor, in the open source graphical digital logic program LogiSim Evolution.   It is able to run original 6502 programs including samples from the classic 1980s Usbourne Machine Code for Beginners. The rebuild includes all instructions in their specified and documented form (i.e. fixing the ROR bugs as in later produced 6502s). Your 6502 programs can be run live using LogiSim's digital logic simulator, or LogiSim can export the design to Verilog and transferred to FPGA, or to ASIC using a multi project wafer fab service such as TinyTapeout.


# Design 

This project consists of multiple components, which can be viewed as sub-circuits within the 6502_Emulation.circ file or accessed individually as .circ files in the components folder of this repository. If you're interested in the design details of these components and how this project is able to emulate the 6502 instruction set, I recommend reading Implementation Chapter. 10. of the Emulating_6502.pdf document, submitted as part of my final year dissertation project.

This chapter first outlines the design and development of smaller components like the clock and program counter.

![image](https://github.com/LAMB-TARK/MOS-6502-Logisim-Evolution/assets/152881313/2cc31422-989f-4480-9804-ac49a98d843d)

Then progressing through the fetch, decode, execute cycle starting with the implementation of a decoder capable of activating pins to trigger the appropriate instruction and addressing mode based on a 8-bit input

![image](https://github.com/LAMB-TARK/MOS-6502-Logisim-Evolution/assets/152881313/75d48cb8-f29e-46e0-9a97-3143d06062bb)

During the decode step this project must retreive a value indicated by the current addressing mode used during execution using the Retreive Component. This Implementation Chapter. 10. describes the design proccess of this component and the the terchinques required to debug and synchronize these components.

![image](https://github.com/LAMB-TARK/MOS-6502-Logisim-Evolution/assets/152881313/4236128e-c33d-4e18-9ed2-7058c8ca20fd)

Finally this chapter discusses the design of the execute component capable of executing any of the instructions in the 6502 instruction set 

![image](https://github.com/LAMB-TARK/MOS-6502-Logisim-Evolution/assets/152881313/ad2937f2-20c4-48f6-bfc9-e63557b727b0)



# Example Execution

an example of this project executing an 8-bit bubble sort can be seen here: https://youtu.be/1x1AG9O5sLY 

# To Run
1) either download logisim evolution from: https://github.com/logisim-evolution/logisim-evolution or run Logisim_Evolution.jar
2) within Logisim open 6502_Emulation.circ
3) select the RAM comonent then in the properties window at the bottom left select contents: (click to edit)
4) In the Hex Editor window select the open button in the bottom left, then select any program you whish to run an example Bubble Sort is provided.
5) In the Main window select simulate in the top left enable ticks or press CTRL T to manual cause a clock tick.

# Learning 6502

If you're interested in learning to write 6502 machine code, I recommend starting with the Requirements and Analysis chapter for an understanding of how 6502 instructions are processed. Next, visit http://www.6502.org/users/obelisk/6502/instructions.html for overview of all possible 6502 instructions. Finally, for example programs written in 6502 assembly, check out the tutorials at http://www.6502.org/source/.

# Project Status and Contributions

This project is still being actively tested and developed however no other major features are expected to be added. Due to this I encourage and would appricate any feedback via Github. If you want to contact me futher please use the following email 25717330@students.lincoln.ac.uk

# Acknowledgments

This project would not have been possible without help and feedback from Prof. Charles Fox and Kristraps Jurkans.
