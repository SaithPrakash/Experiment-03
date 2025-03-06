# Experiment-03

# Diffirential amplifier 

**Whats is a diffirential amplifier ?**

A differential (or difference) amplifier is a two-input circuit that amplifies only the difference between its two inputs.

     Vout = A * (Vin+ - Vin-)
     where A is the gain of the amplifier

![image](https://github.com/user-attachments/assets/ad225cca-8988-4497-9993-49c501c7c360)

**Why diffirential amplifier is preferred than mosfet ?**

A differential amplifier is generally preferred over a single MOSFET because it offers superior noise rejection by actively canceling out common-mode noise (noise present on both input signals), making it ideal for applications where clean signal amplification is crucial, especially in environments with high electrical interference , whereas a single MOSFET only amplifies the signal on one input, making it more susceptible to common-mode noise. 

Common-mode rejection:

The primary advantage of a differential amplifier is its ability to significantly suppress common-mode noise, which is noise present on both input lines simultaneously. 

High input impedance:

Differential amplifiers generally have high input impedances, minimizing loading effects on the signal source. 

Flexibility in design:

They can be easily implemented using various transistor types, including MOSFETs, allowing for customization depending on the application. 

**Question :**

Design and Analyze the Differential Amplifier for the following specs, Vdd=2.2V, P<=2.2mW, Vicm=1.2V, Vocm=1.25V, Vp=0.4V. Perform DC analysis, Transient Analysis, Frequency Response and extract the parameters.

![image](https://github.com/user-attachments/assets/b78dd514-9a27-4a41-a2db-e287d746d321)

<pre>
  
Given,  P = 2.2mW
        P = V*I
        Iss = P/V = 2.2m/2.2 = 1mA
        Iss = 1mA

  Id1 = Id2 = Iss/2

Therefore, Id1 = 0.5mA

To Find Rd :
  
        Rd = Vdd - Vocm / Id1
        
        Subs Id1 in Rd

        Rd = 2.2 - 1.25 / 0.5m = 1.9kohm

By Ohm's Law,
        Rss = Vd/Iss = 0.4/1m = 400ohm

Qpoint : (Vds, Id)Vgs

 Vds = Vd - Vs = 1.25 - 0.4 = 0.85V

Therefore, (0.85V, 0.5m)1.2V

</pre>

# Procedure

Step 1: DC Analysis

The goal in DC analysis is to find the operating point of the circuit (also known as the quiescent point) where the circuit is biased.

**Increase Vicm to 1V and Observe Vocm, Vp**

• Vicm is the common-mode input voltage. When you set Vicm to 1V, you're setting the common-mode voltage at the input of the differential amplifier to 1V.

• Vocm is the output common-mode voltage, which should be observed and ideally remain at a desired level (typically set by the biasing network).

• Vp refers to the peak voltage, which should be related to the output swing.

Step 2: Transient Analysis

Calculate Maximum Input Swing and Output Swing.

• The maximum input swing refers to how much you can vary the input signal without causing distortion or clipping at the output.

• This is determined by the common-mode rejection ratio (CMRR) and the input voltage range that keeps the transistors in the active region.

• Maximum output swing refers to how much the output can vary while still staying in the linear region.

• The output will be limited by the power supply voltages (for instance, if powered with ±Vcc, the output will be constrained between ±Vcc).


Calculate Gain if the Output is Linear.

• If the output is still linear (i.e., no distortion or clipping), you can calculate the gain by:

Gain(𝐴𝑣)= Δ𝑉out / Δ𝑉in

• You can use this ratio to determine how effectively the input signal is being amplified by the circuit.

Step 3: AC Analysis

• In AC analysis, we examine the frequency response of the circuit to find the bandwidth.

• The 3-dB bandwidth is the frequency range where the gain of the amplifier falls to 70.7% (or -3 dB) of its maximum value.


## Circuit 1

![WhatsApp Image 2025-03-06 at 22 41 09_0daee77d](https://github.com/user-attachments/assets/d02ac63d-4c9e-4da9-9a31-7ef425c3145f)


DC Analysis

![WhatsApp Image 2025-03-06 at 22 41 09_f842c61f](https://github.com/user-attachments/assets/dbd979b0-3757-4efd-8f06-b1c57aa7cc96)




