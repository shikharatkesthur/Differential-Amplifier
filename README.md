# EXP_03
# Differential Amplifier

## Introduction
The differential amplifier is a crucial analog circuit that amplifies the difference between two input signals while rejecting common-mode signals, making it essential for applications requiring precise signal amplification and noise reduction; this experiment will investigate its key parameters, including differential-mode gain, common-mode gain, and CMRR, through practical measurements and analysis of a constructed circuit, thereby providing a hands-on understanding of its operational principles.

![image](https://github.com/user-attachments/assets/34ccea41-f74b-49fa-9f6d-67fded2e402e)

## Aim
To design a differential amplifier and perform the DC Analysis, Transient Analysis and AC Analysis and extract the required parameters for the following specifications.<br>
VDD=3.2V<br>
P<=2.8mW<br>
Vicm=1.6V<br>
Vocm=1.7V<br>
Vp=0.6V<br>

## Components Used:
1. M1 and M2 (CMOSN): These NMOS transistors form the heart of the amplifier, doing the actual amplification of the difference between the input signals.

2. VDD (2V): This DC power supply provides the energy for the circuit to operate and defines the voltage range the signals can swing within.

3. R1 and R2: These load resistors convert the amplified current from the transistors into the output voltage that we measure.

4. RSS: This tail resistor sets the bias current for the transistors, which is crucial for proper operation and influences the gain.

5. V2 and V3: These are the input voltage sources, providing the signals that the amplifier will take the difference.


## Design 
Iss = P/Vdd = 2.8mW/3.2V = 0.875mA 
Iss = 0.875mA 
ID1 = ID2 = Iss/2 = 0.875m/2 =0.4375mA 
ID = 0.4375mA 
RD = (VDD - Vocm)/ID 
RD = (3.2-1.7)/0.4375m = 3.428kohm 
RD = 3.428kohm 
Rss = Vp/Iss = 0.6/0.875mA = 685ohm 
Rss = 685ohm 

## Circuit 1 
![image](https://github.com/user-attachments/assets/2a372cf3-ff81-49f4-bfb3
ead053443023) 

## DC Analysis 
DC analysis is done to ensure whether the mosfet operates in saturation region and to 
calculate the DC operationg point of the transistor. This prevents signal distortion, which 
helps in the determination of the biasing resistors.This helps in getting a correct operating 
point despite the fluctuation in the other parameters. 
![image](https://github.com/user-attachments/assets/5a42d957-70a2-4e7b-bbb2
30347450785b) 
![image](https://github.com/user-attachments/assets/3335a21c-5fb4-421c-a8b9
8ef815a56883) 
Mosfet M1 and M2:<br> 
Length:180nm<br> 
Width:2.485um<br> 

## Transient Analysis




