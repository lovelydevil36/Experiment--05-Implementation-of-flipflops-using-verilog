# Experiment-05 Implementation of flipflops using verilog


## AIM:
To implement all the flipflops using verilog and validating their functionality using their functional tables

## HARDWARE REQUIRED: –

PC, Cyclone II , USB flasher

## SOFTWARE REQUIRED:

Quartus prime

## THEORY

SR Flip-Flop SR flip-flop operates with only positive clock transitions or negative clock transitions. Whereas, SR latch operates with enable signal. The circuit diagram of SR flip-flop is shown in the following figure.

![image](https://github.com/lovelydevil36/Experiment--05-Implementation-of-flipflops-using-verilog/assets/123564624/5cd67741-0569-45ef-a8d5-3efc2835136f)


This circuit has two inputs S & R and two outputs Qtt & Qtt’. The operation of SR flipflop is similar to SR Latch. But, this flip-flop affects the outputs only when positive transition of the clock signal is applied instead of active enable. The following table shows the state table of SR flip-flop.

![image](https://github.com/lovelydevil36/Experiment--05-Implementation-of-flipflops-using-verilog/assets/123564624/e3d2e971-af44-436d-be1a-dbf062746f3d)

Here, Qtt & Qt+1t+1 are present state & next state respectively. So, SR flip-flop can be used for one of these three functions such as Hold, Reset & Set based on the input conditions, when positive transition of clock signal is applied. The following table shows the characteristic table of SR flip-flop. Present Inputs Present State Next State

![image](https://github.com/lovelydevil36/Experiment--05-Implementation-of-flipflops-using-verilog/assets/123564624/8f397e3a-94d3-4d72-9fbe-5af9383dcdfe)


By using three variable K-Map, we can get the simplified expression for next state, Qt+1t+1. The three variable K-Map for next state, Qt+1t+1 is shown in the following figure.

![image](https://github.com/lovelydevil36/Experiment--05-Implementation-of-flipflops-using-verilog/assets/123564624/2d4f1768-7565-4a18-bc08-261b991af8f7)


The maximum possible groupings of adjacent ones are already shown in the figure. Therefore, the simplified expression for next state Qt+1t+1 is Q(t+1)=S+R′Q(t)Q(t+1)=S+R′Q(t)

## D Flip-Flop
D flip-flop operates with only positive clock transitions or negative clock transitions. Whereas, D latch operates with enable signal. That means, the output of D flip-flop is insensitive to the changes in the input, D except for active transition of the clock signal. The circuit diagram of D flip-flop is shown in the following figure.

This circuit has single input D and two outputs Qtt & Qtt’. The operation of D flip-flop is similar to D Latch. But, this flip-flop affects the outputs only when positive transition of the clock signal is applied instead of active enable. The following table shows ![image](https://github.com/lovelydevil36/Experiment--05-Implementation-of-flipflops-using-verilog/assets/123564624/a9cba5ac-4254-4348-a007-4dbeb8880388)
the state table of D flip-flop.

![image](https://github.com/lovelydevil36/Experiment--05-Implementation-of-flipflops-using-verilog/assets/123564624/0cefdd9d-a14e-4010-9d6f-4edff95f3d93)


Therefore, D flip-flop always Hold the information, which is available on data input, D of earlier positive transition of clock signal. From the above state table, we can directly write the next state equation as Qt+1t+1 = D

![image](https://github.com/lovelydevil36/Experiment--05-Implementation-of-flipflops-using-verilog/assets/123564624/5e8d88b8-6562-48a8-8687-bd941948e44e)



Next state of D flip-flop is always equal to data input, D for every positive transition of the clock signal. Hence, D flip-flops can be used in registers, shift registers and some of the counters.

## JK Flip-Flop
JK flip-flop is the modified version of SR flip-flop. It operates with only positive clock transitions or negative clock transitions. The circuit diagram of JK flip-flop is shown in the following figure. 

![image](https://github.com/lovelydevil36/Experiment--05-Implementation-of-flipflops-using-verilog/assets/123564624/c0e23331-b51a-4a73-999f-39b686c98ba2)



This circuit has two inputs J & K and two outputs Qtt & Qtt’. The operation of JK flip-flop is similar to SR flip-flop. Here, we considered the inputs of SR flip-flop as S = J Qtt’ and R = KQtt in order to utilize the modified SR flip-flop for 4 combinations of inputs. The following table shows the state table of JK flip-flop.

![image](https://github.com/lovelydevil36/Experiment--05-Implementation-of-flipflops-using-verilog/assets/123564624/f449a3dd-86fc-45f3-b5f9-c5a21976a151)


Here, Qtt & Qt+1t+1 are present state & next state respectively. So, JK flip-flop can be used for one of these four functions such as Hold, Reset, Set & Complement of present state based on the input conditions, when positive transition of clock signal is applied. The following table shows the characteristic table of JK flip-flop. Present Inputs Present State Next State

![image](https://github.com/lovelydevil36/Experiment--05-Implementation-of-flipflops-using-verilog/assets/123564624/ad1251ab-613b-4aec-8645-bd16cec15ab8)


By using three variable K-Map, we can get the simplified expression for next state, Qt+1t+1. Three variable K-Map for next state, Qt+1t+1 is shown in the following figure.

![image](https://github.com/lovelydevil36/Experiment--05-Implementation-of-flipflops-using-verilog/assets/123564624/55cf8a7e-6fe4-4d2e-9ef0-c2b7cca897a7)


The maximum possible groupings of adjacent ones are already shown in the figure. Therefore, the simplified expression for next state Qt+1t+1 is Q(t+1)=JQ(t)′+K′Q(t)Q(t+1)=JQ(t)′+K′Q(t)

## T Flip-Flop

T flip-flop is the simplified version of JK flip-flop. It is obtained by connecting the same input ‘T’ to both inputs of JK flip-flop. It operates with only positive clock transitions or negative clock transitions. The circuit diagram of T flip-flop is shown in the following figure.

![image](https://github.com/lovelydevil36/Experiment--05-Implementation-of-flipflops-using-verilog/assets/123564624/8ef6b03c-a912-4569-8bf2-c4c1d9b13fdc)

This circuit has single input T and two outputs Qtt & Qtt’. The operation of T flip-flop is same as that of JK flip-flop. Here, we considered the inputs of JK flip-flop as J = T and K = T in order to utilize the modified JK flip-flop for 2 combinations of inputs. So, we eliminated the other two combinations of J & K, for which those two values are complement to each other in T flip-flop. The following table shows the state table of T flip-flop.

Here, Qtt & Qt+1t+1 are present state & next state respectively. So, T flip-flop can be used for one of these two functions such as Hold, & Complement of present state based on the input conditions, when positive transition of clock signal is applied. The following table shows the characteristic table of T flip-flop. Inputs Present State Next State

![image](https://github.com/lovelydevil36/Experiment--05-Implementation-of-flipflops-using-verilog/assets/123564624/eecd0574-aa89-4f8e-8889-615994fe4217)


From the above characteristic table, we can directly write the next state equation as Q(t+1)=T′Q(t)+TQ(t)′ ⇒Q(t+1)=T⊕Q(t)

## Procedure:

1.Create a project with required entities.

2.Create a module along with respective file name.

3.Run the respective programs for the given boolean equations.

4.Run the module and get the respective RTL outputs.

5.Create university program(VWF) for getting timing diagram.

6.Give the respective inputs for timing diagram and obtain the results.

## PROGRAM :

Program for flipflops and verify its truth table in quartus using Verilog programming.

Developed by: Abdul hameed.H

RegisterNumber: 212222050001

## SR Flipflop
```
module flipflop(s,r,Q,Qbar,clk);
input s,r,clk;
output reg Q,Qbar;
initial Q=0;
initial Qbar=1;
always @(posedge clk)
begin
Q=s|(Q&(~r));
Qbar=r|(Qbar&(~s));
end
endmodule
```
## JK Flipflop
```
module jkflipflop(k,clk,j,Q,Qbar);
input k,clk,j;
output reg Q;
output reg Qbar;
initial Q=0;
initial Qbar=1;
always @(posedge clk)
begin
Q=((~Q)&j)|(Q&~k);
Qbar=(~Qbar&k)|(Qbar&~j);
end
endmodule
```
## RTL LOGIC FOR SR FLIPFLOPS

![image](https://github.com/lovelydevil36/Experiment--05-Implementation-of-flipflops-using-verilog/assets/123564624/dcf85ec8-e969-49d9-9a74-030a039d0c0e)


## RTL LOGIC FOR JK FLIPFLOPS

![image](https://github.com/lovelydevil36/Experiment--05-Implementation-of-flipflops-using-verilog/assets/123564624/47e23580-2148-482a-b502-2752965f5d8c)


## Waveform Output For SR:

![image](https://github.com/lovelydevil36/Experiment--05-Implementation-of-flipflops-using-verilog/assets/123564624/bb6ef0a7-dfac-4146-b62f-4059a3b9a781)



## Waveform Output For JK:

![image](https://github.com/lovelydevil36/Experiment--05-Implementation-of-flipflops-using-verilog/assets/123564624/028e5853-05df-40eb-a802-cc6988b247b6)



## Truth table For SR:

![image](https://github.com/lovelydevil36/Experiment--05-Implementation-of-flipflops-using-verilog/assets/123564624/7df83287-70b2-4139-b692-2f0519ff1844)


## Truth table For JK:

![image](https://github.com/lovelydevil36/Experiment--05-Implementation-of-flipflops-using-verilog/assets/123564624/299488f2-d1aa-4ae8-a69b-95a788114278)


## RESULTS:-

Thus the flipflops circuits are designed and the truth tables is verified using quartus software.
