# SERIAL-IN-SERIAL-OUT-SHIFTREGISTER

**AIM:**

To implement  SISO Shift Register using verilog and validating their functionality using their functional tables

**SOFTWARE REQUIRED:**

Quartus prime



**SISO shift Register**

A Serial-In Serial-Out shift register is a sequential logic circuit that allows data to be shifted in and out one bit at a time in a serial manner. It consists of a cascade of flip-flops connected in series, forming a chain. The input data is applied to the first flip-flop in the chain, and as the clock pulses, the data propagates through the flip-flops, ultimately appearing at the output.

The logic circuit provided below demonstrates a serial-in serial-out (SISO) shift register. It comprises four D flip-flops that are interconnected in a sequential manner. These flip-flops operate synchronously with one another, as they all receive the same clock signal.

![image](https://github.com/naavaneetha/SERIAL-IN-SERIAL-OUT-SHIFTREGISTER/assets/154305477/e81c4072-37f9-46c6-8145-566764b74c3a)

Figure 01 4 Bit SISO Register

The synchronous nature of the flip-flops ensures that the shifting of data occurs in a coordinated manner. When the clock signal rises, the input data is sampled and stored in the first flip-flop. On subsequent clock pulses, the stored data propagates through the flip-flops, moving from one flip-flop to the next.
Each D flip-flop in the circuit has a Data (D) input, a Clock (CLK) input, and an output (Q). The D input represents the data to be loaded into the flip-flop, while the CLK input is connected to the common clock signal. The output (Q) of each flip-flop is connected to the D input of the next flip-flop, forming a cascade.

**Procedure**

1)Connect the circuit: apply clock to the shift register and connect serial input (sin) and outputs (Q0–Q3).

2)Set the initial value by giving the first bit on the serial input.

3)Generate the clock pulses using a function generator or simulation clock.

4)Apply the clock: at every rising edge, the data shifts one position right (Q0→Q1→Q2→Q3).

5)Change the serial input as required to create the counting sequence.

6)Observe and record the output pattern of Q0–Q3 after each clock pulse.

**PROGRAM**

module EXP10(clk, sin, q);

input clk;

input sin;

output [3:0] q;

reg [3:0] q;

always @(posedge clk)

begin

q[0] <= sin;

q[1] <= q[0];

q[2] <= q[1];

q[3] <= q[2];

end

endmodule

**RTL LOGIC FOR SISO Shift Register**
<img width="1920" height="1080" alt="Screenshot (135)" src="https://github.com/user-attachments/assets/3cab50fe-fb85-4df0-bb5d-021289a09936" />

**TIMING DIGRAMS FOR SISO Shift Register**
<img width="1920" height="1080" alt="Screenshot (136)" src="https://github.com/user-attachments/assets/c5837269-958e-410f-8b34-1a8b4db3efdd" />

**RESULTS**
the program to generate Serial-In Serial-Outshift register has been run successfully and obtained the expected output.
