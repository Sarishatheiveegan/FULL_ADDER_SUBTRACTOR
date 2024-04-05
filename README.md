# FULL_ADDER_SUBTRACTOR

Implementation-of-Full-Adder-and-Full-subtractor-circuit

**AIM:**

To design a Full Adder and Full Subtractor circuit and verify its truth table in Quartus using Verilog programming.

**Equipments Required:**

Hardware – PCs, Cyclone II , USB flasher

Software – Quartus prime

**Full Adder and Full Subtractor**

**Full Adder**

Full adder is a digital circuit used to calculate the sum of three binary bits. It consists of three inputs and two outputs. Two of the input variables, denoted by A and B, represent the two significant bits to be added. The third input, Cin, represents the carry from the previous lower significant position. Two outputs are necessary because the arithmetic sum of three binary digits ranges in value from 0 to 3, and binary 2 or 3 needs two digits. The two outputs are sum and carry.

Sum =A’B’Cin + A’BCin’ + ABCin + AB’Cin’ = A ⊕ B ⊕ Cin 

Carry = AB + ACin + BCin

![image](https://github.com/naavaneetha/FULL_ADDER_SUBTRACTOR/assets/154305477/0f30ba51-5ffb-4198-845f-18e054f675e7)

**Figure -1 FULL ADDER**

**Full Subtractor**

A full subtractor is a combinational circuit that performs subtraction involving three bits, namely minuend, subtrahend, and borrow-in . It accepts three inputs: minuend, subtrahend and a borrow bit and it produces two outputs: difference and borrow.

![image](https://github.com/naavaneetha/FULL_ADDER_SUBTRACTOR/assets/154305477/02b24f51-ab51-4304-9ad6-7b81ffc1ead5)

Diff = A ⊕ B ⊕ Bin 

Borrow out = A'Bin + A'B + BBin

**Truthtable**
![Screenshot 2024-04-05 113104](https://github.com/Sarishatheiveegan/FULL_ADDER_SUBTRACTOR/assets/144979465/44c6f171-24e0-45e5-88ae-1737bfa4b64e)
![Screenshot 2024-04-05 113118](https://github.com/Sarishatheiveegan/FULL_ADDER_SUBTRACTOR/assets/144979465/aceb7ee0-8893-4b5c-983d-3ea3f12f6ac6)

**Procedure**

1.Type the program in Quartus software.

2.Compile and run the program. 

3.Generate the RTL schematic and save the logic diagram.

4.Create nodes for inputs and outputs to generate the timing diagram.

5.For different input combinations generate the timing diagram

**Program:**

/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.

Developed by:Marino Sarisha T

RegisterNumber:212223240084
**Full_Adder**
```
module fulladder(a,b,cin,sum,carry);
input a,b,cin;
output sum,carry;
wire w1,w2,w3,w4;       
xor(w1,a,b);
xor(sum,w1,cin);        
and(w2,a,b);
and(w3,b,cin);
and(w4,cin,a);
or(carry,w2,w3,w4);
endmodule
```
**Full_subracter**
```
module fullsub(a,b,Bin,BO,DIFF);
input a,b,Bin;
output BO,DIFF;
assign DIFF = a ^ b ^ Bin;
  assign BO = (a & b) | ((a ^ b) & Bin);
endmodule
```
**RTL Schematic**
![Screenshot 2024-04-05 112504](https://github.com/Sarishatheiveegan/FULL_ADDER_SUBTRACTOR/assets/144979465/df3c3f91-46f4-43ec-8969-2666b937779e)

**Output Timing Waveform**
![Screenshot 2024-04-05 112640](https://github.com/Sarishatheiveegan/FULL_ADDER_SUBTRACTOR/assets/144979465/dfb691e0-8c3f-4382-86ec-83469c7159d6)
![Screenshot 2024-04-05 112613](https://github.com/Sarishatheiveegan/FULL_ADDER_SUBTRACTOR/assets/144979465/58475691-5db0-4f1c-b599-36ded3f26a28)

**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



