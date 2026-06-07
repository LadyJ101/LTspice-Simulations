# PMOS Characteristic Curves

## Overview
This experiment performs a DC sweep analysis to plot the I-V characteristics of a PMOS transistor. Understanding the PMOS is essential for designing CMOS logic, as it serves as the "pull-up" network that connects the output to $V_{DD}$ in gates like the NAND gate I previously simulated.

## Simulation Details
* **Analysis Type:** `.dc` sweep.
* **Variable 1:** `Vds` (Drain-Source Voltage) swept from 0V to -5V.
* **Variable 2:** `Vgs` (Gate-Source Voltage) stepped from 0V to -5V in 2V increments.

## Results
The plot below illustrates the behavior of the PMOS. Note the use of negative values for current and voltage, which is characteristic of PMOS devices compared to the positive values used for NMOS.

![PMOS Characteristic Curves](./PMOS%20Xtics.png)

## Key Learning Points
* **Polarity:** PMOS transistors operate with negative voltages ($V_{GS}$, $V_{DS}$) and produce negative drain currents.
* **Complementary Logic:** In a CMOS circuit, the PMOS acts as the switch that drives the output high, working in tandem with the NMOS which drives the output low.
* **Region Transition:** Like the NMOS, the PMOS transitions from the linear (triode) region to the saturation region as the magnitude of the drain voltage increases.
