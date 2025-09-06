
# Aim
Write a simple Python program for the construction and reconstruction of ideal, natural, and flattop sampling.
# Tools required
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
<img width="1191" height="650" alt="Screenshot 2025-09-06 161604" src="https://github.com/user-attachments/assets/18e0eaae-bcff-4f1e-936c-4bd06c9f8144" />
<img width="1185" height="704" alt="Screenshot 2025-09-06 161617" src="https://github.com/user-attachments/assets/b2303536-cc43-418a-ae2c-37cab82c969d" />
<img width="1185" height="704" alt="Screenshot 2025-09-06 161617" src="https://github.com/user-attachments/assets/517fac66-37ca-4d07-a11a-677789093771" />

# Results
Hence a simple Python program for the construction and reconstruction of ideal, natural, and flattop sampling.
