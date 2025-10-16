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

**Procedure**

Write the detailed procedure here

**Program:**

/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming. 
Developed by:V Yash Chhajer
RegisterNumber: 25012236
*/
Full Adder:
```
module fa(a,b,cin,sum,carry); 
input a,b,cin; 
output sum,carry; 
assign sum=( (a ^ b)^cin); 
assign carry= ( (a & b)| ( cin &(a ^ b ))); 
endmodule
```
Full Subtractor:
```
module fs(a,b,bin,difference,borrow); 
input a,b,bin; 
output difference,borrow; 
assign difference= ( (a ^ b)^bin); 
assign borrow= ( ( ~a & b)| ( bin & (~(a ^ b )))); 
endmodule
```
**RTL Schematic**
Full Adder:
<img width="1920" height="1020" alt="Logic Diagram" src="https://github.com/user-attachments/assets/05c52b8a-b81a-4b40-a17c-ed9f7591984b" />
Full Subtractor:
<img width="1920" height="1020" alt="Logic Diagram" src="https://github.com/user-attachments/assets/163db8b1-484f-4bfe-9926-3c5a95bdcdb5" />

**Output Timing Waveform**
Full Adder:
<img width="1920" height="1020" alt="Waveform" src="https://github.com/user-attachments/assets/7e6d1d72-f67a-4633-bd56-bf9082d7f559" />
Full Subtractor:
<img width="1920" height="1020" alt="Waveform" src="https://github.com/user-attachments/assets/23e603cf-47bc-48a1-a12b-1b949e730e83" />

**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



