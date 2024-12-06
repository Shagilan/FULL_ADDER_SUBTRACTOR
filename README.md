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
![Screenshot 2024-11-28 111318](https://github.com/user-attachments/assets/91a62e2d-3715-4a24-b4d6-4474d6d846b6)
![Screenshot 2024-11-28 111332](https://github.com/user-attachments/assets/4ee8afb0-5781-40b3-833f-b996f2f11085)

**Procedure**
```
1)Create a New Project in Quartus:
-Open Quartus and create a new project.
-Set the target device (FPGA or CPLD) for your project.

2)Add Verilog File:
-In the project, add a new Verilog file (.v).
-Copy and paste the Verilog code for the Full Adder and Full Subtractor modules (with testbenches) into the file.

3)Compile the Design:
-Click on Compile to check for syntax errors and to synthesize the design.

4)Set Up Simulation (ModelSim):
-Open ModelSim (integrated with Quartus).
-Set up a simulation for the Verilog testbench by specifying the testbench module to simulate.
-Add simulation libraries if necessary.

5)Run the Simulation:
-In ModelSim, run the simulation.
-Observe the waveforms or outputs to verify the truth table results for both the Full Adder and Full Subtractor.

6)Verify Outputs:
-Ensure the outputs match the expected truth tables for both circuits.
-Full Adder should output Sum and Carry (Cout).
-Full Subtractor should output Difference (D) and Borrow (Bout).

7)Finish and Save:
-Save the results and the project.
```
**Program:**
  ```
/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming. 
Developed by: SHAGILAN U
RegisterNumber: 24013515

module exp4(a,b,cin,bin,sum,carry,difference,borrow);
input a,b,cin,bin;
output sum,carry,difference,borrow;
assign sum=( (a ^ b)^cin);
assign carry= ( (a & b)| ( cin &(a ^ b )));
assign difference= ( (a ^ b)^bin);
assign borrow= ( ( a & b)| ( bin & ((a ^ b ))));


*/

```
**RTL Schematic**
![Screenshot 2024-11-28 112042](https://github.com/user-attachments/assets/286c6bf5-0729-4f42-bc71-7feaf5190279)

**Output Timing Waveform**
![Screenshot 2024-11-28 112147](https://github.com/user-attachments/assets/8ad010b5-1204-4d83-9b80-661518bf3edf)

**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



