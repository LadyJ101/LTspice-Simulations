# NMOS Characteristic Curves

## Overview
This experiment performs a DC sweep analysis to plot the I-V characteristics (Drain Current $I_D$ vs. Drain-Source Voltage $V_{DS}$) of an NMOS transistor. This helps in understanding how the transistor behaves as a voltage-controlled current source.

## Simulation Details
* **Analysis Type:** `.dc` sweep.
* **Variable 1:** `VDS` swept from 0V to 5V (Linear sweep).
* **Variable 2:** `VGS` stepped from 3V to 5V in 1V increments.

## Results
The plot shows how increasing the Gate-Source Voltage ($V_{GS}$) shifts the curves, allowing higher current to flow through the Drain.

![NMOS Characteristics](./NMOS%20Xtics%20simulation.png)

## Key Learning Points
* **Triode Region:** The initial linear portion where $I_D$ rises steeply with $V_{DS}$.
* **Saturation Region:** The "flat" portion where $I_D$ remains nearly constant despite increases in $V_{DS}$. This is the region where the transistor acts as an amplifier or a logic switch.
