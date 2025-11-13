# FM

EXP NO: 4	GENERATION AND DETECTION OF FM


AIM:
To write a program for Frequency Modulation and Demodulation using SCILAB and to observe and measure the frequency deviation and the modulation index of FM.


###EQUIPMENTS REQUIRED

•	Computer with i3 Processor
•	SCI LAB

###THEORY:

Frequency modulation is a type of modulation in which the frequency of the high frequency (carrier) is varied in accordance with the instantaneous value of the modulating signal.
FREQUENCY DEVIATION f and MODULATION INDEX m f :
The frequency deviation f represents the maximum shift between the  modulatedsignal
frequency, over and under the frequency of the carrier.

We define modulation index m f the ratio between f and the modulating frequency
m= f / fm


###FREQUENCY MODULATION GENERATION:
The circuits used to generate a frequency modulation must vary the frequency of a high frequency signal (carrier) as function of the amplitude of a low frequency signal (modulating signal). In practice there are two main methods used to generate FM.
Algorithm
1.	Define Parameters:
•	Fs: Sampling frequency.
•	T: Duration of the signal.
•	Fc: Carrier frequency.
•	Fm: Frequency of the modulating signal.
•	Beta: Modulation index, which controls the extent of frequency deviation.
2.	Generate Signals:
•	Modulating signal: Sinusoidal signal used for modulation.
•	Carrier signal: The high-frequency carrier signal.
•	Modulated signal: FM modulated signal calculated by varying the carrier frequency according to the modulating signal.
3.	FM Modulation:
•	Modulated signal is obtained by modulating the carrier signal with the modulating signal.
 
4.	FM Demodulation:
•	Differentiation: Computes the derivative of the modulated signal to extract frequency variations.
•	Envelope Detection: Takes the absolute value to retrieve the envelope of the signal.
•	Low-pass Filtering: Applies a Butterworth low-pass filter to smooth the envelope and recover the original modulating signal.
5.	Visualization:
•	Plots the modulating signal, carrier signal, FM modulated signal, and demodulated signal for analysis.



###PROCEDURE

•	Refer Algorithms and write code for the experiment.
•	Open SCILAB in System
•	Type your code in New Editor
•	Save the file
•	Execute the code
•	If any Error, correct it in code and execute again
Verify the generated waveform using Tabulation and Model Waveform

###MODEL GRAPH:

<img width="512" height="365" alt="image" src="https://github.com/user-attachments/assets/acd787bd-5281-4f1b-802f-1aa39fac9189" />


###Program
```
Ac=20.4;
fc=387.5;
Am=10.2;
fm=416;
fs=50000;
t=0:1/fs:2/fm;
beta=3.6;
Em=Am*cos(2*3.14*fm*t);
subplot(3,1,1);
plot(t,Em);
xlabel("Time(s)");
ylabel("Amplitude");
title("Message Signal m(t)");
Ec=Ac*cos(2*3.14*fc*t);
subplot(3,1,2);
plot(t,Ec);
xlabel("Time(s)");
ylabel("Amplitude");
title("Carrier Signal c(t)");
Efm=Ac*cos(2*3.14*fc*t+beta*sin(2*3.14*fm*t));
subplot(3,1,3);
plot(t,Efm);
xlabel("Time(s)");
ylabel("Amplitude");
title("FM Modulated Signal (USB)");
```
###Output Waveform

![WhatsApp Image 2025-11-12 at 18 27 42_fdabe792](https://github.com/user-attachments/assets/463bb589-c968-47d2-81a8-941be0a5ef4a)

###Tabulation

![WhatsApp Image 2025-11-13 at 16 00 49_19a6b6e4](https://github.com/user-attachments/assets/3256400a-4331-47dd-8a5b-9e9482986f78)


###Calculation
![WhatsApp Image 2025-11-13 at 16 00 49_8e580d51](https://github.com/user-attachments/assets/33f3985b-82be-482b-91ed-63f8d1955431)

![WhatsApp Image 2025-11-13 at 16 00 50_44f9b003](https://github.com/user-attachments/assets/58d6f3be-7a9b-480b-9f39-c27793f84516)

Frequency Deviation Practical = 300

Modulation Index Practical	= 0.050847

Modulation Index Theoretical	=0.758


###RESULT:

Thus, the frequency modulation and demodulation is successfully done and the output is experimentally verified.


