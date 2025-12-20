# JKFLIPFLOP-USING-IF-ELSE

**AIM:** 

To implement  JK flipflop using verilog and validating their functionality using their functional tables

**SOFTWARE REQUIRED:**

Quartus prime

**THEORY**

**JK Flip-Flop**

JK flip-flop is the modified version of SR flip-flop. It operates with only positive clock transitions or negative clock transitions. The circuit diagram of JK flip-flop is shown in the following figure.

![image](https://github.com/naavaneetha/JKFLIPFLOP-USING-IF-ELSE/assets/154305477/a649c30b-232b-4558-b188-fd6c09845180)


This circuit has two inputs J & K and two outputs Qtt & Qtt’. The operation of JK flip-flop is similar to SR flip-flop. Here, we considered the inputs of SR flip-flop as S = J Qtt’ and R = KQtt in order to utilize the modified SR flip-flop for 4 combinations of inputs. The following table shows the state table of JK flip-flop.

![image](https://github.com/naavaneetha/JKFLIPFLOP-USING-IF-ELSE/assets/154305477/c4360742-e8a8-4937-b089-c46c0433f9a3)

 
Here, Qtt & Qt+1t+1 are present state & next state respectively. So, JK flip-flop can be used for one of these four functions such as Hold, Reset, Set & Complement of present state based on the input conditions, when positive transition of clock signal is applied. The following table shows the characteristic table of JK flip-flop. Present Inputs Present State Next State
 
![image](https://github.com/naavaneetha/JKFLIPFLOP-USING-IF-ELSE/assets/154305477/6c275261-a6d5-4c37-a3a7-1e88ca11c4cd)

By using three variable K-Map, we can get the simplified expression for next state, Qt+1t+1. Three variable K-Map for next state, Qt+1t+1 is shown in the following figure.
 
![image](https://github.com/naavaneetha/JKFLIPFLOP-USING-IF-ELSE/assets/154305477/5174f41b-0ce0-4329-a372-6d1943ea6673)

The maximum possible groupings of adjacent ones are already shown in the figure. Therefore, the simplified expression for next state Qt+1t+1 is Q(t+1)=JQ(t)′+K′Q(t)Q(t+1)=JQ(t)′+K′Q(t)

**Procedure**

1.Write the Verilog code for JK flip-flop (inputs: J, K, clk, rst; outputs: Q, Qbar) and save the file in Quartus.

2.Create a new project & add the Verilog file, set the JK flipflop module as the top-level entity.

3.Compile the project and fix any syntax or compilation errors.

4.Open Simulation Waveform Editor, add signals (J, K, clk, rst, Q, Qbar) and apply input combinations according to the JK truth table (00, 01, 10, 11) with clock pulses.

5.Run functional simulation and verify that simulated outputs (Q, Qbar) match the JK flip-flop functional table (no change, reset, set, toggle).


**PROGRAM**

Program for flipflops and verify its truth table in quartus using Verilog programming. Developed by: RegisterNumber: 25018756

```
module jkflipflop(j,k,clk,q,qbar);
input j,k,clk;
output reg q,qbar;
initial 
begin
q=1'b0;
qbar=1'b1;
end 

always @(posedge clk)
begin 
q<=(j&~q)|(~k&q);
qbar<=~q;
end
endmodule

```

**RTL LOGIC FOR FLIPFLOPS**



<img width="1907" height="955" alt="image" src="https://github.com/user-attachments/assets/4d1c8b90-f7cf-46f9-aa0d-ce948b5a0085" />


**TIMING DIGRAMS FOR FLIP FLOPS**



<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/c1ec481b-0aa7-4216-bea1-042d7fb041d2" />


**RESULTS**

Thus the OUTPUT’s of JK Flip Flop is verified by synthesizing and simulating the VERILOG code


