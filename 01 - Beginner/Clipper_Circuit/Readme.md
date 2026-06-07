# Diode Clipper Circuit Experiment

## Overview
This project demonstrates the behavior of a biased diode clipper circuit. The purpose of this simulation is to observe how a diode can be used to limit (clip) the voltage level of an AC signal at a specific threshold set by a DC bias source.

## Circuit Configuration
The simulation uses the following components:
- **V1 (Source):** Sine wave, Amplitude: 5V, Frequency: 1kHz.
- **D1 (Diode):** Custom model `MyIdealDiode` (defined in the schematic).
- **V2 (Bias):** 3V DC source, used to set the clipping reference.
- **R1:** 10kΩ series resistor to limit current when the diode is conducting.

## Circuit Theory
When the input voltage from `V1` exceeds the voltage of the bias source `V2`, the diode becomes forward-biased and begins to conduct. This clamps the output voltage `V(n002)` to the level of `V2` plus the forward voltage drop of the diode ($V_{out} \approx V_{bias} + V_{diode}$).

## How to Run the Simulation
1.  Open `Clipper circuit.asc` in **LTspice**.
2.  Ensure your simulation settings are set to `.tran 5m` for a 5ms window.
3.  Click the **Run** button.
4.  Probe the output node to view the clipped waveform.

## Results
The captured waveform below demonstrates the clipping action:
- **Input (Green):** 5V sine wave.
- **Output (Blue):** Signal clipped at approximately 3V.

![Clipper Circuit Waveform](clipper_waveform.png)

## Key Learning Points
* **Ideal Diode Modeling:** By defining a custom `.model`, we can simulate "perfect" clipping behavior, which is useful for verifying theoretical calculations before using real-world components.
* **Biasing:** Adding a DC source in series with the diode allows for precise control over the voltage threshold, rather than being limited only to the diode's natural forward voltage drop.
