# Experiment--02-Implementation-of-combinational-logic
Implementation of combinational logic gates
 
## AIM:
To implement the given logic function verify its operation in Quartus using Verilog programming.
 F1= A’B’C’D’+AC’D’+B’CD’+A’BCD+BC’D
F2=xy’z+x’y’z+w’xy+wx’y+wxy
 
 
 
## Equipments Required:
## Hardware – PCs, Cyclone II , USB flasher
## Software – Quartus prime


## Theory
Logic gates are electronic circuits which perform logical functions on one or more inputs to produce one output.

## Using NAND gates:
NAND gate is actually a combination of two logic gates i.e. AND gate followed by NOT gate. So its output is complement of the output of an AND gate.This gate can have minimum two inputs, output is always one. By using only NAND gates, we can realize all logic functions: AND, OR, NOT, X-OR, X-NOR, NOR. So this gate is also called as universal gate. First note that the entire expression is inverted and we have three terms ANDed. This means that we must use a 3-input NAND gate. Each of the three terms is, itself, a NAND expression. Finally, negated single terms can be generates with a 2-input NAND gate acting as an inverted.

F=((C'.B.A)'(D'.C.A)'(C.B'.A)')'

## Using NOR Gates:
Using NOR gates NOR gate is actually a combination of two logic gates: OR gate followed by NOT gate. So its output is complement of the output of an OR gate. This gate can have minimum two inputs, output is always one. By using only NOR gates, we can realize all logic functions: AND, OR, NOT, Ex-OR, Ex-NOR, NAND. So this gate is also called universal gate. Designing a circuit with NOR gates only uses the same basic techniques as designing a circuit with NAND gates; that is, the application of deMorgan’s theorem. The only difference between NOR gate design and NAND gate design is that the former must eliminate product terms and the later must eliminate sum terms.

F=(((C.B'.A)+(D.C'.A)+(C.B'.A))')'

## Logic Diagram
## Procedure
1.Create a project with required entities.

2.Create a module along with respective file name.

3.Run the respective programs for the given boolean equations.

4.Run the module and get the respective RTL outputs.

5.Create university program(VWF) for getting timing diagram.

6.Give the respective inputs for timing diagram and obtain the results.

Program:

## Program:
```
/*
Program to implement the given logic function and to verify its operations in quartus using Verilog programming.
Developed by: MOHAMMED IMTHIYAS.M
RegisterNumber:  212222230083

F1:
module ff(a,b,c,d,f1);

input a,b,c,d;

output f1;

assign f1 = (~b&~d) | (~a&b&d) | (a&b&~c);

endmodule


F2:

module de (w,x,y,z,f2);

input w,x,y,z;

output f2;

assign f2 = (x&y)|(w&y)|(~y&z);

endmodule 
*/
```
## Output:
## RTL:
## F1:


![F1](https://github.com/imthiyas19/Experiment--02-Implementation-of-combinational-logic-/assets/120353416/abb37a58-8da7-4bf5-9262-20de33f598f1)

## F2:

![F2](https://github.com/imthiyas19/Experiment--02-Implementation-of-combinational-logic-/assets/120353416/77644f20-5463-4b05-a557-876d84373dda)




## Timing Diagram
## F1 


![TMI 1](https://github.com/imthiyas19/Experiment--02-Implementation-of-combinational-logic-/assets/120353416/d2d4b639-895c-4057-bd41-561e758e1648)

## F2



![TMI 2](https://github.com/imthiyas19/Experiment--02-Implementation-of-combinational-logic-/assets/120353416/e0819a2f-aa6b-4427-8a0d-35d5ff22cdb4)


## TRUTH TABLE:

![TB1](https://github.com/imthiyas19/Experiment--02-Implementation-of-combinational-logic-/assets/120353416/9de72628-eaf6-432a-9706-ce17a5d52930)

## Result:
Thus the given logic functions are implemented using  and their operations are verified using Verilog programming.
