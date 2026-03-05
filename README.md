# Advanced-Telecommunications-Laboratory-3
# Experiment 11 – Sampling and Reconstruction

## Objective

The objective of this experiment is to investigate the principles of **signal sampling, signal reconstruction, and aliasing** using the **Emona Telecoms-Trainer 101 communication system trainer** and a **dual-channel oscilloscope**. 

This experiment aims to demonstrate how a continuous-time analog signal can be converted into a discrete-time signal through sampling, and how the original message signal can be recovered through reconstruction. The experiment also explores the phenomenon of aliasing, which occurs when the sampling frequency is insufficient according to the Nyquist Sampling Theorem.

Through this laboratory exercise, students gain a deeper understanding of the fundamental processes used in **digital communication systems**, **digital signal processing**, and **modern telecommunications networks**.

---

# Theory

## Analog and Digital Signals

In most real-world communication systems, signals such as speech, music, and sensor measurements are originally **analog signals**. These signals vary continuously with respect to time and amplitude. However, modern communication and processing systems often require signals to be handled digitally. 

To convert an analog signal into digital form, the signal must first undergo **sampling**, where the continuous waveform is measured at regular time intervals.

The sampled signal can be mathematically represented as:

s(t) = m(t) × p(t)

Where:

m(t) = message signal  
p(t) = periodic sampling function  
s(t) = sampled signal

The sampling function is typically a periodic pulse train that opens and closes a switch, allowing portions of the original signal to pass through at specific intervals.

Sampling is therefore a **critical bridge between analog communication systems and digital communication systems**.

---

## Natural Sampling

Natural sampling occurs when the input signal passes through a switch that is periodically controlled by a sampling pulse waveform. During the sampling interval, the input signal is allowed to pass through directly.

Because the input signal continues to vary while the switch is open, the resulting sampled waveform follows the shape of the original signal during each sampling pulse.

Important characteristics of natural sampling include:

• The sampled pulses follow the instantaneous shape of the original signal  
• The amplitude varies within each sampling pulse  
• The signal is not held constant between sampling intervals  

Natural sampling is commonly used to illustrate the fundamental principles of sampling in communication theory.

---

## Sample-and-Hold Sampling

In many digital communication systems, **sample-and-hold sampling** is used instead of natural sampling. In this method, the instantaneous amplitude of the signal is captured at the sampling instant and then held constant until the next sampling event occurs.

This produces a waveform consisting of **flat-topped pulses**, where each pulse represents the amplitude of the signal at the sampling instant.

Characteristics of sample-and-hold sampling include:

• The sampled waveform contains flat-topped pulses  
• Each sample maintains a constant amplitude during the holding period  
• The signal more closely resembles digital data representation  

Sample-and-hold circuits are widely used in **analog-to-digital converters (ADCs)**.

---

## Nyquist Sampling Theorem

The **Nyquist Sampling Theorem** states that in order to perfectly reconstruct a continuous-time signal from its samples, the sampling frequency must be at least twice the highest frequency present in the message signal.

The Nyquist condition is expressed as:

fs ≥ 2fm

Where:

fs = sampling frequency  
fm = highest frequency component of the message signal  

If the sampling frequency satisfies this condition, the original signal can theoretically be recovered without distortion.

If the sampling frequency is lower than the Nyquist rate, distortion known as **aliasing** will occur.

---

## Signal Reconstruction

Once a signal has been sampled, it can be reconstructed back into its continuous-time form by using a **reconstruction filter**, typically a **low-pass filter**.

The reconstruction filter removes the high-frequency components introduced by the sampling process and recovers the original baseband signal.

Mathematically:

m(t) = LPF{s(t)}

Where LPF represents the low-pass filter operation.

Signal reconstruction is essential in systems such as:

• Digital audio systems  
• Digital communication receivers  
• Data acquisition systems  
• Telecommunications receivers  

---

## Aliasing

Aliasing occurs when the sampling frequency is **lower than twice the highest frequency component of the signal**.

When this happens, the sampled signal becomes indistinguishable from another signal of a different frequency. As a result, incorrect frequency components appear in the reconstructed signal.

The condition for aliasing is:

fs < 2fm

When aliasing occurs:

• Frequency distortion appears in the signal  
• The reconstructed waveform differs from the original message  
• Signal information may be permanently lost  

Aliasing is a major concern in digital signal processing systems, and proper sampling frequency selection is necessary to avoid it.

---

# Materials

- Emona Telecoms-Trainer 101 (plus power pack)
- Dual-channel 20 MHz oscilloscope
- Two Emona Telecoms-Trainer 101 oscilloscope leads
- Assorted Emona Telecoms-Trainer 101 patch leads

---

# Part A – Sampling a Simple Message

## Natural Sampling Block Diagram

![Natural Sampling Block Diagram](images/PIC1.png)

