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
1.Use module projname(input,output) to start the Verilog programmming.

2.Assign inputs and outputs using the word input and output respectively.

3.Use defined keywords like wire,assign and required logic gates to represent the boolean expression.

4.Use each output to represnt onre for differnce and the other for borrow.

5.End the verilog program using keyword endmodule.


## Program:
```
Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.
Developed by: PRAVEENKUMAR S
RegisterNumber:212222230108
```

# HALF SUBTRACTOR:
```
/*
Program to design a half subtractor circuit and verify its truth table in quartus using Verilog programming.
Developed by: Praveen Kumar S
RegisterNumber:  212222230108
*/
module half_sub(x,y,d,b);
input x,y;
output d,b;
wire x1;
xor(d,a,b);
not(x1,x);
and(b,x1,y);
endmodule
```

# FULL SUBTRACTOR:
```
module full_sub(a,b,c,d,bo);
input a,b,c;
output d,bo;
wire w1,w2,w3,w4,w5;
xor(w1,b,c);
xor(d,w1,a);
not(w2,b);
and(w5,w2,c);
not(w3,w1);
and(w4,w2,a);
or(bo,w4,w5);
endmodule
```

## Output:
## RTL realization for Half Subtractor:
![de00](https://user-images.githubusercontent.com/119559827/234013854-eecc5bd2-91c7-4e0a-a5cf-dba0e33c5265.png)

## TRUTH TABLE:
![d01](https://user-images.githubusercontent.com/119559827/234014149-bef0e9ab-d2ed-4c93-bbe0-e9e7bb3dc47a.png)

## Timing diagram:
![d02](https://user-images.githubusercontent.com/119559827/234014404-66bdabe5-009b-4118-8bc1-d531737b6d4c.png)

## RTL realization for Full subtractor:
![d03](https://user-images.githubusercontent.com/119559827/234014803-8dc7f778-0171-41af-8ba5-f389fb0d0972.png)

## Truthtable:
![d05](https://user-images.githubusercontent.com/119559827/234015468-5f6b1288-c29b-4a22-ba37-89e1e0a8ccfd.png)

## Timing diagram:
![d06](https://user-images.githubusercontent.com/119559827/234015710-8e6bd51c-084f-48e0-97e3-7b2b980fd869.png)

## Result:
Thus the half subtractor and full subtractor circuits are designed and the truth tables is verified using quartus software.
