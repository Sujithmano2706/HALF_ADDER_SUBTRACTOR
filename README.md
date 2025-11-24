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
<img width="424" height="249" alt="adder" src="https://github.com/user-attachments/assets/4eed5e75-492b-49be-9884-9e7e1dba5fdf" />
<img width="436" height="248" alt="sub" src="https://github.com/user-attachments/assets/0ef26a03-c651-48fa-a68e-7486c20f20d8" />

**Procedure**

1.	Type the program in Quartus software.

2.	Compile and run the program.

3.	Generate the RTL schematic and save the logic diagram.

4.	Create nodes for inputs and outputs to generate the timing diagram.

5.	For different input combinations generate the timing diagram.


**Program:**
```
/* Program to design a half adder and full adder circuit and verify its truth table in quartus using Verilog programming.

Developed by:Sujith Mano M 
RegisterNumber: 25018328 */
```
```
module suji4(sum, carry, a, b);
  output sum;
  output carry;
  input a;
  input b;
  assign sum = a ^ b;
  assign carry = a & b;
endmodule
```
```
module suji5(diff, borrow, a, b);
  output diff;
  output borrow;
  input a;
  input b;
  assign diff = a ^ b;
  assign borrow = ~a & b;
endmodule
```
**RTL Schematic**
<img width="1700" height="812" alt="Screenshot 2025-11-23 151702" src="https://github.com/user-attachments/assets/06a2e8d3-e3b6-45c7-95b2-412d33187357" />
<img width="1667" height="725" alt="Screenshot 2025-11-23 152131" src="https://github.com/user-attachments/assets/d44b1565-21ff-47a1-b107-2bd1bf40c67e" />

**Output/TIMING Waveform**
<img width="1920" height="1080" alt="Screenshot 2025-11-24 111613" src="https://github.com/user-attachments/assets/9f785a38-daf4-4cd9-b7df-12d3d0351092" />
<img width="1920" height="1080" alt="Screenshot 2025-11-24 112811" src="https://github.com/user-attachments/assets/c7834a74-8be4-49f7-a2cd-7f4465805b3b" />

**Result:**
Thus the Half Adder and Half Subtractor are studied and the truth tables are verified
