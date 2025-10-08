# BOOLEAN_FUNCTION_MINIMIZATION

**AIM:**

To implement the given logic function verify its operation in Quartus using Verilog programming.

F1= A’B’C’D’+AC’D’+B’CD’+A’BCD+BC’D 

F2=xy’z+x’y’z+w’xy+wx’y+wxy

**Equipment Required:**

Hardware – PCs, Cyclone II , USB flasher

**Software – Quartus prime**

**Theory**
In digital electronics, a Boolean function expresses the relationship between input and output variables using Boolean algebra.
It can be realized using logic gates such as AND, OR, and NOT.

A combinational circuit is one in which the output depends only on the current values of the inputs and not on any previous states.
The process of minimizing a Boolean function aims to reduce the number of logic gates used while maintaining the same output behavior.
This can be done using Boolean algebra laws or K-map (Karnaugh Map) simplification.

Once the Boolean function is minimized, it can be implemented in Verilog HDL using logic operators:

~ → NOT

& → AND

| → OR

🔸 Part (i): Implementation of f1
Given Function:
𝑓
1
=
(
𝑏
‾
⋅
𝑑
‾
)
+
(
𝑎
‾
⋅
𝑏
⋅
𝑑
)
+
(
𝑎
⋅
𝑏
⋅
𝑐
‾
)
f1=(
b
⋅
d
)+(
a
⋅b⋅d)+(a⋅b⋅
c
)
Verilog Code:
module funct1(a,b,c,d,f1);
input a,b,c,d;
output f1;
assign f1 = ((~b & ~d) | (~a & b & d) | (a & b & ~c));
endmodule

Explanation:

The function has four inputs: a, b, c, d

The output f1 is derived from three product (AND) terms combined by OR operations.

The circuit performs logic operations equivalent to the given Boolean expression.

This function can be realized using AND, OR, and NOT gates.

🔸 Part (ii): Implementation of f2
Given Function:
𝑓
2
=
(
𝑦
‾
⋅
𝑧
)
+
(
𝑤
⋅
𝑦
)
+
(
𝑥
⋅
𝑦
)
f2=(
y
	​

⋅z)+(w⋅y)+(x⋅y)
Verilog Code:
module funct2(w,x,y,z,f2);
input w,x,y,z;
output f2;
assign f2 = ((~y & z) | (w & y) | (x & y));
endmodule

Explanation:

The function has four inputs: w, x, y, z

The output f2 is formed from three AND terms, joined by an OR gate.

Each product term represents a minterm from the simplified Boolean function.

This is also a combinational circuit, where output depends only on the present input values.

TRUTH TABLE REPRESENTATION:

You can verify both functions using their truth tables by listing all possible input combinations (16 combinations for 4 inputs) and checking which combinations give output = 1 according to the Boolean expression.

APPLICATIONS:

Used in digital logic design and optimization of circuits.

Common in arithmetic logic units (ALU) and control logic.

Helps in simplifying complex Boolean equations for hardware implementation.

RESULT:

The given Boolean functions f1 and f2 were successfully implemented using Verilog HDL and verified through simulation.
The outputs matched the expected truth table values, confirming correct logic design.

Would you like me to include K-map simplification steps for f1 and f2 in the theory (as many colleges require it under “Minimization of Boolean Function”)?

**Logic Diagram**

**Procedure**

1.	Type the program in Quartus software.

2.	Compile and run the program.

3.	Generate the RTL schematic and save the logic diagram.

4.	Create nodes for inputs and outputs to generate the timing diagram.

5.	For different input combinations generate the timing diagram.


**Program:**

/* Program to implement the given logic function and to verify its operations in quartus using Verilog programming. 

Developed by: RegisterNumber:*/ 25018734
i)
module funct1(a,b,c,d,f1);
input a,b,c,d;
output f1;
assign f1=((~b & ~d)|(~a & b & d)|(a & b & ~c));
endmodule

ii)
module funct2(w,x,y,z,f2);
input w,x,y,z;
output f2;
assign f2=((~y & z)|( w & y )|(x & y));
endmodule


**RTL realization**
<img width="1920" height="1080" alt="Screenshot (30)" src="https://github.com/user-attachments/assets/9eec2853-627e-4e26-80a0-d7c4909cc9a8" />
<img width="681" height="319" alt="Screenshot (44)" src="https://github.com/user-attachments/assets/24b343f6-d3b6-4dc3-8906-9dd5698150c9" />



**Output:**

**RTL**
<img width="1920" height="1080" alt="Screenshot (31)" src="https://github.com/user-attachments/assets/61b7d0b6-a2f0-4149-ae0c-c211e94abd7e" />
![IMG-20251008-WA0009 1](https://github.com/user-attachments/assets/18d26ce5-a0ff-48cb-b8aa-16473d6ca75a)


**Timing Diagram**

**Result:**

Thus the given logic functions are implemented using and their operations are verified using Verilog programming.

