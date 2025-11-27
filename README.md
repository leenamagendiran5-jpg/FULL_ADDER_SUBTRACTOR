# FULL_ADDER_SUBTRACTOR

Implementation-of-Full-Adder-and-Full-subtractor-circuit

**AIM:**

To design a Full Adder and Full Subtractor circuit and verify its truth table in Quartus using Verilog programming.

**Equipments Required:**

Hardware – PCs, Cyclone II , USB flasher

Software – Quartus prime

**Full Adder and Full Subtractor**

**FULL ADDER**

Full adder is a digital circuit used to calculate the sum of three binary bits. It consists of three inputs and two outputs. Two of the input variables, denoted by A and B, represent the two significant bits to be added. The third input, Cin, represents the carry from the previous lower significant position. Two outputs are necessary because the arithmetic sum of three binary digits ranges in value from 0 to 3, and binary 2 or 3 needs two digits. The two outputs are sum and carry.

Sum =A’B’Cin + A’BCin’ + ABCin + AB’Cin’ = A ⊕ B ⊕ Cin 

Carry = AB + ACin + BCin

![image](https://github.com/naavaneetha/FULL_ADDER_SUBTRACTOR/assets/154305477/0f30ba51-5ffb-4198-845f-18e054f675e7)

**Figure -1 FULL ADDER**

**FULL SUBTRACTOR**           

A full subtractor is a combinational circuit that performs subtraction involving three bits, namely minuend, subtrahend, and borrow-in . It accepts three inputs: minuend, subtrahend and a borrow bit and it produces two outputs: difference and borrow.

![image](https://github.com/naavaneetha/FULL_ADDER_SUBTRACTOR/assets/154305477/02b24f51-ab51-4304-9ad6-7b81ffc1ead5)

Diff = A ⊕ B ⊕ Bin 

Borrow out = A'Bin + A'B + BBin

**Truthtable**

FULL ADDER

<img width="691" height="571" alt="Screenshot 2025-11-27 151431" src="https://github.com/user-attachments/assets/e3b68d15-4ba0-4d54-9051-cb659a010335" />

FULL SUBTRACTOR

<img width="662" height="445" alt="Screenshot 2025-11-27 151454" src="https://github.com/user-attachments/assets/eb972158-656c-498e-9971-3d05c9a9aa62" />

**Procedure**

1. Type the program in Quartus software.

2. Compile and run the program.

3. Generate the RTL schematic and save the logic diagram.

4. Create nodes for inputs and outputs to generate the timing diagram.

5. For different input combinations generate the timing diagram.

**Program:**
Developed by : M.LEENA SHREE RegisterNumber: 25018414

i) FULL ADDER

```
module fa(a,b,cin,sum,carry);
input a,b,cin;
output sum,carry;
assign sum=( (a ^ b)^cin);
assign carry= ( (a & b)| ( cin &(a ^ b )));
endmodule

```
ii) FULL SUBTRACTOR

```
module fs(a,b,bin,difference,borrow);
input a,b,bin;
output difference,borrow;
assign difference= ( (a ^ b)^bin);
assign borrow= ( ( a & b)| ( bin & ((a ^ b ))));
endmodule

```
**RTL Schematic**

FULL ADDER

<img width="1108" height="568" alt="Screenshot 2025-11-27 151837" src="https://github.com/user-attachments/assets/4778b876-a80a-4ef2-bf77-0116992c062c" />

FULL SUBTRACTOR

<img width="1119" height="576" alt="Screenshot 2025-11-27 151857" src="https://github.com/user-attachments/assets/d43185a0-cced-41d0-8a74-b185d00604ff" />


**Output Timing Waveform**

FULL ADDER

<img width="1109" height="571" alt="Screenshot 2025-11-27 151652" src="https://github.com/user-attachments/assets/433e7f01-01bc-42af-9253-5e0c489adaa7" />

FULL SUBTRACTOR

<img width="1106" height="570" alt="Screenshot 2025-11-27 151713" src="https://github.com/user-attachments/assets/182d9f89-5145-432d-a0f9-c64c8229c0b3" />

**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



