# Experiment--05-Implementation-of-flipflops-using-verilog
### AIM: To implement all the flipflops using verilog and validating their functionality using their functional tables
### HARDWARE REQUIRED:  – PC, Cyclone II , USB flasher
### SOFTWARE REQUIRED:   Quartus prime
### THEORY 
SR Flip-Flop
SR flip-flop operates with only positive clock transitions or negative clock transitions. Whereas, SR latch operates with enable signal. The circuit diagram of SR flip-flop is shown in the following figure.
![Screenshot 2023-11-26 165020](https://github.com/MabbuAdarsh/Experiment--05-Implementation-of-flipflops-using-verilog/assets/149365583/e4867286-2ac8-41bf-aecf-5c3b3dac6035)


 
This circuit has two inputs S & R and two outputs Qtt & Qtt’. The operation of SR flipflop is similar to SR Latch. But, this flip-flop affects the outputs only when positive transition of the clock signal is applied instead of active enable.
The following table shows the state table of SR flip-flop.

![Screenshot 2023-11-26 164934](https://github.com/MabbuAdarsh/Experiment--05-Implementation-of-flipflops-using-verilog/assets/149365583/25097e21-aa5f-47f4-a58d-5025961a55f1)



Here, Qtt & Qt+1t+1 are present state & next state respectively. So, SR flip-flop can be used for one of these three functions such as Hold, Reset & Set based on the input conditions, when positive transition of clock signal is applied. The following table shows the characteristic table of SR flip-flop.
Present Inputs	Present State	Next State

![Screenshot 2023-11-26 164713](https://github.com/MabbuAdarsh/Experiment--05-Implementation-of-flipflops-using-verilog/assets/149365583/89d6ea61-e09d-43a1-8b44-5c65b0523f61)


By using three variable K-Map, we can get the simplified expression for next state, Qt+1t+1. The three variable K-Map for next state, Qt+1t+1 is shown in the following figure.

![download](https://github.com/MabbuAdarsh/Experiment--05-Implementation-of-flipflops-using-verilog/assets/149365583/1da024f4-6dab-471d-92d3-b5098677d3a7)
 
The maximum possible grouping
s of adjacent ones are already shown in the figure. Therefore, the simplified expression for next state Qt+1t+1 is
Q(t+1)=S+R′Q(t)Q(t+1)=S+R′Q(t)


### D Flip-Flop
D flip-flop operates with only positive clock transitions or negative clock transitions. Whereas, D latch operates with enable signal. That means, the output of D flip-flop is insensitive to the changes in the input, D except for active transition of the clock signal. The circuit diagram of D flip-flop is shown in the following figure.
 
This circuit has single input D and two outputs Qtt & Qtt’. The operation of D flip-flop is similar to D Latch. But, this flip-flop affects the outputs only when positive transition of the clock signal is applied instead of active enable.
The following table shows the state table of D flip-flop.


![Screenshot 2023-11-26 204555](https://github.com/MabbuAdarsh/Experiment--05-Implementation-of-flipflops-using-verilog/assets/149365583/4d631884-a460-4369-96b0-746904f17426)


Therefore, D flip-flop always Hold the information, which is available on data input, D of earlier positive transition of clock signal. From the above state table, we can directly write the next state equation as
Qt+1t+1 = D

![Screenshot 2023-11-26 204625](https://github.com/MabbuAdarsh/Experiment--05-Implementation-of-flipflops-using-verilog/assets/149365583/7139dd40-e7c0-4735-bc9b-85bbb58a210d)


![Screenshot 2023-11-26 204800](https://github.com/MabbuAdarsh/Experiment--05-Implementation-of-flipflops-using-verilog/assets/149365583/65c6607d-42eb-4910-a9e3-6d9a266be461)

Next state of D flip-flop is always equal to data input, D for every positive transition of the clock signal. Hence, D flip-flops can be used in registers, shift registers and some of the counters.


### JK Flip-Flop
JK flip-flop is the modified version of SR flip-flop. It operates with only positive clock transitions or negative clock transitions. The circuit diagram of JK flip-flop is shown in the following figure.
![Screenshot 2023-11-22 142451](https://github.com/MabbuAdarsh/Experiment--05-Implementation-of-flipflops-using-verilog/assets/149365583/81bb7766-c4de-407a-921b-6ba69551faa8)

 
This circuit has two inputs J & K and two outputs Qtt & Qtt’. The operation of JK flip-flop is similar to SR flip-flop. Here, we considered the inputs of SR flip-flop as S = J Qtt’ and R = KQtt in order to utilize the modified SR flip-flop for 4 combinations of inputs.
The following table shows the state table of JK flip-flop.

![Screenshot 2023-11-26 210428](https://github.com/MabbuAdarsh/Experiment--05-Implementation-of-flipflops-using-verilog/assets/149365583/1b697bbd-0346-4acd-a78f-5986bbba2a95)



Here, Qtt & Qt+1t+1 are present state & next state respectively. So, JK flip-flop can be used for one of these four functions such as Hold, Reset, Set & Complement of present state based on the input conditions, when positive transition of clock signal is applied. The following table shows the characteristic table of JK flip-flop.
Present Inputs	Present State	Next State

![Screenshot 2023-11-22 143128](https://github.com/MabbuAdarsh/Experiment--05-Implementation-of-flipflops-using-verilog/assets/149365583/0f7b4231-a019-436d-ba0e-439e9982912d)



By using three variable K-Map, we can get the simplified expression for next state, Qt+1t+1. Three variable K-Map for next state, Qt+1t+1 is shown in the following figure.

 ![download](https://github.com/MabbuAdarsh/Experiment--05-Implementation-of-flipflops-using-verilog/assets/149365583/bf1c8ed2-a328-4538-be30-3edc9bc60bf0)

 

The maximum possible groupings of adjacent ones are already shown in the figure. Therefore, the simplified expression for next state Qt+1t+1 is
Q(t+1)=JQ(t)′+K′Q(t)Q(t+1)=JQ(t)′+K′Q(t)



### T Flip-Flop
T flip-flop is the simplified version of JK flip-flop. It is obtained by connecting the same input ‘T’ to both inputs of JK flip-flop. It operates with only positive clock transitions or negative clock transitions. The circuit diagram of T flip-flop is shown in the following figure.

![Screenshot 2023-11-26 170739](https://github.com/MabbuAdarsh/Experiment--05-Implementation-of-flipflops-using-verilog/assets/149365583/2dbccc1c-a405-4445-9eb6-17976658d0f3)




This circuit has single input T and two outputs Qtt & Qtt’. The operation of T flip-flop is same as that of JK flip-flop. Here, we considered the inputs of JK flip-flop as J = T and K = T in order to utilize the modified JK flip-flop for 2 combinations of inputs. So, we eliminated the other two combinations of J & K, for which those two values are complement to each other in T flip-flop.
The following table shows the state table of T flip-flop.


![Screenshot 2023-11-26 170613](https://github.com/MabbuAdarsh/Experiment--05-Implementation-of-flipflops-using-verilog/assets/149365583/8f6ba664-424a-4d8a-b527-afc4bc35a229)

Here, Qtt & Qt+1t+1 are present state & next state respectively. So, T flip-flop can be used for one of these two functions such as Hold, & Complement of present state based on the input conditions, when positive transition of clock signal is applied. The following table shows the characteristic table of T flip-flop.
Inputs	Present State	Next State

![Screenshot 2023-11-26 204555](https://github.com/MabbuAdarsh/Experiment--05-Implementation-of-flipflops-using-verilog/assets/149365583/6f5f8282-9d13-4f5a-8c78-9b02281d4a10)

![download](https://github.com/MabbuAdarsh/Experiment--05-Implementation-of-flipflops-using-verilog/assets/149365583/40d38bab-76f3-4409-8a09-ae394c9e016e)

From the above characteristic table, we can directly write the next state equation as
Q(t+1)=T′Q(t)+TQ(t)′
⇒Q(t+1)=T⊕Q(t)

### Procedure
/* write all the steps invloved */



### PROGRAM 
/*
Program for flipflops  and verify its truth table in quartus using Verilog programming.
Developed by: 
RegisterNumber:  
*/






### RTL LOGIC FOR FLIPFLOPS 









### TIMING DIGRAMS FOR FLIP FLOPS 








### RESULTS 
