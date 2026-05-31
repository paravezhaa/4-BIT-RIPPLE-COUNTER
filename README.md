# 4-BIT-RIPPLE-COUNTER

**AIM:**

To implement  4 Bit Ripple Counter using verilog and validating their functionality using their functional tables

**SOFTWARE REQUIRED:**

Quartus prime

**THEORY**

**4 Bit Ripple Counter**

A binary ripple counter consists of a series connection of complementing flip-flops (T or JK type), with the output of each flip-flop connected to the Clock Pulse input of the next higher-order flip-flop. The flip-flop holding the least significant bit receives the incoming count pulses. The diagram of a 4-bit binary ripple counter is shown in Fig. below.

![image](https://github.com/naavaneetha/4-BIT-RIPPLE-COUNTER/assets/154305477/cb4b74d4-31ab-4359-95d0-d22e67daba13)

In timing diagram Q0 is changing as soon as the negative edge of clock pulse is encountered, Q1 is changing when negative edge of Q0 is encountered(because Q0 is like clock pulse for second flip flop) and so on.

![image](https://github.com/naavaneetha/4-BIT-RIPPLE-COUNTER/assets/154305477/a573a7d6-014e-4e54-93e6-e2ac9530960b)

![image](https://github.com/naavaneetha/4-BIT-RIPPLE-COUNTER/assets/154305477/85e1958a-2fc1-49bb-9a9f-d58ccbf3663c)

**Procedure**

/* write all the steps invloved */

1.TYPE THE CODE IN THE QUARTUS SOFTWARE
2.COMPILE AND RUN THE CODE
3.GENERATE THE RTL VIEWER
4.CREATE NODES FOR INPUT AND OUTPUT NODES TO GENERATE TIMING DIAGRAM
5.FOR DIFFERENT COMBINATIONS OF INPUT GENERATE THE TIMING DIAGRAM

**PROGRAM**

/* Program for 4 Bit Ripple Counter and verify its truth table in quartus using Verilog programming.
module exp1(clk, reset, q0, q1, q2, q3);

input clk, reset; output q0, q1, q2, q3;

wire nq0, nq1, nq2, nq3;

not (nq0, q0); not (nq1, q1); not (nq2, q2); not (nq3, q3);

always @(negedge clk or posedge reset) if (reset) q0 <= 1'b0; else q0 <= nq0;

always @(negedge q0 or posedge reset) if (reset) q1 <= 1'b0; else q1 <= nq1;

always @(negedge q1 or posedge reset) if (reset) q2 <= 1'b0; else q2 <= nq2;

always @(negedge q2 or posedge reset) if (reset) q3 <= 1'b0; else q3 <= nq3;

endmodule

Developed by:PARAVEZHAA M RegisterNumber:212225220070
*/

**TRUTH TABLE**
| Clock Pulse | Q3 | Q2 | Q1 | Q0 | Decimal |
| ----------- | -- | -- | -- | -- | ------- |
| Reset       | 0  | 0  | 0  | 0  | 0       |
| 1           | 0  | 0  | 0  | 1  | 1       |
| 2           | 0  | 0  | 1  | 0  | 2       |
| 3           | 0  | 0  | 1  | 1  | 3       |
| 4           | 0  | 1  | 0  | 0  | 4       |
| 5           | 0  | 1  | 0  | 1  | 5       |
| 6           | 0  | 1  | 1  | 0  | 6       |
| 7           | 0  | 1  | 1  | 1  | 7       |
| 8           | 1  | 0  | 0  | 0  | 8       |
| 9           | 1  | 0  | 0  | 1  | 9       |
| 10          | 1  | 0  | 1  | 0  | 10      |
| 11          | 1  | 0  | 1  | 1  | 11      |
| 12          | 1  | 1  | 0  | 0  | 12      |
| 13          | 1  | 1  | 0  | 1  | 13      |
| 14          | 1  | 1  | 1  | 0  | 14      |
| 15          | 1  | 1  | 1  | 1  | 15      |
| 16 → Reset  | 0  | 0  | 0  | 0  | 0       |

**RTL LOGIC FOR 4 Bit Ripple Counter**
<img width="1727" height="847" alt="image" src="https://github.com/user-attachments/assets/96567f34-e5df-44cb-8c54-d5cab05f3263" />

**TIMING DIGRAMS FOR 4 Bit Ripple Counter**
<img width="1694" height="840" alt="image" src="https://github.com/user-attachments/assets/c3ce40c0-c0dd-4b5b-ba26-7714085e187a" />

**RESULTS**
Thus the verilog code to implement 4 Bit Ripple Counter using verilog and validating their functionality using their functional tables is done.

.



.
.
