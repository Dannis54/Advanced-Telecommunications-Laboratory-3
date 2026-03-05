# EXPERIMENT 12 – Pulse Code Modulation (PCM) Encoding

## Introduction

Pulse Code Modulation (PCM) is one of the most widely used digital communication techniques for converting analog signals into digital form. In PCM systems, an analog signal such as speech, music, or sensor output is first sampled at regular intervals. Each sampled value is then quantized into a discrete level and represented by a binary code. This digital representation allows the signal to be transmitted, processed, and stored more efficiently in modern communication systems.

PCM plays a critical role in many technologies such as digital telephony, audio recording systems, satellite communications, and digital networks. By representing signals as binary numbers, PCM enables reliable transmission over noisy channels and compatibility with digital processing equipment.

In this experiment, the PCM Encoder module of the Emona Telecoms-Trainer 101 is used to observe how analog voltages are converted into digital binary codes. The experiment begins with a fixed DC voltage to understand the encoder's basic behavior. It then progresses to variable voltages and continuously changing signals to demonstrate quantization effects and digital data generation.

The oscilloscope is used throughout the experiment to observe the encoder input signal and the resulting digital data output.

---

# MATERIALS

• Emona Telecoms-Trainer 101 (with power supply)  
• Dual-channel oscilloscope (20 MHz or higher)  
• Two oscilloscope leads  
• Assorted Emona patch cords  
• PCM Encoder module  
• Variable DC Voltage module  

---

# PART A – Introduction to PCM Encoding using a Static DC Voltage

## PCM Encoding Block Diagram

![PCM Encoding Block Diagram](12pic1.png)

*Figure 1. PCM encoding block diagram.*

In this part of the experiment, a constant DC voltage is applied to the input of the PCM Encoder module. Even though the input voltage remains steady, the encoder continuously samples the signal and produces a digital code corresponding to the quantization level nearest to the input voltage.

The PCM encoder operates by periodically sampling the analog input signal and assigning each sampled value to a discrete quantization level. Each quantization level corresponds to a unique binary code which is then transmitted as digital data.

---

## Output Observation

![PCM Encoder Output](12pic2.png)

*Figure 2. PCM encoder output waveform.*

### Questions

**Why does the code change even though the input voltage is steady?**

Although the input voltage remains constant, the PCM encoder continues to sample the signal at a fixed sampling frequency. Because of small internal noise, quantization boundaries, and timing variations, the sampled value may occasionally fall into adjacent quantization levels. As a result, the digital code may slightly fluctuate between nearby binary values even when the analog input voltage is constant.

**Why does the PCM Encoder module output this code for 0V DC and not 00000000?**

In many PCM encoder designs, the midpoint of the quantization range corresponds to zero volts. Instead of assigning the binary value `00000000` to zero voltage, the encoder often uses a mid-range binary value to represent zero. This is done so that both positive and negative signal variations can be represented symmetrically around the midpoint of the digital range.

---

![Additional PCM Output Observation](12pic3.png)

*Figure 3. Additional PCM encoder observation.*

---

# PART B – PCM Encoding of a Variable DC Voltage

## Output Observation

![Variable DCV Output](12pic4.png)

*Figure 4. PCM output for a changing DC voltage.*

---

## Block Diagram

![PCM Encoding of Variable DC Voltage](12pic5.png)

*Figure 5. PCM encoding of the variable DC voltage.*

In this part of the experiment, the Variable DC Voltage module is used as the input signal for the PCM Encoder. Unlike the previous section where the voltage remained fixed, the input voltage is now gradually changed. As the voltage changes, the PCM encoder produces different binary codes corresponding to the quantization levels that best approximate the input voltage.

Each time the input voltage crosses a quantization boundary, the output binary number changes to represent the new voltage level.

---

### Questions

**What happens to the Variable DCV module’s output?**

The output voltage from the Variable DCV module increases or decreases smoothly as the control knob is adjusted. This changing analog voltage represents a continuous signal that the PCM encoder must convert into discrete digital values.

---

**In what way does the binary number that the PCM Encoder module outputs change?**

As the input voltage increases, the binary output of the PCM encoder increases step-by-step according to the quantization levels. Each binary value represents a particular voltage range. When the input voltage crosses the boundary between two quantization levels, the digital code changes to the next corresponding binary value.

---

**It’s possible that you were unable to obtain 111111 on the PCM Encoder module’s output. Explain why.**

This may occur because the maximum output voltage of the Variable DC module might not reach the upper limit of the PCM encoder’s input range. If the encoder requires a slightly higher voltage to reach the highest quantization level, the maximum binary value cannot be generated.

---

**Devise a method to obtain a variable DC voltage that can reach the encoder limits.**

One possible solution is to amplify the variable DC signal using an amplifier or buffer module before feeding it into the PCM encoder. Another method is to combine the variable voltage with an offset voltage so that the signal range extends further into the encoder’s allowable input range.


---

### Questions

**What happens to the binary number as the negative input voltage increases?**

As the input voltage becomes more negative, the binary output decreases step-by-step. Each decrease represents the signal moving to a lower quantization level within the encoder’s voltage range.

---

**Based on the table, what is the maximum allowable peak-to-peak amplitude for an AC signal at the encoder input?**

The maximum allowable peak-to-peak amplitude corresponds to the full voltage range that the PCM encoder can accept without exceeding its quantization limits. If the encoder input range is ±2.5 V, the maximum peak-to-peak signal amplitude would be approximately:

```
Vpp = 5 V
```

Any signal exceeding this range would cause clipping or incorrect digital representation.

---

# PART C – Quantisation

Quantization is the process of mapping a continuous range of analog voltage values into a finite number of discrete levels. Since the analog input signal can take any value within its range, some rounding or approximation must occur when assigning the signal to the nearest quantization level.

This approximation introduces a small difference between the actual sampled voltage and the quantized level.

---

### Questions

**What is the name for the difference between a sampled voltage and its closest quantisation level?**

This difference is called **quantization error** or **quantization noise**.

---

**To reduce quantisation error, which is better?**

The best solution is:

**More quantisation levels between ±2.5 V**

Increasing the number of quantization levels allows the analog signal to be represented more accurately, reducing the magnitude of quantization error.

---

# PART D – PCM Encoding of Continuously Changing Voltages

![Continuously Changing Voltage Input](12pic6.png)

*Figure 6. PCM encoding of a continuously changing analog signal.*

In this section, a continuously varying signal is applied to the PCM encoder input. As the input voltage changes over time, the encoder samples the signal and produces a corresponding sequence of binary codes.

The output digital data therefore represents the changing waveform of the original analog signal.

---

### Questions

**Why does the DATA change continuously?**

The DATA output changes continuously because the input signal itself is continuously varying. As the analog voltage changes, the sampled values also change. Each new sample may fall into a different quantization level, causing the PCM encoder to produce a new binary code. This sequence of changing codes forms the digital representation of the original analog waveform.

---

# Conclusion

This experiment demonstrated how analog signals are converted into digital form using Pulse Code Modulation. By observing the PCM encoder output for both constant and varying input voltages, the relationship between analog voltage levels and digital binary codes became clearer.

The experiment also illustrated the concept of quantization and how limited quantization levels introduce small approximation errors. Understanding PCM encoding is essential in modern communication systems because it forms the foundation of digital audio transmission, digital telephony, and data communication networks.

Through the use of the Emona Telecoms-Trainer 101 and the oscilloscope, the experiment provided practical insight into the process of analog-to-digital conversion and the generation of digital data streams from real-world signals.
