# BOOLEAN_FUNCTION_MINIMIZATION

**AIM:**

To implement the given logic function verify its operation in Quartus using Verilog programming.

F1= A’B’C’D’+AC’D’+B’CD’+A’BCD+BC’D 

F2=xy’z+x’y’z+w’xy+wx’y+wxy

**Equipment Required:**

Hardware – PCs, Cyclone II , USB flasher

**Software – Quartus prime**

**Theory**

**Logic Diagram**

**Procedure**

1.	Type the program in Quartus software.

2.	Compile and run the program.

3.	Generate the RTL schematic and save the logic diagram.

4.	Create nodes for inputs and outputs to generate the timing diagram.

5.	For different input combinations generate the timing diagram.


**Program:**

/* Program to implement the given logic function and to verify its operations in quartus using Verilog programming. 

Developed by: RegisterNumber:*/
~~~
//Program to compute the function f1=a'b'c'd'+ac'd'+b'cd'+a'bcd+bc'd
//f2=xy'z+x'y'z+w'xy+wx'y+wxy
// simplify the logic using Boolean minimization/k map 
//compute f2 and write verilog code for f2 as like f1
module ex2(a,b,c,d,w,x,y,z,f1,f2);
input a,b,c,d,w,x,y,z;
output f1,f2;
wire adash,bdash,cdash,ddash,ydash,p,q,r,s,t,u;
not(adash,a);
not(bdash,b);
not(cdash,c);
not(ddash,d);
not(ydash,y);
and(p,bdash,ddash);
and(q,adash,b,d);
and(r,a,b,cdash);
or(f1,p,q,r);
and (s,ydashz);
and (t,x,y);
and (u,w,y);
or (f2,s,t,u);
endmodule
~~~


**RTL realization**

**Output:**![Screenshot 2024-03-23 114741](https://github.com/vijayashreeb14/BOOLEAN_FUNCTION_MINIMIZATION/assets/161238151/77aded87-1834-4fab-8565-71399078044a)


**RTL**
![Screenshot 2024-03-23 114805](https://github.com/vijayashreeb14/BOOLEAN_FUNCTION_MINIMIZATION/assets/161238151/72b43f72-b941-4c3b-9cb5-a9cb59f8e0bc)


**Timing Diagram**

**Result:**

Thus the given logic functions are implemented using and their operations are verified using Verilog programming.

