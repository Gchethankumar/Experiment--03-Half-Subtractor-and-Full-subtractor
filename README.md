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

Connect the supply (+5) to the circuit
Switch ON the main switch
If the output is 1, then the led glows.


## Program:

Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.

Developed by: G.Chethan kumar

RegisterNumber: 22005596

Half subtractor:
```
module halfsub(output B,D, input X,Y);
assign D = (X ^ Y);
assign B = (~X & Y);
endmodule
```

Full subtractor:
```
module fullsub(X,Y,Z,Borrow,Difference);
input X,Y,Z;
output Borrow,Difference;
assign Difference = (X^Y^Z);
assign Borrow = (~X&(Y^Z)|(Y&Z));
endmodule
```

## Output:
## Half subtractor:

### RTL realization:

![Screenshot_20230105_100141](https://user-images.githubusercontent.com/118348224/210837673-2a4a35a0-24b5-40ef-a90b-3dab1897a1a2.png)

### Timing diagram:

![Screenshot_20230105_100428](https://user-images.githubusercontent.com/118348224/210839128-f0f9b185-566f-4e0a-a0f8-2fc3e5d38324.png)

### Truthtable:

![image](https://user-images.githubusercontent.com/118348224/210838655-9c1aab18-52ed-4aed-95a2-0d7bd76dec98.png)

## Full subtractor:

### RTL realization:

![Screenshot_20230105_101341](https://user-images.githubusercontent.com/118348224/210837877-2796d142-2c65-45d4-b6ce-8763d07ddcba.png)

### Timing diagram 

![Screenshot_20230105_101858](https://user-images.githubusercontent.com/118348224/210839349-71939a5a-2978-4fd4-ae2a-8efc61b632ed.png)

### Truthtable:

![image](https://user-images.githubusercontent.com/118348224/210838909-a86df8b1-969d-404a-842f-ea5df4870e22.png)


## Result:
Thus, the half subtractor and full subtractor circuits are designed and the truth tables is verified using quartus software.
