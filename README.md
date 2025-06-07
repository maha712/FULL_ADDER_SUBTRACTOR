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
FULL ADDER

![389268000-515e464d-2b44-4b1a-a8eb-67961cb2b70d](https://github.com/user-attachments/assets/7ef6f0f9-604a-4036-8285-541ecf6d8aa1)

FULL SUBTRACTOR

![389268010-d9f2bb69-c371-4be6-9da9-19fd7c60ac6e](https://github.com/user-attachments/assets/8f3ac60e-7557-4df0-adc3-d2313bade212)

Procedure

Write the detailed procedure here

1).Type the program in Quartus software.

2).Compile and run the program.

3).Generate the RTL schematic and save the logic diagram.

4).Create nodes for inputs and outputs to generate the timing diagram.

5).For different input combinations generate the timing diagram

**Program:**

```

i)FULL ADDER

module fulladder(a,b,cin,sum,carry);
input a,b,cin;
output sum,carry;
assign sum=( (a ^ b)^cin);
assign carry= ( (a & b)| ( cin &(a ^ b )));
endmodule

ii)FULL SUBTRACTOR

module fullsubtractor(a,b,bin,difference,borrow);
input a,b,bin;![391884214-515eaa7b-11ed-4243-9cbf-20bf5ae296e0](https://github.com/user-attachments/assets/e617daaa-fb32-4222-afd0-a0a212230629)

output difference,borrow;
assign difference= ( (a ^ b)^bin);
assign borrow= ( ( ~a & b)| ( bin & (~(a ^ b ))));
endmodule


```
RTL Schematic

FULL ADDER

![391884026-5dc82452-1baa-4caa-880f-03b173e70865](https://github.com/user-attachments/assets/5e34c0f2-7d8a-4523-88db-a1d23cc7b1c8)

FULL SUBTRACTOR

![391884105-3a9b8ee0-0370-45ee-bba7-9616c4554746](https://github.com/user-attachments/assets/cb88f774-6104-41dd-9df9-0f037adc1355)

Output Timing Waveform

FULL ADDER

![391884214-515eaa7b-11ed-4243-9cbf-20bf5ae296e0](https://github.com/user-attachments/assets/62decf7e-5485-42df-aa2f-1dcae732e374)

FULL SUBTRACTOR

![391884279-da805de2-28f1-4641-aefe-cff2d51ac340](https://github.com/user-attachments/assets/0d841c16-7b39-4591-b29f-ecf043aac1d8)

**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



