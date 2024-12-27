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
Full Adder

![WhatsApp Image 2024-12-21 at 21 42 20_96876c69](https://github.com/user-attachments/assets/4c20ae54-8e5f-48db-888c-72169c96ce09)

Full Subtractor

![WhatsApp Image 2024-12-21 at 21 46 51_5be87e73](https://github.com/user-attachments/assets/b8dd6332-1190-4f03-9761-c76a6b619f75)

**Procedure**

1.	Type the program in Quartus software.

2.	Compile and run the program.

3.	Generate the RTL schematic and save the logic diagram.

4.	Create nodes for inputs and outputs to generate the timing diagram.

5.	For different input combinations generate the timing diagram.


Write the detailed procedure here

**Program:**

Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.
Developed by:n v mohan krishna RegisterNumber:24000587

      i)FULL ADDER
      
      module fa(a,b,cin,sum,carry);
      input a,b,cin;
      output sum,carry;
      assign sum=( (a ^ b)^cin);
      assign carry= ( (a & b)| ( cin &(a ^ b )));
      endmodule

    ii)FULL SUBTRACTOR
    
    module fs(a,b,bin,difference,borrow);
    input a,b,bin;
    output difference,borrow;
    assign difference= ( (a ^ b)^bin);
    assign borrow= ( ( ~a & b)| ( bin & (~(a ^ b ))));
    endmodule


**RTL Schematic**

Full Adder

![ex4fa](https://github.com/user-attachments/assets/5f9cdb9d-76d5-420f-8979-7608118e60b6)

Full subtractor

![Screenshot 2024-11-16 021556](https://github.com/user-attachments/assets/93cbefab-e0d3-43e4-b7c0-0a0cb17a4df8)

**Timing Waveform**

Full Adder

![ex-4fa](https://github.com/user-attachments/assets/6cf64a41-28de-4790-b680-afa6b5da8e64)

Full subtractor

![Screenshot 2024-11-16 021801](https://github.com/user-attachments/assets/2e9eefb7-2a1b-481b-a2bf-2b8408d1d442)

**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



