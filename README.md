# FULL_ADDER_SUBTRACTOR
## Name: S Madhumitha
## Reg No: 212225040217

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

/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming. Developed by: RegisterNumber:212225040217
*/
~~~
/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming. Developed by: RegisterNumber:25004301 */ full adder module exp4add (a,b,c,x,y,z,sum,dif,car,bor); input a,b,c,x,y,z; output sum,dif,car,bor; assign sum = a^b^c; assign car = a&b | a&c | b&c; assign dif = x^y^z; assign bor = ~x&z | ~x&y | y&z; endmodule

full subractor module exp4sub(a, b, bin, diff, bout); input a, b, bin; // a, b, borrow-in output diff, bout; // difference, borrow-out

wire xor1, and1, and2;

assign xor1 = a ^ b; // First XOR stage assign diff = xor1 ^ bin; // Final difference (XOR with borrow-in)

assign and1 = ~a & b; // Borrow from a-b assign and2 = ~xor1 & bin; // Borrow from borrow-in assign bout = and1 | and2; // Final borrow-out (OR)

endmodule
~~~
**RTL Schematic**
## Full Adder
<img width="751" height="579" alt="Screenshot 2026-05-22 133415" src="https://github.com/user-attachments/assets/ef40d0ef-1a26-4f3f-86a7-09a5dc02c27d" />

## Half Adder
<img width="823" height="270" alt="Screenshot 2026-05-22 133427" src="https://github.com/user-attachments/assets/564e08e1-e70f-4dd7-988e-e3eb7f9b7d7d" />
 
 **Output Timing Waveform**
 <img width="1270" height="620" alt="Screenshot 2026-05-22 133442" src="https://github.com/user-attachments/assets/6177ca10-a4a3-4895-81b2-736584cc0a08" />

**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



