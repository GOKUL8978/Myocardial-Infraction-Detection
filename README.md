# Myocardial-Infraction-Detection
## Abstract

Myocardial infarction (MI) is a cardiovascular disease (CVD), which manifests due to the
complete blockage of a coronary artery and spawns due to the rupture of atherosclerotic plaque. It
causes deprivation of oxygen to the heart muscles making them necrotic. MI is one of the leading
cause of deaths causing 9 million fatalities yearly worldwide, which is predicted to increase upto
12 million by 2030. MI progresses in three stages, namely, early MI (EMI), acute MI (AMI) and
chronic MI (CMI) characterized by its severity. With the onset of MI, the changes in
characteristics of ECG starts manifesting, therefore, it becomes imperative to perform ECG as
soon as possible. The variation in features enhances as the MI progresses, which aid cardiologists
to diagnose myocardial infarction properly. In several cases of MI, a person does not feel any
symptom before reaching to a critical condition [1]. This is because of the common symptoms of
MI progression, such as, feeling uneasy, dizziness, and light headedness are often ignored by
many people. Further, it may also happen that ECG performed in the initial stage of MI might not
be diagnostic, as the evolution of ECG variations may vary considerably from person to person.
Therefore, it becomes important to take serial electrocardiograms in certain intervals to get an
assured diagnosis.

## Softwares Used
 - **Xilinx 14.7 ISE**
 - **Modelsim**
 - **Verilog HDL**

## Block Diagram

![Block Diagram](https://i.ibb.co/b3NyV0h/BD.png "a title")

## RTL Schematic Pre-Processing Stages

![RTL Schematic](https://i.ibb.co/gm2yt19/rtl.png  "RTL")

## Pre- Procesing stages

**Band Pass Filter**
<br>
<br>
The band-pass filter reduces the influence of noise. The desirable passband maximises the QRS
energy up to a suitable frequency. The Low Pass Filter (LPF) and High Pass Filter (HPF) were
cascaded to achieve an approximately 5–15 Hz passband. LPF was used to remove the highfrequency
noise such as EMG, Power Line Interference, and T-wave interference while allowing
the low-frequency signals to be recorded. HPF was used to remove the low-frequency noise such
as the Baseline Wander
<br>
<br>
<a href="https://ibb.co/cvNZ4hV"><img src="https://i.ibb.co/LPCcVdH/BPF.png" alt="BPF" border="0"></a>
<br>
<br>
**Derivative filter**
<br>
<br>
After the filtering process, the ECG signal was differentiated i.e. the slope information was
determined using the ideal QRS complex from other waves. The low-frequency P- and T-waves
were suppressed in the derivative process to gain high frequency signals existing in the higher
slopes of the QRS complex
<br>
<br>
<a href="https://ibb.co/kxy33vB"><img src="https://i.ibb.co/Msh88QS/DF.png" alt="DF" border="0"></a>
<br>
<br>
**Squaring**
<br>
<br>
From the derivative process, the signal was squared so that all components of the signal displayed
a positive value The higher amplitudes in the signal related to the QRS complex were further
enhanced. The squaring function helps reduce the usual higher amplitudes from T-waves that
cause false detection. This process emphasises large differences from the QRS complexes.
<br>
<br>
<a href="https://ibb.co/2jpy07p"><img src="https://i.ibb.co/30P75yP/SQUARING.png" alt="SQUARING" border="0"></a>
<br>
<br>
**Integrator**
<br>
<br>
The Integration is performed to acquire information from the waveform feature with the addition
of the R wave slope. The integrated window is important in this process. The widest integrated
window must be used to match with a possible QRS complex.
<br>
<br>
<a href="https://ibb.co/RvKdgYk"><img src="https://i.ibb.co/w0qjdBF/Integrator.png" alt="Integrator" border="0"></a>
<br>
<br>
## Simulation Results for Pre-Processing Stages (MODELSIM)
<br>
<a href="https://ibb.co/S6bnFtq"><img src="https://i.ibb.co/0nTMHCP/r1.png" alt="r1" border="0"></a>
<br>
<br>
<a href="https://ibb.co/3NcbWrq"><img src="https://i.ibb.co/XstPp2g/r2.png" alt="r2" border="0"></a>





