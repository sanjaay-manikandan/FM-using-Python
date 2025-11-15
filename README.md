# FM-using-Python

## Aim


To implement and analyze frequency modulation (FM) using Python's NumPy and Matplotlib libraries. 

## Apparatus Required

1.	Software: Python with NumPy and Matplotlib libraries
2.	Hardware: Personal Computer
  
## Theory

Frequency Modulation (FM) is a method of transmitting information over a carrier wave by varying its frequency in accordance with the amplitude of the input signal (message signal). The frequency of the carrier wave is varied according to the instantaneous amplitude of the message signal. The general form of an FM signal is:



## Algorithm


1.	Initialize Parameters: Set the values for carrier frequency, message frequency, sampling frequency, and frequency deviation.
2.	Generate Time Axis: Create a time vector for the signal duration.
3.	Generate Message Signal: Define the message signal as a cosine wave.
4.	Compute the Integral of the Message Signal: Calculate the integral of the message signal over time.
5.	Generate FM Signal: Apply the FM modulation formula to obtain the modulated signal.
6.	Plot the Signals: Use Matplotlib to plot the message signal, carrier signal, and modulated signal.

## Program
```
import numpy as np
import matplotlib.pyplot as plt

Am=5.6
Ac=11.2
fm=448
fc=4480
fs=44800
b=5.7
t=np.arange(0,2/fm,1/fs)
wm=2*np.pi*fm
wc=2*np.pi*fc
m=Am*np.cos(wm*t)
plt.subplot(3,1,1)
plt.plot(t,m)
c=Ac*np.cos(wc*t)
plt.subplot(3,1,2)
plt.plot(t,c)
efm=Ac*np.cos((wc*t)+(b*np.sin(wm*t)))
plt.subplot(3,1,3)
plt.plot(t,efm)
plt.show()

```

## Output Waveform

<img width="726" height="533" alt="image" src="https://github.com/user-attachments/assets/aa765cfd-c563-464b-96e8-74e7340c8343" />


## Tabular Column

![WhatsApp Image 2025-11-15 at 22 27 57](https://github.com/user-attachments/assets/ef11cc15-8165-44a5-b2cc-0eedcfda506c)


## Calculation

![WhatsApp Image 2025-11-15 at 22 28 18](https://github.com/user-attachments/assets/e700554f-b870-4031-be81-d7667eaf81bf)


## Result

The message signal, carrier signal, and frequency modulated (FM) signal will be displayed in separate plots. The modulated signal will show frequency variations corresponding to the amplitude of the message signal.
