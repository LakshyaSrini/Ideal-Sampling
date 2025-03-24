# Ideal-Sampling

AIM : 
To perform Construction and Re-contruction of impluse or ideal sampling using python.

TOOLS REQUIRED : 
Google Colab 
Python libraries: 
NumPy, Matplotlib

PROGRAM :
import numpy as np
import matplotlib.pyplot as plt
from scipy.signal import resample
fs = 100
t = np.arange(0, 1, 1/fs) 
f = 5
signal = np.sin(2 * np.pi * f * t)
plt.figure(figsize=(10, 4))
plt.plot(t, signal, label='Continuous Signal')
plt.title('Continuous Signal (fs = 100 Hz)')
plt.xlabel('Time [s]')
plt.ylabel('Amplitude')
plt.grid(True)
plt.legend()
plt.show()
t_sampled = np.arange(0, 1, 1/fs)
signal_sampled = np.sin(2 * np.pi * f * t_sampled)
plt.figure(figsize=(10, 4))
plt.plot(t, signal, label='Continuous Signal', alpha=0.7)
plt.stem(t_sampled, signal_sampled, linefmt='r-', markerfmt='ro', basefmt='r-', label='Sampled Signal (fs = 100 Hz)')
plt.title('Sampling of Continuous Signal (fs = 100 Hz)')
plt.xlabel('Time [s]')
plt.ylabel('Amplitude')
plt.grid(True)
plt.legend()
plt.show()
reconstructed_signal = resample(signal_sampled, len(t))
plt.figure(figsize=(10, 4))
plt.plot(t, reconstructed_signal, 'r--', label='Reconstructed Signal (fs = 100 Hz)')
plt.title('Reconstruction of Sampled Signal (fs = 100 Hz)')
plt.xlabel('Time [s]')
plt.ylabel('Amplitude')
plt.grid(True)
plt.legend()
plt.show()

OUTPUT WAVEFORM:
![Screenshot 2025-03-24 080217](https://github.com/user-attachments/assets/319cc06d-de82-4a96-ae77-2d2f588a2252)
![Screenshot 2025-03-24 080229](https://github.com/user-attachments/assets/28a3add0-bec9-4613-abe4-970be55b118a)
![Screenshot 2025-03-24 080241](https://github.com/user-attachments/assets/4537752d-e2bd-4786-a3b5-2cf2c2a17c7c)


RESULT : 
The Construction and Re-construction of impulse or ideal sampling using python are verified.