Figure 1 shows the block diagram used to demonstrate the **natural sampling process** using the Telecoms-Trainer modules.

---

## Output

![Natural Sampling Output](images/PIC2.png)

The oscilloscope output shows the resulting sampled waveform obtained from the natural sampling configuration.

### Questions

**What type of sampling is this an example of?**

This is an example of **natural sampling** because the sampled pulses follow the shape of the original analog message signal during the sampling interval.

**What two features of the sampled signal confirm this?**

• The top of each pulse follows the waveform shape of the original message signal.  
• The amplitude varies continuously within the sampling window rather than remaining constant.

These characteristics indicate that the signal is being directly passed through the sampling gate without a holding mechanism.

---

## Sample-and-Hold Scheme Block Diagram

![Sample and Hold Block Diagram](images/PIC3.png)

This configuration models the **sample-and-hold sampling technique**, which is commonly used in digital systems.

---

## Output

![Sample and Hold Output](images/PIC4.png)

The oscilloscope waveform displays the output of the sample-and-hold sampling system.

### Questions

**What two features confirm that the setup models the sample-and-hold scheme?**

• The sampled waveform consists of **flat-topped pulses**.  
• Each sampled value remains constant until the next sampling instant.

These features indicate that the amplitude of the signal is captured and held momentarily, which is the defining behavior of a sample-and-hold circuit.

---

# Part B – Sampling Speech

In this section of the experiment, a **speech signal** is used as the message input instead of a simple sine wave.

Speech signals are more complex than simple sinusoidal signals because they contain a wide range of frequency components and amplitude variations. Sampling speech demonstrates how real-world signals are processed in digital communication systems.

Proper sampling of speech signals is essential in systems such as:

• Digital telephony  
• Voice-over-IP communication  
• Speech recognition systems  
• Digital audio recording  

---

## Video Output

Sampling Speech Demonstration:

https://drive.google.com/file/d/1QsZkZZK8j3FB-EJjSYh7eBU-mKezPkWP/view?usp=drive_link

https://drive.google.com/file/d/1csFihkhbXtEx4kAG__1YBwU1-oiRESU-/view?usp=drive_link

---

# Part C – Reconstructing a Sampled Message

![Reconstruction Block Diagram](images/PIC5.png)

In this part of the experiment, the sampled signal is passed through a **reconstruction filter** to recover the original message signal.

The reconstruction filter removes unwanted spectral components introduced during sampling and restores the original waveform shape.

---

## Video Outputs

Part C #15  
https://drive.google.com/file/d/1qUPEXzyx8mXMDKWrtXM2qjsQj7xSR2bh/view?usp=drive_link

Part C #16  
https://drive.google.com/file/d/1m3sWZLQn7Z5CEuWdT0qYZiDADEkKw5Vg/view?usp=drive_link

Part C #19  
https://drive.google.com/file/d/1VnD_w1dVP2FJPg1sonHtyEXRq8awluh4/view?usp=drive_link

---

# Part D – Aliasing

![Aliasing Block Diagram](images/PIC6.png)

Aliasing occurs when the sampling frequency becomes too low relative to the frequency of the message signal.

---

## Output

![Aliasing Output](images/PIC7.png)

### Questions

**What is the name of the distortion that appears when the VCO module’s Frequency Adjust control is turned far enough?**

The distortion observed is known as **aliasing distortion**.

Aliasing causes the sampled signal to appear as though it contains incorrect or lower-frequency components that were not originally present in the message signal.

---

**Given the message signal is a 2 kHz sine wave, what is the theoretical minimum sampling frequency?**

Using the Nyquist Sampling Theorem:

fs ≥ 2fm

fm = 2 kHz

Therefore:

fs ≥ 4 kHz

The theoretical minimum sampling frequency is **4 kHz**.

---

### Question

**Why is the actual minimum sampling frequency higher than the theoretical minimum?**

In practical systems, the sampling frequency must often be higher than the theoretical Nyquist rate because real systems contain **non-ideal filters, noise, and hardware limitations**.

Reconstruction filters cannot perfectly remove unwanted spectral components, and therefore engineers typically design systems with a **safety margin above the Nyquist rate** to ensure accurate signal recovery and to prevent aliasing.

---

# Conclusion

This experiment successfully demonstrated the principles of **signal sampling, reconstruction, and aliasing** using the Emona Telecoms-Trainer 101. Natural sampling and sample-and-hold sampling methods were observed and compared using oscilloscope measurements. The Nyquist Sampling Theorem was validated by analyzing the relationship between sampling frequency and signal frequency.

Additionally, the experiment illustrated the effects of aliasing when the sampling frequency falls below the required limit. These observations highlight the importance of proper sampling design in digital communication systems. Understanding these concepts is essential for engineers working in fields such as **digital communications, signal processing, audio engineering, and telecommunications systems design**.
