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

## Procedure:

1.Open LTspice and import the tsmc018.lib file before building up the circuit.<br>
2.Make sure that the file must be in the same folder as the experiment file<br>
3.Use the (.t) option in the toolbar and type .lib tsmc018.lib to import the library of that file<br>
4.Select the Rd and Rs with accurate Values and Select NMOS4<br>
5.Rename the MOSFET's as CMOSN<br>
6.DC Analysis :To perform the DC analsyis select the Configure Analysis Option in toolbar and select 'DC op pnt'. Find the Id by adjusting the length and width of the CMOSN.<br>
7.Transient Analysis: To perform the Transient analsyis select the Configure Analysis Option in toolbar and select 'Transient' set the operating point such as Stop time 5ms find the Gain by finding out the Vin and Vout from the waveform.<br>
8.AC Analysis: To perform the AC analsyis we must select the Configure Analysis Option in toolbar and select AC analysis select the operating points like Type of sweep as decade, Number of points per decade as 20, Start and Stop Frequency from 0.1 to 1T Hz.<br>

## Design 
Iss = P/Vdd = 2.8mW/3.2V = 0.875mA<br>
Iss = 0.875mA<br>

ID1 = ID2 = Iss/2 = 0.875m/2 =0.4375mA<br>
ID = 0.4375mA <br>

RD = (VDD - Vocm)/ID<br> 
RD = (3.2-1.7)/0.4375m = 3.428kohm<br> 
RD = 3.428kohm<br>

Rss = Vp/Iss = 0.6/0.875mA = 685ohm<br>
Rss = 685ohm<br>

# Circuit 1
Resistor Connected 

![image](https://github.com/user-attachments/assets/df58dab7-d84a-431f-a8d5-20c80acad852)

## DC Analysis
After setting the voltage source as specified we must find the appropriate W and L values for CMOSN

![image](https://github.com/user-attachments/assets/8e196874-687b-43c2-a1ab-7506b6837f9a)

![image](https://github.com/user-attachments/assets/f91fc071-6409-4684-89d3-c4d7ed889d00)

Mosfet M1 and M2:<br> 

Length:180nm<br> 
Width:2.485um<br> 
Id=0.4375mA<br>
Iss=0.875mA<br>

## Transient Analysis
For M1 and M2:<br>
Set DC Offset as 1.6V and Amplitude as 50m and Frequency as 1K Hz<br>

![image](https://github.com/user-attachments/assets/0b174dc1-b294-46d6-9b6a-cb65f571b98f)

![image](https://github.com/user-attachments/assets/c29ba443-fa52-4cb3-9fc4-c1644e19a115)

The above two waveforms are the Vocm and Vicm. The green waveform represents the output waveform and the blue waveform represents the input waveform.

![image](https://github.com/user-attachments/assets/7ce7a76a-b716-48b4-a443-966a8220a0e4)

Voltage gain,<br> 
AV = Voutp-p/Vinp-p<br>
AV=(1.76-1.63)/(1.65-1.55)<br>
AV=1.4<br>

## AC Analysis

To perform AC analysis we must set the operating point first they are shown below

Type of sweep as decade<br>
Number of points per decade as 20<br>
Start Frequency as 0.1 Hz<br>
Stop Frequency as 1T Hz<br>

![image](https://github.com/user-attachments/assets/f122c9eb-364f-4c54-b0c9-f85c70f20005)

Gain in dB= 20log(AV)<br>
=20log(1.4)<br>
=2.922dB<br>

# Circuit 2 
Replace the resistor with current source,Iss = 0.875mA.

![image](https://github.com/user-attachments/assets/facc411e-81a5-4b29-9e78-1a0f226f541a)


## DC Analysis 
DC analysis is done to ensure whether the mosfet operates in saturation region and to calculate the DC operationg point of the transistor. This prevents signal distortion, which helps in the determination of the biasing resistors.This helps in getting a correct operating point despite the fluctuation in the other parameters. 

![image](https://github.com/user-attachments/assets/dad7954b-8500-4647-b908-90415a186668)


![image](https://github.com/user-attachments/assets/57d2f4e1-bb62-430e-97f9-5ce330d91066)

Mosfet M1 and M2:<br> 

Length:180nm<br> 
Width:2.485um<br> 
Id=0.4375mA<br>
Iss=0.875mA<br>



## Transient Analysis:
For M1 :<br>
Set DC Offset as 1.6V and Amplitude as 50m and Frequency as 1K Hz<br>

For M2: <br>
Set DC Offset as 1.6V and Amplitude as -50m and Frequency as 1K Hz<br>

![Screenshot 2025-03-06 232710](https://github.com/user-attachments/assets/972d4ff3-3881-4fb4-bbc7-c5bc0a8214d1)

![Screenshot 2025-03-06 232826](https://github.com/user-attachments/assets/dfd01936-f252-4321-ba8c-c2819ebff7d6)

The above two waveforms are the Vocm and Vicm. The green waveform represents the output waveform and the blue waveform represents the input waveform.

![Screenshot 2025-03-06 233212](https://github.com/user-attachments/assets/bd0f8a56-ca2e-4652-ac05-fbd61e764e42)

Voltage gain,<br>
     AV = Voutp-p/Vinp-p<br>
     AV=(1.87-1.54)/(1.65-1.55)<br>
     AV=3.3<br>


## AC Analysis:

![Screenshot 2025-03-06 233536](https://github.com/user-attachments/assets/3bb0c18e-2808-46ee-a440-a044eb93b214)

Gain in dB= 20log(AV)<br>
=20log(3.3)<br>
=10.37dB<br>

# Circuit 3
Replace the current source with Mosfet M3.

![image](https://github.com/user-attachments/assets/e50b05d9-8ae6-4e3e-b34f-299184cc510b)

## DC Analysis:
DC analysis is done to ensure whether the mosfet operates in saturation region and to calculate the DC operationg point of the transistor. This prevents signal distortion, which helps in the determination of the biasing resistors.This helps in getting a correct operating point despite the fluctuation in the other parameters. 

![image](https://github.com/user-attachments/assets/925bbd97-4c65-471e-8252-7a978721d57b)

Mosfet M1 and M2:<br> 

Length:180nm<br> 
Width:2.485um<br> 

Mosfet M3:<br> 

Length:180nm<br> 
Width:2.53um<br> 

## Transient Analysis:
To perform AC analysis we must set the operating point first they are shown below

Type of sweep as decade<br>
Number of points per decade as 20<br>
Start Frequency as 0.1 Hz<br>
Stop Frequency as 1T Hz<br>
To perform Transient Analysis we must set the stop time for 5ms and the appropriate waveform is given by,

![image](https://github.com/user-attachments/assets/63bfe10e-dfe2-47ac-9c36-39ab9674010d)

Gain = (Vout)/(Vin)<br>
= (0.013875)/(0.04864)<br>
= 0.285259<br>

## AC Analysis

![image](https://github.com/user-attachments/assets/04a14ae9-b803-4553-abe1-8d18317eaaae

## Inference

Differential amplifiers are preferred because they offer *high stability, precision, and noise rejection. They ensure **consistent gain* and work well even with power or temperature changes. Their ability to reject *common-mode noise* makes them essential in *op-amps and signal processing* applications.










