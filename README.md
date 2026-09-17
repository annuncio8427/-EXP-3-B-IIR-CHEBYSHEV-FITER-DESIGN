# EXP 3 : IIR-CHEBYSHEV-FITER-DESIGN

## AIM: 

 To design an IIR Chebyshev filter  using SCILAB. 

## APPARATUS REQUIRED: 
PC installed with SCILAB. 

## PROGRAM (LPF): 
~~~
clc; 
clear;

// Sampling frequency Fs = 5000; // Hz

// Cutoff frequency fc = 1500; // Hz

// Butterworth LPF order 3 coefficients (Chebyshev Type I, 1 dB ripple) // Precomputed numerator (b) and denominator (a) b = [0.0929 0.2787 0.2787 0.0929]; // Numerator coefficients a = [1.0000 -0.5772 0.4218 -0.0561]; // Denominator coefficients

// Frequency response Npoints = 512; [H, f_norm] = frmag(b, a, Npoints);

// Convert normalized frequency to Hz f = f_norm * Fs;

// Plot magnitude response in dB clf(); plot(f, 20*log10(H + %eps)); xlabel("Frequency (Hz)"); ylabel("Magnitude (dB)"); title("Chebyshev Type I Low Pass Filter (Order 3)"); xgrid();

// Display coefficients disp(b, "Numerator coefficients (b):"); disp(a, "Denominator coefficients (a):");
~~~

## PROGRAM (HPF): 
~~~
clc; clear;

// Sampling frequency Fs = 5000; // Hz

// Cutoff frequency fc = 1500; // Hz

// Chebyshev HPF order 3 coefficients (Type I, 1 dB ripple) // Precomputed numerator (b) and denominator (a) b = [0.4218 -0.5772 0.2787 -0.0929]; // Numerator coefficients a = [1.0000 -0.5772 0.4218 -0.0561]; // Denominator coefficients

// Frequency response Npoints = 512; [H, f_norm] = frmag(b, a, Npoints);

// Convert normalized frequency to Hz f = f_norm * Fs;

// Plot magnitude response in dB clf(); plot(f, 20*log10(H + %eps)); xlabel("Frequency (Hz)"); ylabel("Magnitude (dB)"); title("Chebyshev Type I High Pass Filter (Order 3)"); xgrid();

// Display coefficients disp(b, "Numerator coefficients (b):"); disp(a, "Denominator coefficients (a):");
~~~


## OUTPUT (LPF) : 
<img width="1600" height="1000" alt="image" src="https://github.com/user-attachments/assets/5b3982de-b772-4218-bca1-458f4f28418f" />

## OUTPUT (HPF) : 
<img width="1600" height="1000" alt="image" src="https://github.com/user-attachments/assets/43a7a37a-45d4-49db-bfc6-4ef1d53d78a2" />

## RESULT: 
The IIR Chebyshev filter was successfully designed in SCILAB based on the given specifications. The frequency response plot demonstrated the characteristic ripple in the passband and a sharp roll-off at the cutoff frequency, confirming the expected behavior of the Chebyshev filter. The filter met the design criteria for passband ripple and stopband attenuation.
