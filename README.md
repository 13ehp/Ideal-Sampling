# Ideal, Natural, & Flat-top -Sampling
# Aim
Write a simple Python program for the construction and reconstruction of ideal, natural, and flattop sampling.

# Program

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
 plt.plot(t, signal, label='Continuous Signal', alpha=0.7)
 plt.plot(t, reconstructed_signal, 'r--', label='Reconstructed Signal (fs = 100 Hz)')
 plt.title('Reconstruction of Sampled Signal (fs = 100 Hz)')
 plt.xlabel('Time [s]')
 plt.ylabel('Amplitude')
 plt.grid(True)
 plt.legend()
 plt.show() 
# Output Waveform
<img width="1191" height="650" alt="1" src="https://github.com/user-attachments/assets/75a1c26c-1b97-4b21-a95a-48b57f961230" />
<img width="1185" height="704" alt="2" src="https://github.com/user-attachments/assets/a6c2f644-7692-4678-862f-c822cdb82fa4" />

<img width="1104" height="487" alt="3" src="https://github.com/user-attachments/assets/764a589b-152b-4b8c-80d3-07418ea41dc6" />

# Results
Hence a simple Python program for the construction and reconstruction of ideal, natural, and flattop sampling verified


