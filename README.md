# Exp 03 Implementation of Half Adder and Full Adder circuit:
### AIM:
To design a half adder and full adder circuit and verify its truth table in Quartus using Verilog programming.

### Equipments Required:
Hardware – PCs, Cyclone II , USB flasher
Software – Quartus prime


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

1. Connect the supply (+5V) to the circuit
2. Switch ON the main switch
3. If the output is 1, then the led glows.
### Program:
```
Developed by: Harini.M
RegisterNumber: 212222240035
```
### Half Adder:
```
module Experiment03(A,B,S,C);
input A,B;
output S,C;
assign S=A^B;
assign C=A&B;
endmodule
```
### Full Adder:
```
module EX03(a,b,c,sum,carry);
input a,b,c;
output sum,carry;
assign sum=a^b^c;
assign carry=((a&b)|(b&c)|(c&a));
endmodule
```

### RTL
![image](https://github.com/Harinimuthu17/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/130278614/92e9b33b-3de7-4268-997e-9107866bb03c)
### Half Adder:
![image](https://github.com/Harinimuthu17/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/130278614/85c318f8-cdcf-4933-96e4-778a0e19059d)

### Full Adder::
![image](https://github.com/Harinimuthu17/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/130278614/e7245c1f-d244-4b36-a8b7-5ad4908fe2ed)

### TRUTH TABLE:
### Half Adder:
![image](https://github.com/Harinimuthu17/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/130278614/4fa83e7d-0c2b-44ee-a8da-d3dc8f03e56c)
### Full Adder:
![image](https://github.com/Harinimuthu17/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/130278614/ee5a79d7-0d95-44a2-908c-cc03f5a96cd3)

### OUTPUT WAVEFORM:
### Half Adder:
![image](https://github.com/Harinimuthu17/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/130278614/11948860-8969-4cc6-ad23-533be44e4daf)
### Full Adder:
![image](https://github.com/Harinimuthu17/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/130278614/915280a1-0628-4264-a874-a351a56ee598)

### Result:
Thus the given logic functions are implemented using and their operations are verified using Verilog programming.
