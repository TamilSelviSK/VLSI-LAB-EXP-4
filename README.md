# SIMULATE AND SYNTHESIS SR, JK, T, D - FLIPFLOP, COUNTER DESIGN USING VIVADO.
## AIM: 
  To simulate and synthesis SR, JK, T, D - FLIPFLOP, COUNTER DESIGN using VIVADO.

 ## APPARATUS REQUIRED:
 VIVADO 2023.2

## PROCEDURE:
### STEP:1 
Start the Vivado, Select and Name the New project.<br>
### STEP:2
Select the device family, device, package and speed. <br>
### STEP:3 
Select new source in the New Project and select Verilog Module as the Source type.<br>
### STEP:4 
Type the File Name and Click Next and then finish button. Type the code and save it.<br>
### STEP:5
Select the Behavioural Simulation in the Source Window and click the check syntax.<br>
### STEP:6 
Click the simulation to simulate the program and give the inputs and verify the outputs as per the truth table.<br>             

## SR FLIPFLOP:

![image](https://github.com/Sachita02/VLSI-LAB-EXP-4/assets/162723490/f2860206-87ff-4167-943c-82964a253db2)


## PROGRAM:
```
module sr_ff(clk,q,rst,s,r);<br>
input s,r,clk,rst;<br>
output reg q;<br>
always@(posedge clk)<br>
begin<br>
if(rst==1)<br>
q=1'b0;<br>
else<br>
begin<br>
case({s,r})<br>
2'b00:q=q;<br>
2'b01:q=1'b0;<br>
2'b10:q=1'b1;<br>
2'b11:q=1'bx;<br>
endcase<br>
end<br>
end<br>
endmodule<br>
```


## OUTPUT:               
                   
![image](https://github.com/Sachita02/VLSI-LAB-EXP-4/assets/162723490/24f238c7-9325-491a-9c31-52370ce92caa)


## JK FLIPFLOP:

![image](https://github.com/Sachita02/VLSI-LAB-EXP-4/assets/162723490/4256e509-b064-4f71-9e3f-e14587b64dd0)


## PROGRAM:
```
module jk_ff(clk,q,rst,j,k);<br>
input j,k,clk,rst;<br>
output reg q;<br>
always@(posedge clk)<br>
begin<br>
if(rst==1)<br>
q=1'b0;<br>
else<br>
begin<br>
case({j,k})<br>
2'b00:q=q;<br>
2'b01:q=1'b0;<br>
2'b10:q=1'b1;<br>
2'b11:q=~q;<br>
endcase<br>
end<br>
end<br>
endmodule<br>
```
## OUTPUT:

![image](https://github.com/Sachita02/VLSI-LAB-EXP-4/assets/162723490/52b33837-1dec-4c79-a41f-6ae98a35fec5)


## T FLIPFLOP
	
![image](https://github.com/Sachita02/VLSI-LAB-EXP-4/assets/162723490/71d57328-673b-41f5-90e6-d63a7f08877c)


## PROGRAM: 
```
module t_ff(clk,q,rst,t);<br>
input t,clk,rst;<br>
output reg q;<br>
always@(posedge clk)<br>
begin<br>
if(rst==1)<br>
q=1'b0;<br>
else<br>
if(t==0)<br>
q=q;<br>
else<br>
q=~q;<br>
end<br>
endmodule
```

## OUTPUT

![image](https://github.com/Sachita02/VLSI-LAB-EXP-4/assets/162723490/7f0a5fae-e338-4b7f-9897-5b07d35f4a98)

                

## D FLIPFLOP:

![image](https://github.com/Sachita02/VLSI-LAB-EXP-4/assets/162723490/e84a13f7-61b2-433c-b9e2-4ae4399d9842)


## PROGRAM:
```
module d_ff(clk,q,rst,d);<br>
input d,clk,rst;<br>
output reg q;<br>
always@(posedge clk)<br>
begin<br>
if(rst==1)<br>
q=1'b0;<br>
else<br>
q=d;<br>
end<br>
endmodule<br>
```
## OUTPUT:

![image](https://github.com/Sachita02/VLSI-LAB-EXP-4/assets/162723490/60bc0cd8-d337-411f-8e2f-b651992cfac3)

## MOD 10 COUNTER
![image](https://github.com/Sachita02/VLSI-LAB-EXP-4/assets/162723490/09e9f7b6-a07d-4cf6-9005-d9f9621c7e9c)

## PROGRAM
```
module mod_10(clk,rst,out); <br>
input clk,rst; <br>
output reg[3:0]out;<br>
always@(posedge clk)<br>
begin<br>
if(rst==1|out==9)<br>
out=4'b0;<br>
else<br>
out=out+1;<br>
end<br>
endmodule<br>
```
## OUTPUT
![image](https://github.com/Sachita02/VLSI-LAB-EXP-4/assets/162723490/e1ce8d5f-2664-4b64-8f2f-d56295cdf690)


## UP-DOWN-COUNTER
![image](https://github.com/Sachita02/VLSI-LAB-EXP-4/assets/162723490/01e4f27d-ba10-4db4-8248-2f075a416800)

## PROGRAM
```
module updown_counter(clk,rst,ud,out); 
input clk,rst,ud; 
output reg[3:0]out;
always@(posedge clk)
begin
if(rst==1)
out=4'b0;
else if (ud==1)
out=out+1;
else if(ud==0)
out=out-1;
end
endmodule
```

## OUTPUT
![image](https://github.com/Sachita02/VLSI-LAB-EXP-4/assets/162723490/063b9f9f-8926-4a04-98c4-9ffd80697cf7)



## RESULT:
	The simulate and synthesis SR, JK, T, D - FLIPFLOP, COUNTER DESIGN using VIVADO is successfully verified.

