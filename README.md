# Experiment--03-Half-Subtractor-and-Full-subtractor
## Implementation-of-Half-subtractor-and-Full-subtractor-circuit
## AIM:
To design a half subtractor and full subtractor circuit and verify its truth table in Quartus using Verilog programming.

## Equipments Required:
## Hardware – PCs, Cyclone II , USB flasher
## Software – Quartus prime
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
Connect the supply (+5V) to the circuit.

Switch ON the main switch.

If the output is 1 , then the LED Glows.




Write the detailed procedure here 


## Program:
/*
Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.
Developed by: P.Jeba Princy
RegisterNumber: 22008375
FOR HALF SUBTRACTOR 

module exphalfsub(A,B,Diff,Borrow);
input A,B;
output Diff,Borrow;
assign Diff=(A^B);
assign Borrow=(~A&B);
endmodule


FOR FULL SUBTRACTOR:

module fullsub(A,B,C,diff,borrow);
input A,B,C;
output diff,borrow;
assign borrow = (~A&(B^C)|(B&C));
assign diff
= (A^B^C);
endmodule
*/

## Output:

## Truthtable
Truth Table For Half Subtractor
!
[image](https://user-images.githubusercontent.com/122682918/213997746-4e7d53ee-b04e-4672-a1b8-3e61bd9f7546.png)
Truth Table For Full Subtractor![image](https://user-images.githubusercontent.com/122682918/213998270-a7bd1fb2-4a24-4e18-8e5a-58062fd9e0f4.png)








##  RTL realization
Half Subtractor
![Screenshot (5)](https://user-images.githubusercontent.com/122682918/213999242-b56f4a67-3236-48b1-8048-830a8f49b14
Full Subtractor



![Screenshot (6)](https://user-images.githubusercontent.com/122682918/213999442-d3b0aab7-86ac-4844-84dc-097a7376ef39.png)


## Timing diagram 
Timing Digram For Half Subtractor
![image](https://user-images.githubusercontent.com/122682918/213998617-eab8ca8a-e970-4fed-9085-dbf633c7f277.png)
Timing Digram For Full Subtractor
![image](https://user-images.githubusercontent.com/122682918/213999068-7ac0cc2a-01fc-458b-a106-1d40f8dfa9fd.png)


## Result:
Thus the half subtractor and full subtractor circuits are designed and the truth tables is verified using quartus software.
