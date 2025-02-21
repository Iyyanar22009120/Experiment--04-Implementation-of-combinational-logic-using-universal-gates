# Experiment--02-Implementation-of-combinational-logic-using-universal-gates
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
```
Program to implement the given logic function using NAND and NOR gates and to verify its operations in quartus using Verilog programming.
Developed by: S.IYYANAR
RegisterNumber:  212222240036
```
```
module toexpoto(a,b,c,d,f1);
input a,b,c,d;
output f1;
assign f1=(~b&~d)|(~a&b&d)|(a&b&~c);
endmodule
```
```
module toexpo(w,x,y,z,f2);
input w,x,y,z;
output f2;
assign f2=(x&y)|(w&y)|(~y&z);
endmodule
```
## RTL realization

## Output:
## RTL
![f1 viewer](https://user-images.githubusercontent.com/118680259/232877229-87a92fc0-db13-4ff3-b803-1d38f012083d.png)
![f 2 viewer](https://user-images.githubusercontent.com/118680259/232877105-15984cd9-2446-4e4e-b4ae-a881b91649d6.png)

## Timing Diagram
![f1](https://user-images.githubusercontent.com/118680259/232874835-8f044e00-89d2-4af7-9cbe-2f67efa8fd95.png)
![f2](https://user-images.githubusercontent.com/118680259/232875035-56c05fd9-1b26-4821-9995-55b89a296e81.png)
## Result:
Thus the given logic functions are implemented using NAND and NOR gates and their operations are verified using Verilog programming.
