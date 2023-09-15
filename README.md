# Exp-03-Implementation-of-Half-Adder-and-Full-Adder-circuit

# Implementation-of-Half-Adder-and-Full-Adder-circuit
### AIM:
To design a half adder and full adder circuit and verify its truth table in Quartus using Verilog programming.

### Equipments Required:
Hardware – PCs, Cyclone II , USB flasher
Software – Quartus prime
Theory
Adders are digital circuits that carry out addition of numbers.

### Half Adder
Half adder is a combinational circuit that performs simple addition of two binary numbers. The input variables designate the augend and addend bits; the output variables produce the sum and carry. It is necessary to specify two output variables because the result may consist of two binary digits.

Sum = A’B+AB’ =A ⊕ B Carry = AB

### Full Adder
Full adder is a digital circuit used to calculate the sum of three binary bits. It consists of three inputs and two outputs. Two of the input variables, denoted by A and B, represent the two significant bits to be added. The third input, Cin, represents the carry from the previous lower significant position. Two outputs are necessary because the arithmetic sum of three binary digits ranges in value from 0 to 3, and binary 2 or 3 needs two digits. The two outputs are sum and carry.

Sum =A’B’Cin + A’BCin’ + ABCin + AB’Cin’ = A ⊕ B ⊕ Cin Carry = AB + ACin + BCin

 ![image](https://user-images.githubusercontent.com/36288975/163552156-a13e5a56-c638-4110-97d9-8896907c8d25.png)

#### Figure -01 HALF ADDER 


![image](https://user-images.githubusercontent.com/36288975/163552057-b3547877-6d07-45b4-b7e0-bcfebfad9e1d.png)

#### Figure -02 FULL ADDER 
## Theory:
Logic gates are electronic circuits which perform logical functions on one or more inputs to produce one output.
#### OR Gate:
The OR gate is a fundamental digital logic gate that operates on two binary inputs, producing an output of 1 if at least one input is 1. It symbolizes logical disjunction and is essential in building logical circuits and decision-making processes in computers and electronics.
#### AND Gate:
The AND gate is a fundamental digital logic gate with two inputs and one output. It produces a high output (1) only when both input signals are high (1). If any input is low (0), the output remains low. It's a building block for more complex logic circuits and is integral in digital computations.
#### NOT Gate:
The NOT gate is a fundamental digital logic gate. It has a single input and a single output. The output is the inverse of the input: if the input is high (1), the output is low (0), and vice versa. It's a basic building block in digital circuits, used for logic inversion.

### Procedure

Connect the supply (+5V) to the circuit
Switch ON the main switch
If the output is 1, then the led glows.

1. Create a New Project:
   - Open Quartus and create a new project by selecting "File" > "New Project Wizard."
   - Follow the wizard's instructions to set up your project, including specifying the project name, location, and target device (FPGA).

2. Create a New Design File:
   - Once the project is created, right-click on the project name in the Project Navigator and select "Add New File."
   - Choose "Verilog HDL File" or "VHDL File," depending on your chosen hardware description language.

3. Write the Combinational Logic Code:
   - Open the newly created Verilog or VHDL file and write the code for your combinational logic.
     
4. Compile the Project:
   - To compile the project, click on "Processing" > "Start Compilation" in the menu.
   - Quartus will analyze your code, synthesize it into a netlist, and perform optimizations based on your target FPGA device.

5. Analyze and Fix Errors:*
   - If there are any errors or warnings during the compilation process, Quartus will display them in the Messages window.
   - Review and fix any issues in your code if necessary.
   - View the RTL diagram.

6.*Verification:
   - Click on "File" > "New" > "Verification/Debugging Files" > "University Program VWF".
   - Once Waveform is created Right Click on the Input/Output Panel > " Insert Node or Bus" > Click on Node Finder > Click On "List" > Select All.
   - Give the Input Combinations according to the Truth Table amd then simulate the Output Waveform.
### Program:
```
/*
Program to design a half adder and full adder circuit and verify its truth table in quartus using Verilog programming.
Developed by: BHARATHGANESH S
RegisterNumber:  212222230022
*/
```
### Half Adder
```
module HalfAdder(A,B,sum,carry);
input A,B;
output sum,carry;
assign sum= A^B;
assign carry = A&B;
endmodule
```
### Full Adder
```
module FullAdder(A,B,Cin,sum,carry);
input A,B,Cin;
output sum,carry;
assign sum= A^B^Cin;
assign carry = (A&B)|((A^B)&Cin);
endmodule
```
### RTL DIAGRAM
### Half Adder
![exp3a RTL](https://github.com/bharathganeshsivasankaran/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/119478098/21b8e6bb-6e21-4aa3-b0f0-744b1ca9ce0a)
### Full Adder
![exp3b](https://github.com/bharathganeshsivasankaran/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/119478098/c5226ba2-6b7a-413f-bc35-39f351b2425c)

### Output Waveform
### Half Adder
![ex3halfadder](https://github.com/bharathganeshsivasankaran/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/119478098/d74502ad-b909-495b-8c8e-323eec0c3eac)
### Full Adder
![exp3b FULL ADDER](https://github.com/bharathganeshsivasankaran/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/119478098/b775e525-3ef6-4e6e-b502-c3bd94c0657d)

### TRUTH TABLE 
### Half Adder
![HALADDER](https://github.com/bharathganeshsivasankaran/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/119478098/2a164203-31f7-4c75-80eb-bd791d6e29e8)
### Full Adder
![FULLADDER](https://github.com/bharathganeshsivasankaran/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/119478098/d4372249-11be-4609-80d7-296c0a482f2c)

### Result:
Thus, a half adder and full adder circuit is designed to verify its truth table in Quartus using Verilog
programming.
