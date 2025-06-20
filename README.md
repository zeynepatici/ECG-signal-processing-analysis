# ECG Signal Processing and Analysis

## Project Description
This project performs comprehensive time-domain and frequency-domain analysis of electrocardiogram (ECG) signals to compare normal sinus rhythms with arrhythmic cases. We use publicly available data from PhysioNet’s MIT-BIH Arrhythmia Database
(physionet.org) (48 half-hour ECG recordings from 47 subjects) and the MIT-BIH Normal Sinus Rhythm Database (18 long-term recordings of healthy subjects). Signals are read using the Python WFDB library and then processed with NumPy, SciPy, and Matplotlib. Processing steps include filtering (high-pass to remove baseline wander and notch to remove powerline interference), computing the Fast Fourier Transform (FFT) and power spectral density, and visualizing both raw and filtered signals.

## Technologies and Libraries
- Python 3 – Programming language.
- NumPy – Numerical computing (array operations, FFT).
- SciPy – Signal processing (filter design and application).
- Matplotlib – Plotting and visualization.
- WFDB – PhysioNet database tools for reading ECG records (e.g. wfdb.rdrecord('100', pb_dir='mitdb') [wfdb-python.readthedocs.io](https://wfdb-python.readthedocs.io/en/latest/wfdb.html#:~:text=pb_dir%20%3A%20str%2C%20optional%20Option,org%2Fphysiobank%2Fdatabase%2Fmitdb%E2%80%99%20pb_dir%3D%E2%80%99mitdb%E2%80%99)).
- PhysioNet Data: We reference PhysioNet for data: MIT-BIH Arrhythmia Database [physionet.org](https://www.physionet.org/content/mitdb/1.0.0/) and MIT-BIH Normal Sinus Rhythm Database [physionet.org](https://www.physionet.org/content/nsrdb/1.0.0/)

## Results
The comparative analysis clearly shows differences between normal and arrhythmic ECGs. In the time domain, arrhythmic signals (e.g. atrial fibrillation in Record 101) have irregular beat intervals and occasional abnormal beats, whereas normal signals (e.g. Record 16265) are more periodic. In the frequency domain, normal ECGs typically exhibit a single strong peak near the heart rate frequency, while arrhythmic ECGs display additional spectral components and broader peaks due to variability. For example, Record 101’s power spectrum has extra low-frequency energy corresponding to the irregular R-R intervals. These results demonstrate that combined time and frequency analysis (using FFT, power spectra, and filtering) can help distinguish normal and pathological ECG patterns.


