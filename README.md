# HALF_ADDER_SUBTRACTOR

Implementation-of-Half-Adder-and-Half Subtractor-circuit

**AIM:**

To design a half adder and half subtractor circuit and verify its truth table in Quartus using Verilog programming.

**Equipments Required:**

Hardware – PCs, Cyclone II , USB flasher 

Software – Quartus prime Theory Adders are digital circuits that carry out the addition of numbers.

**Half Adder**

Half adder is a combinational circuit that performs simple addition of two binary numbers. The input variables designate the augend and addend bits; the output variables produce the sum and carry. It is necessary to specify two output variables because the result may consist of two binary digits.

Sum = A’B+AB’ =A ⊕ B Carry = AB

![image](https://github.com/naavaneetha/HALF_ADDER_SUBTRACTOR/assets/154305477/bd4a0b2c-cdbc-4184-ab08-81578f121e1f)

Figure -01 HALF ADDER

**Half Subtractor**

The half-subtractor is a combinational circuit which is used to perform subtraction of two bits. It has two inputs, X (minuend) and Y (subtrahend) and two outputs D (difference) and B (borrow). To perform x - y, we have to check the relative magnitudes of x and y. If x ;;, y, we have three possibilities: 0 - 0 = 0, 1 - 0 = 1, and 1 - I = 0. The result is called the difference bit. If x < y, we have 0 - I, and it is necessary to borrow a 1 from the next higher stage. The I borrowed from the next higher stage adds 2 to the minuend bit, just as in the decimal system a borrow adds 10 to a minuend digit. With the minuend equal to 2, the difference becomes 2 - I = 1. The half-subtractor needs two outputs. One output generates the difference and will be designated by the symbol D. The second output, designated B for borrow, generates the binary signal that informs the next stage that a I has been borrowed. 

Diff = A’B+AB’ =A ⊕ B
Borrow = A’B

 ![image](https://github.com/naavaneetha/HALF_ADDER_SUBTRACTOR/assets/154305477/d76b099c-513f-4e7c-843a-e2fd028a531a)

Figure -02 HALF Subtractor

**Truthtable**

![WhatsApp Image 2024-10-01 at 11 30 58_a4072e75](https://github.com/user-attachments/assets/62787516-4753-42ce-8169-2d48df5b4e7d)


**Procedure**

1.	Type the program in Quartus software.

2.	Compile and run the program.

3.	Generate the RTL schematic and save the logic diagram.

4.	Create nodes for inputs and outputs to generate the timing diagram.

5.	For different input combinations generate the timing diagram.


**Program:**

Half_adder

module halfadd_top(a,b,sum,carry);

input a,b;

output sum,carry;

 assign sum = a^b;
 
 assign carry = a & b;
 
endmodule

Half_subtractor

module halfsub_top(a,b,D,Bo);

input a,b;

output D,Bo; // Outputs sum and carry for half adder:Outputs difference D,Borrow Bo for half subtractor

assign D = a ^ b;

  assign Bo = ~a & b;
  
endmodule


Developed by: **KARTHICK R**

RegisterNumber:**24900278**

**RTL Schematic**

![WhatsApp Image 2024-10-01 at 11 27 34_83a5c844](https://github.com/user-attachments/assets/d9a222d6-f722-43e4-af05-8c2212fa331a)


**Output/TIMING Waveform**

![WhatsApp Image 2024-10-01 at 11 32 00_3615c3f7](https://github.com/user-attachments/assets/33afad18-cf39-493f-ae5a-09376c51d7e0)

![WhatsApp Image 2024-10-01 at 11 32 11_d1d4347e](https://github.com/user-attachments/assets/74ab1dde-1578-4eb2-8530-25bb215373f3)

**Result:** 
  Thus the half adder and half subtractor circuit verify  successfully  using Verilog programming

