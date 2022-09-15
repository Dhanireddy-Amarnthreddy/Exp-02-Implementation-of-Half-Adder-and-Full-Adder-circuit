# Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit

# Implementation-of-Half-Adder-and-Full-Adder-circuit
### AIM:
To design a half adder and full adder circuit and verify its truth table in Quartus using Verilog programming.

### Equipments Required:
Hardware – PCs, Cyclone II , USB flasher
Software – Quartus prime
Theory
Adders are digital circuits that carry out addition of numbers.

### Half Adder
Half adder is a combinational circuit that performs simple addition of two binary numbers. The input variables designate the augend and addend bits; the output variables produce the sum and carry. It is necessary to specify two output variables because the result may consist of two binary digits.

Sum = A’B+AB’ =A ⊕ B Carry = AB

### Full Adder
Full adder is a digital circuit used to calculate the sum of three binary bits. It consists of three inputs and two outputs. Two of the input variables, denoted by A and B, represent the two significant bits to be added. The third input, Cin, represents the carry from the previous lower significant position. Two outputs are necessary because the arithmetic sum of three binary digits ranges in value from 0 to 3, and binary 2 or 3 needs two digits. The two outputs are sum and carry.

Sum =A’B’Cin + A’BCin’ + ABCin + AB’Cin’ = A ⊕ B ⊕ Cin Carry = AB + ACin + BCin

 ![image](https://user-images.githubusercontent.com/36288975/163552156-a13e5a56-c638-4110-97d9-8896907c8d25.png)

#### Figure -01 HALF ADDER 


![image](https://user-images.githubusercontent.com/36288975/163552057-b3547877-6d07-45b4-b7e0-bcfebfad9e1d.png)

#### Figure -02 FULL ADDER 

### Procedure

Connect the supply (+5V) to the circuit
Switch ON the main switch
If the output is 1, then the led glows.
### 
### Program:
/*
Program to design a half adder and full adder circuit and verify its truth table in quartus using Verilog programming.
### Developed by: D.Amarnath
### RegisterNumber:  212221240012
*/
### HALF ADDER
```
module exp3(a,b,sum,carry);
input a,b;
output sum,carry;
xor(sum,a,b);
and(carry,a,b);
endmodule 
```
### FULL ADDER
```
module exp3(a,b,c,sum,carry);
input a,b,c;
output sum,carry;
assign sum = ((a^b)^c);
assign carry = ((a&b)|(b&c)|(c&a));
endmodule
```
### Logic symbol & Truthtable RTL realization

### Output:
### RTL
![rtl](https://user-images.githubusercontent.com/94165103/190319308-2e5c54cd-aee3-42fd-9c35-9d55125f21f6.jpg)

### TIMING DIAGRAM

![timming](https://user-images.githubusercontent.com/94165103/190319363-baccf828-d9c5-4fc4-ac43-a06c7d2834dc.jpg)

### TRUTH TABLE

![truth table](https://user-images.githubusercontent.com/94165103/190319410-b4c7b69c-f51a-4fb2-a2f5-4fa3775a3675.jpg)
### RTL
![rtl2](https://user-images.githubusercontent.com/94165103/190319470-5268d8c7-9d4d-455a-99a5-7d5f44257eda.jpg)
### TIMING DIAGRAM

![timming2](https://user-images.githubusercontent.com/94165103/190319534-5d29926b-caed-42e4-b9d2-aecbc65d273f.jpg)
### TRUTH TABLE

![truth 2](https://user-images.githubusercontent.com/94165103/190319647-41c1445a-b9d3-416f-a9d5-413948066e3c.jpg)

### Result:

Thus, a half adder and full adder circuit is designed to verify its truth table in Quartus using Verilog programming.


