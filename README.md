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



Write the detailed procedure here 


## Program:
/*
Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.
Developed by: JEECIKASRINA M
RegisterNumber: 23013947 


## CODE:

### PROGRAM FOR HALF SUBTRACTOR:
```
module halfsub(a,b,difference,borrow);
input a,b;
output difference,borrow;
assign difference = (a^b);
assign borrow = (~a&b);
endmodule
```
### PROGRAM FOR FULL SUBTRACTOR:
```
module fullsub(a,b,difference,borrow);
input a,b;
output difference,borrow;
assign difference = (a^b);
assign borrow = (~a&b);
endmodule
```

## truth table:

HALF SUBTRACTOR:

![image](https://github.com/Jeecikasrina23013947/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/148515300/a2cf1add-90a0-4e0a-9006-aa816f8352cf)

FULL ADDER SUBTRACTOR:

![image](https://github.com/Jeecikasrina23013947/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/148515300/9e09473e-3546-4b6e-9e6e-36047dc92800)

## RTL VIEW:

HALF ADDER RTL VIEW:

![image](https://github.com/Jeecikasrina23013947/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/148515300/3481650a-fef3-4b7e-ad80-0c03e28fcb89)

FULL ADDER SUBTRACTOR:

![image](https://github.com/Jeecikasrina23013947/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/148515300/18da9a14-bb38-45e9-82e6-c7829736d585)

## TIMING DIAGRAM:

HALF ADDER:

![image](https://github.com/Jeecikasrina23013947/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/148515300/4193f2d9-41ed-4d8e-8bd5-6fec33327525)

FULL ADDER :

![image](https://github.com/Jeecikasrina23013947/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/148515300/0be57a44-5c97-4103-98a6-59cbc7095b9d)


## Result:
Thus the half subtractor and full subtractor circuits are designed and the truth tables is verified using quartus software.
