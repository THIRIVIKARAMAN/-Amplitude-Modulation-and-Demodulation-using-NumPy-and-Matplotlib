 # -Amplitude-Modulation-and-Demodulation-using-NumPy-and-Matplotlib

__Aim__: 

To implement and analyze amplitude modulation (AM) using Python's NumPy and Matplotlib libraries. 

__Apparatus Required__: 

Software: Python with NumPy and Matplotlib libraries 
Hardware: Personal Computer 

__Theory__: 

Amplitude Modulation (AM) is a technique used in electronic communication, primarily for transmitting 
information via a radio carrier wave. In AM, the amplitude of the carrier wave is varied in proportion to that of 
the message signal. The general form of an AM signal is: 


__Algorithm__:
1. Initialize Parameters: Set the values for carrier frequency, message frequency, and sampling frequency. 
2. Generate Time Axis: Create a time vector for the signal duration. 
3. Generate Message Signal: Define the message signal as a cosine wave. 
4. Generate Carrier Signal: Define the carrier signal as a cosine wave. 
5. Modulate Signal: Apply the AM formula to obtain the modulated signal. 
6. Plot the Signals: Use Matplotlib to plot the message signal, carrier signal, and modulated signal.

PROGRAM :
```
import numpy as np 
import matplotlib.pyplot as plt 
# Given parameters 
Ac = 33.2 # Carrier amplitude 
fc = 7800  # Carrier frequency in Hz 
Am = 16.6# Message signal amplitude 
fm = 780 # Message signal frequency in Hz 
fs = 78000  # Sampling frequency 
t = np.arange(0, 2/fm, 1/fs)  # Time vector 
# Message signal (modulating signal) 
Em = Am * np.sin(2 * np.pi * fm * t) 
# Carrier signal 
Ec = Ac * np.sin(2 * np.pi * fc * t) 
Eam = (Ac + Am * np.sin(2 * np.pi * fm * t)) * np.sin(2 * np.pi * fc * t) 
# Plot the signals 
plt.figure(figsize=(10, 6)) 
plt.subplot(3, 1, 1) 
plt.plot(t, Em) 
plt.grid() 
plt.subplot(3, 1, 2) 
plt.plot(t, Ec) 
plt.grid() 
plt.subplot(3, 1, 3) 
plt.plot(t, Eam) 
plt.grid() 
plt.tight_layout() 
plt.show()
```


 TABULATION:

![WhatsApp Image 2025-11-22 at 08 18 30_bf77d59b](https://github.com/user-attachments/assets/f99e14c9-3149-4d9c-a794-59258c877a7f)




Calculation
1.	ma (Theory) = am/ac =0.5
2.	ma(Practical) = (Emax-Emin)/(Emax+Emin) =0.5
![WhatsApp Image 2025-11-22 at 08 18 30_e2b07d9f](https://github.com/user-attachments/assets/701bd121-4043-4f78-9024-976e88e3a15f)

 __Output__:
<img width="989" height="590" alt="image" src="https://github.com/user-attachments/assets/a9643cf7-910c-4839-9d00-05fdf6753d96" />


 __Result__:
The message signal, carrier signal, and amplitude modulated (AM) signal will be displayed in separate plots. Thus, AM is implemented using numPy and Matplotlib.

