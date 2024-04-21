# VLSI-LAB-EXP-4
SIMULATION AND IMPLEMENTATION OF SEQUENTIAL LOGIC CIRCUITS

**AIM**: 

 To simulate and synthesis SR, JK, T, D - FLIPFLOP, COUNTER DESIGN using Xilinx ISE.

**APPARATUS REQUIRED**:

Xilinx 14.7
Spartan6 FPGA

**LOGIC DIAGRAM**

**SR FLIPFLOP**

![image](https://github.com/navaneethans/VLSI-LAB-EXP-4/assets/6987778/77fb7f38-5649-4778-a987-8468df9ea3c3)


**JK FLIPFLOP**

![image](https://github.com/navaneethans/VLSI-LAB-EXP-4/assets/6987778/1510e030-4ddc-42b1-88ce-d00f6f0dc7e6)

**T FLIPFLOP**

![image](https://github.com/navaneethans/VLSI-LAB-EXP-4/assets/6987778/7a020379-efb1-4104-85ee-439d660baa08)


**D FLIPFLOP**

![image](https://github.com/navaneethans/VLSI-LAB-EXP-4/assets/6987778/dda843c5-f0a0-4b51-93a2-eaa4b7fa8aa0)


**COUNTER**

![image](https://github.com/navaneethans/VLSI-LAB-EXP-4/assets/6987778/a1fc5f68-aafb-49a1-93d2-779529f525fa)


  
**PROCEDURE**:

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

**VERILOG CODE**

**SR FLIP FLOP**

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

**JK FLIP FLOP**

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

**T FLIP FLOP**

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

**D FLIP FLOP**

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

**MODE 10 COUNTER**

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

**UPDOWN COUNTER**

module updown_counter(clk,rst,ud,out);

input clk,rst,ud; o

Output reg[3:0]out;

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

**OUTPUT WAVEFORM**

**SR FLIP FLOP**

![image](https://github.com/REkha18s/VLSI-LAB-EXP-4/assets/161815097/97771e14-35da-41c3-b10f-a07cdd515129)

**JK FLIP FLOP**

![image](https://github.com/REkha18s/VLSI-LAB-EXP-4/assets/161815097/ac5bdde8-9ab9-45fa-86ba-2bb50156ecbf)

**T FLIP FLOP**

![image](https://github.com/REkha18s/VLSI-LAB-EXP-4/assets/161815097/ae3eaaf3-4b24-4a50-8df9-ea54268b0cd8)

**D FLIP FLOP**

![image](https://github.com/REkha18s/VLSI-LAB-EXP-4/assets/161815097/433b4e49-d61b-4613-ad21-0f81d8ce28fe)

**MOD 10 COUNTER**

![image](https://github.com/REkha18s/VLSI-LAB-EXP-4/assets/161815097/e2ee3aac-bcd7-45f7-9db1-99f42dba1f40)

**UP DOWN COUNTER**

![image](https://github.com/REkha18s/VLSI-LAB-EXP-4/assets/161815097/c3c69c2a-dd35-4b9c-9f56-70022370d03c)

**RESULT**

Thus simulate and synthesis SR, JK, T, D - FLIPFLOP, COUNTER DESIGN using VIVADO is successfully verified.


