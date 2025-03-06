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

5. V2 and V3: These are the input voltage sources, providing the signals that the amplifier will take the difference of.




