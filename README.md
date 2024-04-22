# VLSI-LAB-EXP-4
# SIMULATION AND IMPLEMENTATION OF SEQUENTIAL LOGIC CIRCUITS

# AIM: 
 To simulate and synthesis SR, JK, T, D - FLIPFLOP, COUNTER DESIGN using Xilinx ISE.

# APPARATUS REQUIRED:

Xilinx 14.7
Spartan6 FPGA

# LOGIC DIAGRAM 

# SR FLIPFLOP

![image](https://github.com/navaneethans/VLSI-LAB-EXP-4/assets/6987778/77fb7f38-5649-4778-a987-8468df9ea3c3)


# JK FLIPFLOP

![image](https://github.com/navaneethans/VLSI-LAB-EXP-4/assets/6987778/1510e030-4ddc-42b1-88ce-d00f6f0dc7e6)

# T FLIPFLOP

![image](https://github.com/navaneethans/VLSI-LAB-EXP-4/assets/6987778/7a020379-efb1-4104-85ee-439d660baa08)


# D FLIPFLOP

![image](https://github.com/navaneethans/VLSI-LAB-EXP-4/assets/6987778/dda843c5-f0a0-4b51-93a2-eaa4b7fa8aa0)


# COUNTER

![image](https://github.com/navaneethans/VLSI-LAB-EXP-4/assets/6987778/a1fc5f68-aafb-49a1-93d2-779529f525fa)


  
# PROCEDURE:
STEP:1  Start  the Xilinx navigator, Select and Name the New project.
STEP:2  Select the device family, device, package and speed.       
STEP:3  Select new source in the New Project and select Verilog Module as the Source type.                       
STEP:4  Type the File Name and Click Next and then finish button. Type the code and save it.
STEP:5  Select the Behavioral Simulation in the Source Window and click the check syntax.                       
STEP:6  Click the simulation to simulate the program and  give the inputs and verify the outputs as per the truth table.               
STEP:7  Select the Implementation in the Sources Window and select the required file in the Processes Window.
STEP:8  Select Check Syntax from the Synthesize  XST Process. Double Click in the  FloorplanArea/IO/Logic-Post Synthesis process in the User Constraints process group. UCF(User constraint File) is obtained. 
STEP:9  In the Design Object List Window, enter the pin location for each pin in the Loc column Select save from the File menu.
STEP:10 Double click on the Implement Design and double click on the Generate Programming File to create a bitstream of the design.(.v) file is converted into .bit file here.
STEP:11  On the board, by giving required input, the LEDs starts to glow light, indicating the output.

# VERILOG CODE

  #  SR FLIPFLOP
module sr_ff(clk,q,rst,s,r);

input s,r,clk,rst;

output reg q;

always@(posedge clk)

begin

if(rst==1)

q=1'b0;

else

begin

case({s,r})

2'b00:q=q;

2'b01:q=1'b0;

2'b10:q=1'b1;

2'b11:q=1'bx;

endcase

end

end

endmodule

# JK FLIPFLOP
module jk_ff(clk,q,rst,j,k);

input j,k,clk,rst;

output reg q;
always@(posedge clk)

begin

if(rst==1)

q=1'b0;

else

begin

case({j,k})

2'b00:q=q;

2'b01:q=1'b0;

2'b10:q=1'b1;

2'b11:q=~q;

endcase

end

end

endmodule

# T FLIPFLOP
module t_ff(clk,q,rst,t);

input t,clk,rst;

output reg q;

always@(posedge clk)

begin

if(rst==1)

q=1'b0;

else

if(t==0)

q=q;

else

q=~q;

end

endmodule

# D FLIPFLOP
module d_ff(clk,q,rst,d);

input d,clk,rst;

output reg q;

always@(posedge clk)

begin

if(rst==1)

q=1'b0;

else

q=d;

end

endmodule

# MOD 10 COUNTER
module mod_10(clk,rst,out);

input clk,rst;

output reg[3:0]out;

always@(posedge clk)

begin

if(rst==1|out==9)

out=4'b0;

else

out=out+1;

end

endmodule

# UPDOWN COUNTER
module updown_counter(clk,rst,ud,out);

input clk,rst,ud;

output reg[3:0]out;

always@(posedge clk) begin if(rst==1) out=4'b0; else if (ud==1) out=out+1;

else if(ud==0) out=out-1;

end endmodule



# OUTPUT WAVEFORM
 # SR FLIP FLOP 
![image](https://github.com/TamilSelviSK/VLSI-LAB-EXP-4/assets/118039197/023340d4-0207-4b4f-8069-4df513cee9e5)
# JK FLIP FLOP
![image](https://github.com/TamilSelviSK/VLSI-LAB-EXP-4/assets/118039197/529699bf-e8d6-460d-8300-0fd56fd0b68b)
# T FLIP FLOP
![image](https://github.com/TamilSelviSK/VLSI-LAB-EXP-4/assets/118039197/c29cbbd6-fcf4-4005-900b-97b3f2f7fab9)
# D FLIP FLOP
![image](https://github.com/TamilSelviSK/VLSI-LAB-EXP-4/assets/118039197/2c9e4490-def4-4567-9ae5-86107c771cee)
# MOD 10 COUNTER
![image](https://github.com/TamilSelviSK/VLSI-LAB-EXP-4/assets/118039197/43403fae-5abd-44a5-aa04-89b595bc6fa0)
# UPDOWN COUNTER
![image](https://github.com/TamilSelviSK/VLSI-LAB-EXP-4/assets/118039197/250495c1-eade-42fa-bf62-6f350ddce1b3)









# RESULT
Thus the simulation of sequential circuits is done and outputs are verified successfully


