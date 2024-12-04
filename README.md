# D-FLIPDLOP-NEGEDGE

**AIM:**

To implement  D flipflop using verilog and validating their functionality using their functional tables

**SOFTWARE REQUIRED:**

Quartus prime

**THEORY**

**D Flip-Flop**

D flip-flop operates with only positive clock transitions or negative clock transitions. Whereas, D latch operates with enable signal. That means, the output of D flip-flop is insensitive to the changes in the input, D except for active transition of the clock signal. The circuit diagram of D flip-flop is shown in the following figure.

![image](https://github.com/naavaneetha/D-FLIPDLOP-NEGEDGE/assets/154305477/48c81fe8-bc3f-40e7-95e2-519fc155ad51)

This circuit has single input D and two outputs Qtt & Qtt’. The operation of D flip-flop is similar to D Latch. But, this flip-flop affects the outputs only when positive transition of the clock signal is applied instead of active enable. The following table shows the state table of D flip-flop.

![image](https://github.com/naavaneetha/D-FLIPDLOP-NEGEDGE/assets/154305477/e5f3fda7-68ec-4a3a-a0a4-cf6f9cc4ab55)

Therefore, D flip-flop always Hold the information, which is available on data input, D of earlier positive transition of clock signal. From the above state table, we can directly write the next state equation as Qt+1t+1 = D

![image](https://github.com/naavaneetha/D-FLIPDLOP-NEGEDGE/assets/154305477/8592c0d8-2917-4142-91b9-d6c30dd891d2)

Next state of D flip-flop is always equal to data input, D for every positive transition of the clock signal. Hence, D flip-flops can be used in registers, shift registers and some of the counters.

**Procedure**

1. Define a Verilog module for the D flip-flop with inputs (D, CLK) and outputs (Q, Q_bar).

2. Declare input and output ports for the module.

3. Write Verilog code to implement the D flip-flop logic based on its functional table. Use a synchronous always @(posedge CLK) block to trigger the flip-flop on the positive edge of the clock signal.

4. Write a Verilog testbench to simulate the behavior of the D flip-flop under different input conditions.

5. In the testbench, apply various combinations of input stimuli (D, CLK) to cover all possible input states.

6. Verify that the output behavior of the D flip-flop matches the expected behavior defined by its functional table.

7. Ensure that there are no race conditions or undefined states in the design by analyzing the timing and sequence of input changes.

**PROGRAM**
```
Program for flipflops and verify its truth table in quartus using Verilog programming.
Developed by: ASTLE JOE A S
RegisterNumber: 24004571

module exp8(d, clk, rst, q);
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

![WhatsApp Image 2024-12-03 at 14 31 28_50a9f727](https://github.com/user-attachments/assets/25ac3727-322b-4510-ac2b-1bdac6ddb5c8)


**TIMING DIGRAMS FOR FLIP FLOPS**

![WhatsApp Image 2024-12-03 at 14 44 51_bf1b1ba2](https://github.com/user-attachments/assets/41d4f04a-a9b9-4e38-b5dc-1d3310ac3de3)

**RESULTS**

Thus the D flipflop using verilog and validating their functionality using their functional tables are verified.
