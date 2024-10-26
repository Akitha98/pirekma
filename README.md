A simple 15-tap low-pass FIR filter was chosen to be implemented, sampling at 1 Ms/s, with a passband frequency of 200 kHz and a stopband frequency of 355 kHz, yielding the following coefficients.-0.0265 
0 
0.0441 
0 
-0.0934 
0 
0.3139 
0.5000 
0.3139 
0 
-0.0934 
0 
0.0441 
0 
-0.026


This imlplementation was done in a Zybo Z7-20 FPGA board.
Its Zynq 7000 SoC was used.

***Procedure***
1. First the hardware design for the project was done with Xilinx Vivado, incooperaring Zynq SoC.
2. Then the synthesis, implementation, bitstream generation and hardware export were done.
3. From this hard ware file (.xsa file) the Xilinx Vitis project was created i.e. the firmware was created.
4. This firmware prgrammed the SoC.
5. Two firm ware were created first one for the simulation and the other for real time application.
6. The first firm ware (application project) named "new-system" focuses on simulation.
7. In here a precalculated sine wave form of two frequencies 200kHz and 500kHz was fed to the filter.
8. Then the filter generates the filter values and these values are displayed via a COM port.
9. For the generation of the wave form I used a Pythin script and it has been attached in the repository.
10. Then I copies the values from the COM port and these output values and the input values were then used in python to see the filter's functioning.
11. The other firm ware application named "continuous_operation" does the FIR functioning in real time.
 
