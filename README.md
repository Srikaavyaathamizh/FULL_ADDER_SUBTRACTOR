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

Developed by: SRIKAAVYAA T
RegisterNumber: 212223230214
*/

## FULL_adder

```
module fulladd_top(a,b,cin,sum,carry);
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
## Full_Subractor

```
module fullsub_top(a,b,Bin,BO,DIFF);
input a,b,Bin;
output BO,DIFF;
assign DIFF = a ^ b ^ Bin;
assign BO = (a & b) | ((a ^ b) & Bin);
endmodule
```

## TruthTable

## FULL ADDER

![Screenshot 2024-10-17 230058](https://github.com/user-attachments/assets/514e3295-9cc1-4d07-b463-7b081f97aec6)

## FULL SUBTRACTOR

![Screenshot 2024-10-17 230207](https://github.com/user-attachments/assets/22390aad-b913-48d3-bedb-dad37e6d2f22)

## RTL Schematic

## FULL ADDER:
![Screenshot 2024-10-17 230317](https://github.com/user-attachments/assets/d53bd736-6d9d-4eec-a201-e291bcbb3b2d)

## FULL SUBTRACTOR:

![Screenshot 2024-10-17 230322](https://github.com/user-attachments/assets/236a0252-cd70-4652-8155-d05ef441e060)

**Output Timing Waveform**
## FULL ADDER

![Screenshot 2024-10-17 230429](https://github.com/user-attachments/assets/2eda1962-694c-475b-8e74-7b7c59dae004)

## FULL SUBTRACTOR

![Screenshot 2024-10-17 230443](https://github.com/user-attachments/assets/ddb83afe-629c-4ba8-ba97-8ba7a4d5b2ed)

**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



