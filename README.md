# SR-FLIPFLOP-USING-CASE
This circuit has two inputs S & R and two outputs Qtt & Qtt’. The operation of SR flipflop is similar to SR Latch. But, this flip-flop affects the outputs only when positive transition of the clock signal is applied instead of active enable. The following table shows the state table of SR flip-flop.

![image](https://github.com/naavaneetha/SR-FLIPFLOP-USING-CASE/assets/154305477/dabfc4f4-87e3-4cbc-9472-f89ee1b5ed30)

 
Here, Qtt & Qt+1t+1 are present state & next state respectively. So, SR flip-flop can be used for one of these three functions such as Hold, Reset & Set based on the input conditions, when positive transition of clock signal is applied. The following table shows the characteristic table of SR flip-flop. Present Inputs Present State Next State

![image](https://github.com/naavaneetha/SR-FLIPFLOP-USING-CASE/assets/154305477/dd90d16c-aec5-4290-a586-e2346b1e9eb5)

 
By using three variable K-Map, we can get the simplified expression for next state, Qt+1t+1. The three variable K-Map for next state, Qt+1t+1 is shown in the following figure.

![image](https://github.com/naavaneetha/SR-FLIPFLOP-USING-CASE/assets/154305477/473efad6-d70b-4ca7-aeb7-898bbfca319f)

 
The maximum possible groupings of adjacent ones are already shown in the figure. Therefore, the simplified expression for next state Qt+1t+1 is Q(t+1)=S+R′Q(t)Q(t+1)=S+R′Q(t)

**Procedure**

/* write all the steps invloved */

**PROGRAM**

/* Program for flipflops and verify its truth table in quartus using Verilog programming. Developed by: M.V.Vamsidhar Reddy
RegisterNumber: 212224040205
*/

module ex6(din, clk, rst, dout); 
    input din; 
    input clk; 
    input rst; 
    output dout; 
  reg dout; 
  reg [7:0]x; 
  always @ (posedge(clk) or posedge(rst)) begin 
  if (rst==1'b1) 
  begin 
  dout=8'hzz; 
  end 
  else 
  begin 
  x={x[6:0],din}; 
  dout=x[7]; 
  end 
  end 
  endmodule


**RTL LOGIC FOR FLIPFLOPS**

<img width="1193" height="746" alt="image" src="https://github.com/user-attachments/assets/b1b666a4-cb16-4eca-9744-4186e012d0f3" />


**TIMING DIGRAMS FOR FLIP FLOPS**

<img width="1200" height="758" alt="image" src="https://github.com/user-attachments/assets/f5664898-bff5-491a-8e22-d8607d39a8f7" />


**RESULTS**
Thus the SR flipflop using verilog is implemented and validated their functionality using their functional tables
