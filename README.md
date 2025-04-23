# FULL_ADDER_SUBTRACTOR

Implementation-of-Full-Adder-and-Full-subtractor-circuit

*AIM:*

To design a Full Adder and Full Subtractor circuit and verify its truth table in Quartus using Verilog programming.

*Equipments Required:*

Hardware – PCs, Cyclone II , USB flasher

Software – Quartus prime

*Full Adder and Full Subtractor*

*Full Adder*

Full adder is a digital circuit used to calculate the sum of three binary bits. It consists of three inputs and two outputs. Two of the input variables, denoted by A and B, represent the two significant bits to be added. The third input, Cin, represents the carry from the previous lower significant position. Two outputs are necessary because the arithmetic sum of three binary digits ranges in value from 0 to 3, and binary 2 or 3 needs two digits. The two outputs are sum and carry.

Sum =A’B’Cin + A’BCin’ + ABCin + AB’Cin’ = A ⊕ B ⊕ Cin 

Carry = AB + ACin + BCin

![image](https://github.com/naavaneetha/FULL_ADDER_SUBTRACTOR/assets/154305477/0f30ba51-5ffb-4198-845f-18e054f675e7)

*Figure -1 FULL ADDER*

*Full Subtractor*

A full subtractor is a combinational circuit that performs subtraction involving three bits, namely minuend, subtrahend, and borrow-in . It accepts three inputs: minuend, subtrahend and a borrow bit and it produces two outputs: difference and borrow.

![image](https://github.com/naavaneetha/FULL_ADDER_SUBTRACTOR/assets/154305477/02b24f51-ab51-4304-9ad6-7b81ffc1ead5)

Diff = A ⊕ B ⊕ Bin 

Borrow out = A'Bin + A'B + BBin

*Truthtable*
### FULL ADDER
![image](https://github.com/user-attachments/assets/5e3486b4-8d0e-438e-9bea-93cba27e24b9)

### FULL SUBTRACTOR
![image](https://github.com/user-attachments/assets/bf0954ef-e8db-414a-a9f9-92530d5779e0)

## Procedure

1.Open Quartus Software.

2.Create a New Project.

3.Create a New Design File.

4.Compile the Program.

5.Generate RTL Schematic.

6.Create Nodes for Inputs/Outputs

7.Generate Timing Diagram

8.Simulate Different Input Combinations

9.Save Your Work


*Program:*

/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.

Developed by: AKBAR I
RegisterNumber:212224230014

FULL ADDER
```
module fa1_df(sum, cout, a, b, cin);
    output sum;
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
```
FULL SUBTRACTOR
```
module fullsub(df, bo, a, b, bin);
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

## RTL Schematic
### FULL_ADDER
![Screenshot 2025-04-11 134429](https://github.com/user-attachments/assets/3ff00ed4-4602-4177-b2c6-db3621b9ab11)
### FULL_SUBTRACTOR
![Screenshot 2025-04-11 134437](https://github.com/user-attachments/assets/ae4c59b3-5c17-40d9-87ee-339947e1058d)


*Output Timing Waveform*
![Screenshot 2025-04-11 134548](https://github.com/user-attachments/assets/926bb21d-3637-4db3-a43a-80e95e790756)
![Screenshot 2025-04-11 134525](https://github.com/user-attachments/assets/96e41934-f130-4b46-85d0-3841be976fff)

*Result:*

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.
