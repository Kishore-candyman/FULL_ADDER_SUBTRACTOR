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

![Screenshot 2024-11-24 164706](https://github.com/user-attachments/assets/515e464d-2b44-4b1a-a8eb-67961cb2b70d)


FULL SUBTRACTOR

![Screenshot 2024-11-24 165029](https://github.com/user-attachments/assets/d9f2bb69-c371-4be6-9da9-19fd7c60ac6e)


**Procedure**

Write the detailed procedure here

1).Type the program in Quartus software.

2).Compile and run the program.

3).Generate the RTL schematic and save the logic diagram.

4).Create nodes for inputs and outputs to generate the timing diagram.

5).For different input combinations generate the timing diagram


**Program:**
```

FULL ADDER
module fulladder(sum, cout, a, b, cin); output sum;
output cout;
input a;
input b;
input cin;
wire w1,w2,w3;
assign w1=a^b;
assign w2=a&b;
assign w3=w1&cin;
assign sum=w1^cin;
assign cout=w2|w3;
endmodule

FULL SUBTRACTOR
module fullsub(df,bo,a,b,bin); 
output df;
output bo; 
input a; 
input b; 
input bin;
wire w1,w2,w3; 
assign w1=a^b; 
assign w2=(~a&b); 
assign w3=(~w1&bin); 
assign df=w1^bin; 
assign bo=w2|w3; 
endmodule

```
 Developed by: M. KISHORE
 RegisterNumber:24900763

**RTL Schematic**

FULL ADDER

![Screenshot 2024-11-24 161000](https://github.com/user-attachments/assets/a4ebd96e-232e-432b-98e5-e272b1999183)


FULL SUBTRACTOR

![Screenshot 2024-11-24 162447](https://github.com/user-attachments/assets/3c72c4ab-524c-4e5d-acc6-e8270d5e92f7)


**Output Timing Waveform**

FULL ADDER

![Screenshot (18)](https://github.com/user-attachments/assets/41402564-a33b-4d6b-9882-8d66765d4fec)


FULL SUBTRACTOR

![Screenshot (19)](https://github.com/user-attachments/assets/a0f08c01-492a-4cea-bb7a-8486c89009cd)


**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



