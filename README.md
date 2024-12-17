# D-FLIPDLOP-NEGEDGE

**AIM:**

To implement  D flipflop using verilog and validating their functionality using their functional tables

**SOFTWARE REQUIRED:**

Quartus prime

**THEORY**

**D Flip-Flop**

D flip-flop operates with only positive clock transitions or negative clock transitions. Whereas, D latch operates with enable signal. That means, the output of D flip-flop is insensitive to the changes in the input, D except for active transition of the clock signal. The circuit diagram of D flip-flop is shown in the following figure.

![image](https://github.com/user-attachments/assets/db5056a5-015d-4ede-a254-c7f77960f2c5)

This circuit has single input D and two outputs Qtt & Qtt’. The operation of D flip-flop is similar to D Latch. But, this flip-flop affects the outputs only when positive transition of the clock signal is applied instead of active enable. The following table shows the state table of D flip-flop.

![image](https://github.com/user-attachments/assets/693c8e59-2547-4507-b1ca-da1c07e5c38e)

Therefore, D flip-flop always Hold the information, which is available on data input, D of earlier positive transition of clock signal. From the above state table, we can directly write the next state equation as Qt+1t+1 = D

![image](https://github.com/user-attachments/assets/4bb2a4f5-2d23-495b-b8fd-32b342ed4b20)

Next state of D flip-flop is always equal to data input, D for every positive transition of the clock signal. Hence, D flip-flops can be used in registers, shift registers and some of the counters.

**Procedure**

1.Type the program in Quartus software.

2.Compile and run the program.

3.Generate the RTL schematic and save the logic diagram.

4.Create nodes for inputs and outputs to generate the timing diagram.

5.For different input combinations generate the timing diagram.

**PROGRAM**

/* Program for flipflops and verify its truth table in quartus using Verilog programming. Developed by:Paveen Kumaran SV
RegisterNumber:24000025
```
module Dflipflopneg_edge (d, clk, rst, q);
  input d, clk, rst;
  output reg q;

  always @(negedge clk or posedge rst) begin
    if (rst)
      q <= 0; // Reset the flip-flop
    else
      q <= d; // D input is passed to Q on the negative clock edge
  end
endmodule
```
**RTL LOGIC FOR FLIPFLOPS**

![image](https://github.com/user-attachments/assets/f0437611-f6a6-4897-9a1c-6ed8c9f94b24)

**TIMING DIGRAMS FOR FLIP FLOPS**

**RESULTS**
Thus the truth table for D-FLIPFLOP in Quartus II using Verilog programming are studied, verified and executed successfully.
