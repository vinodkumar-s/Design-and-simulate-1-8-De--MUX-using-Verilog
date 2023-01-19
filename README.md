# Design and simulate 1:8 De- MUX using Verilog.
### AIM: 1X8 de multiplexer using verilog and validate its outputs

### HARDWARE REQUIRED:  – PC, Cyclone II , USB flasher

### SOFTWARE REQUIRED:   Quartus prime

### THEORY 

## What is Demultiplexer?
The demultiplexer is a combinational logic circuit designed to switch one common input line to one of several seperate output line

The data distributor, known more commonly as the demultiplexer or “Demux” for short, is the exact opposite of the Multiplexer we saw in the previous tutorial.

The demultiplexer takes one single input data line and then switches it to any one of a number of individual output lines one at a time. The demultiplexer converts a serial data signal at the input to a parallel data at its output lines as shown below.

### 1 to 8 Demultiplexer
The 1-8 demultiplexer block diagram is shown below which includes one input ‘D’, 3-select inputs like S0, S1 & S2 & 8 outputs like X0, X1, X2¸ X3, X4¸ X5¸ X6 & X7. This type of Demux is also called 3-8 Demux because of the 3 select input lines & 8 output lines.

### BLOCK DIAGRAM:


![output](/Block-diagram-of-18-demultiplexer.jpg)

It transmits one input line toward one of the eight output lines based on the select inputs combinations like input ‘D’ is connected to one of the outputs from X0 to X7 depending on the S0, S1 & S2 select lines.

### LOGIC DIAGRAM:

![output](/de-multiplexer9.png)


 
### Procedure
#### step1: Start the module using module projname().
#### step2: Declare the inputs and outputs along with the select lines according to the demultiplexer.
#### step3: Use wire to assign intermediate outputs.
#### step4: Use and and not gates to get the desired output.
#### step5: End the module.
#### step6: Generate RTL realization and timing diagrams.

### PROGRAM 

#### Developed by: s.vinod kumar
#### RegisterNumber: 22004903
```
DEMULTIPLEXER:

module demux(Y0,Y1,Y2,Y3,Y4,Y5,Y6,Y7,S0,S1,S2,S3,I);
input S0,S1,S2,S3,I;
output Y0,Y1,Y2,Y3,Y4,Y5,Y6,Y7;
wire S0C,S1C,S2C,S3C;
not(S0C,S0);
not(S1C,S1);
not(S2C,S2);
not(S3C,S3);
and(Y0,I,S0C,S1C,S2C,S3C);
and(Y1,I,S0C,S1C,S2C,S3);
and(Y2,I,S0C,S1C,S2,S3C);
and(Y3,I,S0C,S1C,S2,S3);
and(Y4,I,S0C,S1,S2C,S3C);
and(Y5,I,S0C,S1,S2C,S3);
and(Y6,I,S0C,S1,S2,S3C);
and(Y7,I,S0C,S1,S2,S3);
endmodule

```
### RTL LOGIC  
DEMULTIPLEXER:

![output](/RTL.png)

### TIMING DIGRAMS  
DEMULTIPLEXER:

![output](/timing%20diagram.png)

### TRUTH TABLE 
DEMULTIPLEXER:

![output](/de-multiplexer8%20truht%20table.png)

### RESULTS 

Hence 1x8 Demultiplexer is been implemented and verified using verilog programming and its output are validated.


