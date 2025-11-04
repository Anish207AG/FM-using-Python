# FM-using-Python

Aim


To implement and analyze frequency modulation (FM) using Python's NumPy and Matplotlib libraries. 

Apparatus Required

1.	Software: Python with NumPy and Matplotlib libraries
2.	Hardware: Personal Computer
  
Theory

Frequency Modulation (FM) is a method of transmitting information over a carrier wave by varying its frequency in accordance with the amplitude of the input signal (message signal). The frequency of the carrier wave is varied according to the instantaneous amplitude of the message signal. The general form of an FM signal is:



Algorithm


1.	Initialize Parameters: Set the values for carrier frequency, message frequency, sampling frequency, and frequency deviation.
2.	Generate Time Axis: Create a time vector for the signal duration.
3.	Generate Message Signal: Define the message signal as a cosine wave.
4.	Compute the Integral of the Message Signal: Calculate the integral of the message signal over time.
5.	Generate FM Signal: Apply the FM modulation formula to obtain the modulated signal.
6.	Plot the Signals: Use Matplotlib to plot the message signal, carrier signal, and modulated signal.

Program
```
import numpy as np
import matplotlib.pyplot as plt

Am=5.3
Ac=10.6
fm=434
fc=4340
fs=43400
t=np.arange(0,3/fm,1/fs)
m=Am*np.cos(2*np.pi*fm*t)
c=Ac*np.cos(2*np.pi*fc*t)
b=4.6
eFM =Ac*np.cos(2 * np.pi * fc * t + b * np.sin(2 * np.pi * fm * t))
plt.subplot(3,1,1)
plt.plot(t,m)
plt.grid()
plt.subplot(3,1,2)
plt.plot(t,c)
plt.grid()
plt.subplot(3,1,3)
plt.plot(t,eFM)
plt.grid()

plt.tight_layout()
plt.show()
```

Output Waveform

<img width="627" height="469" alt="image" src="https://github.com/user-attachments/assets/7e18f371-fe53-406b-922d-319961becac8" />

Tabular Column

<img width="1454" height="916" alt="image" src="https://github.com/user-attachments/assets/a3f96cec-1482-4c91-a4b6-b689e821401d" />

Calculation

![IMG-20251104-WA0026](https://github.com/user-attachments/assets/8de8f94a-2027-4bf5-af77-6c7c74b65bc7)

Result

The message signal, carrier signal, and frequency modulated (FM) signal will be displayed in separate plots. The modulated signal will show frequency variations corresponding to the amplitude of the message signal.
