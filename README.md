![280580781-48c2cef2-e711-49bd-aa3b-1438aea930ad](https://github.com/Revathi-Dayalan/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/96000574/e9badbf3-9f97-4fab-a5f2-f407d63f93c1)# Experiment--03-Half-Subtractor-and-Full-subtractor
## Implementation-of-Half-subtractor-and-Full-subtractor-circuit
## AIM:
To design a half subtractor and full subtractor circuit and verify its truth table in Quartus using Verilog programming.

## Equipments Required:
 Hardware – PCs, Cyclone II , USB flasher
Software – Quartus prime
## Theory
Subtractor circuits take two binary numbers as input and subtract one binary number input from the other binary number input. Similar to adders, it gives out two outputs, difference and borrow (carry-in the case of Adder). There are two types of subtractors.

## Half Subtractor Full Subtractor
## Half Subtractor

The half-subtractor is a combinational circuit which is used to perform subtraction of two bits. It has two inputs, X (minuend) and Y (subtrahend) and two outputs D (difference) and B (borrow). To perform x - y, we have to check the relative magnitudes of x and y. If x ;;, y, we have three possibilities: 0 - 0 = 0, 1 - 0 = 1, and 1 - I = 0. The result is called the difference bit. If x < y, we have 0 - I, and it is necessary to borrow a 1 from the next higher stage. The I borrowed from the next higher stage adds 2 to the minuend bit, just as in the decimal system a borrow adds 10 to a minuend digit. With the minuend equal to 2, the difference becomes 2 - I = 1. The half-subtractor needs two outputs. One output generates the difference and will be designated by the symbol D. The second output, designated B for borrow, generates the binary signal that informs the next stage that a I has been borrowed.

![half-subtractor9](https://user-images.githubusercontent.com/36288975/166112538-58c3bc7c-ee5d-4e6a-ac8d-8e8328efe27a.png)


Sum = X'Y+XY' = X ⊕ Y
Carry=X'Y

## Full Subtractor
A full subtractor is a combinational circuit that performs subtraction involving three bits, namely minuend, subtrahend, and borrow-in . It accepts three inputs: minuend, subtrahend and a borrow bit and it produces two outputs: difference and borrow. 

![full-subtractor6](https://user-images.githubusercontent.com/36288975/166112541-24c68359-3de8-4674-ae22-8272ffc385ed.png)


Diff = A ⊕ B ⊕ Bin B = A'Bin + A'B + BBin

## Procedure

1.Use module projname(input,output) to start the Verilog programmming.

2.Assign inputs and outputs using the word input and output respectively.

3.Use defined keywords like wire,assign and required logic gates to represent the boolean expression.

4.Use each output to represent one for difference and the other for borrow.

5.End the verilog program using keyword endmodule.


## Program:
```
Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.
Developed by: REVATHI D
RegisterNumber:  212221240045
```

## HALF SUBTRACTOR:
```
module exp04(a,b,difference,borrow);
input a,b;
output difference,borrow;
wire x;
xor(difference,a,b);
not(x,a);
and(borrow,x,b);
endmodule
```

## FULL SUBTRACTOR:
```
module FullSub04(a,b,bin,difference,borrow);
input a,b,bin;
output difference,borrow;
wire p;
assign difference=((a^b)^bin);
not (p,a);
assign borrow=((p&b)|(p&bin)|(b&bin));
endmodule
```

## Output:
## Half Subtractor:

![280580781-48c2cef2-e711-49bd-aa3b-1438aea930ad](https://github.com/Revathi-Dayalan/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/96000574/1ee08f07-f4f8-4688-be83-0680614e8fd6)

## Full Subtractor:

![280580819-41640ea2-b4c7-4373-b004-1bc1f158ebe6](https://github.com/Revathi-Dayalan/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/96000574/7ce0a355-a5a0-43a7-b7eb-633861aa6f9c)


## Truthtable
## Half subtractor:

![280580838-1e2db12c-5864-4cc5-9071-ce0983cbf722](https://github.com/Revathi-Dayalan/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/96000574/e8bf6624-a87f-4374-bdf7-f48856eb085c)


## Full subtractor:


![280580876-32b0915e-a3bf-4af1-bd6c-0a954b754dd1](https://github.com/Revathi-Dayalan/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/96000574/4c617ddc-0b74-4929-817c-952cd7105ed0)


## output waveform:
## Half subtractor:

![280580946-a4052fca-6b36-456d-8c74-96df5549710b](https://github.com/Revathi-Dayalan/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/96000574/5f4b6d4d-92af-465c-852f-efd5e99c5c76)


## Full subtractor:

![280580973-f5097db4-fe77-4f44-a35f-335d6eb9bdcb](https://github.com/Revathi-Dayalan/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/96000574/4db28400-545f-4737-aacd-14dae19d4ec1)




## Result:
Thus the half subtractor and full subtractor circuits are designed and the truth tables is verified using quartus software.
