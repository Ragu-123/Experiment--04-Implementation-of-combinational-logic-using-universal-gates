# Experiment--04-Implementation-of-combinational-logic-using-universal-gates
Implementation of combinational logic using universal-gates
 
## AIM:
To implement the given logic function using NAND and NOR gates and to verify its operation in Quartus using Verilog programming.

F=((C'.B.A)'(D'.C.A)'(C.B'.A)')' using NAND gate
F=(((C.B'.A)+(D.C'.A)+(C.B'.A))')' using NOR gate
## Equipments Required:
## Hardware – PCs, Cyclone II , USB flasher
## Software – Quartus prime


## Theory
Logic gates are electronic circuits which perform logical functions on one or more inputs to produce one output. 

## Using NAND gates
NAND gate is actually a combination of two logic gates i.e. AND gate followed by NOT gate. So its output is complement of the output of an AND gate.This gate can have minimum two inputs, output is always one. By using only NAND gates, we can realize all logic functions: AND, OR, NOT, X-OR, X-NOR, NOR. So this gate is also called as universal gate. First note that the entire expression is inverted and we have three terms ANDed. This means that we must use a 3-input NAND gate. Each of the three terms is, itself, a NAND expression. Finally, negated single terms can be generates with a 2-input NAND gate acting as an inverted.

F=((C'.B.A)'(D'.C.A)'(C.B'.A)')'

## Logic Diagram

Using NOR gates
NOR gate is actually a combination of two logic gates: OR gate followed by NOT gate. So its output is complement of the output of an OR gate. This gate can have minimum two inputs, output is always one. By using only NOR gates, we can realize all logic functions: AND, OR, NOT, Ex-OR, Ex-NOR, NAND. So this gate is also called universal gate. Designing a circuit with NOR gates only uses the same basic techniques as designing a circuit with NAND gates; that is, the application of deMorgan’s theorem. The only difference between NOR gate design and NAND gate design is that the former must eliminate product terms and the later must eliminate sum terms.

F=(((C.B'.A)+(D.C'.A)+(C.B'.A))')'

## Logic Diagram
## Procedure
## Program:

/*
Program to implement the given logic function using NAND and NOR gates and to verify its operations in quartus using Verilog programming.
Developed by:RAGUNATH R 
RegisterNumber:22008922
USING NAND OPERATION:
module combine(a,b,c,d,f);
input a,b,c,d;
output f;
wire p,q,r;
assign p=c&(~b)&(~a);
assign q=d&(~c)&(~a);
assign r=(~c)&b&(~a);
assign f=(~p&~q&~r);
endmodule

USING NOR OPERATION:
module combine2(a,b,c,d,f);
input a,b,c,d;
output f;
wire p,q,r,s;
assign p=c&(~b)&a; 
assign q=d&(~c)&a;
assign r=c&(~b)&a;
assign s=~(p|q|r);
assign f=~s;
endmodule;


*/
## RTL realization
NAND:
![image](https://user-images.githubusercontent.com/113915622/211316194-0c1a6a06-1331-496c-ae6e-6f63153a4f14.png)
NOR:
![image](https://user-images.githubusercontent.com/113915622/211316324-20f0c430-75aa-407d-8945-34d8284a0630.png)

## Output:
NAND:
![image](https://user-images.githubusercontent.com/113915622/211316616-59e344e3-1655-4cc5-a96e-9852248d8e3c.png)
NOR:
![image](https://user-images.githubusercontent.com/113915622/211316728-878321f4-f6cd-4015-ae02-30a77e512df1.png)


## Timing Diagram
NAND:
![image](https://user-images.githubusercontent.com/113915622/211316836-068c017c-0d56-401c-8df9-54fd136cda46.png)
NOR:
![image](https://user-images.githubusercontent.com/113915622/211316980-ddfc11b4-a356-416a-b9e4-1f0123c03440.png)

## Result:
Thus the given logic functions are implemented using NAND and NOR gates and their operations are verified using Verilog programming.
