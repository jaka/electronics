# TDA2030 DIY Audio Power Amplifier Circuit

This is a simple audio power amplifier built around the TDA2030 audio amplifier IC. It’s a classic beginner-friendly design often used for small speakers, desktop audio, or homemade powered speakers.

![tiv](TDA2030.png)

Circuit is versatile: can accomodate also TDA2050 and LM1875 due to same pinout, requires single rail power supply.

## What this circuit does

The circuit takes a small audio signal from input and amplifies it enough to drive a speaker connected to output.

# Expected performance

| Supply Voltage | Speaker | Approx Power |
|---|---|---|
| 12V | 8Ω | 6–8W |
| 18V | 4Ω | 14–18W |

## Power supply
- 12 V–18 V regulated supply
- 2 A or more

Heat sink is mandatory!

| Component | Recommended value | Purpose | Larger than recommended value | Smaller than recommended value |
|-----------|------------------|---------|------------------------------|-------------------------------|
| R₁/R₂ | 100 kΩ | Bias voltage divider | Poor high-frequency attenuation | Danger of oscillation |
| R₃ | 100 kΩ | Non-inverting input biasing | Increase of input impedance | Decrease in input impedance |
| R₄ | 4,7kΩ | Closed loop gain setting | Decrease of gain | Increase in gain |
| R₅ | 100 kΩ | Closed loop gain setting | Increase of gain | Decrease in gain |
| R₆ | 1 Ω | Frequency stability | Danger of oscillation at high frequencies with inductive loads | — |
| R₇ | 2 kΩ | Upper frequency cutoff | Poor high-frequency attenuation | — |
| C₁ | 10 µF | Bias voltage stabilizer | | |
| C₂ | 2,2 µF | Input DC decoupling | — | Increase in low-frequency cutoff |
| C₃ | 2,2 µF | Inverting input DC decoupling | — | Increase in low-frequency cutoff |
| C₄ | 220 µF | Supply voltage bypass | — | Danger of oscillation |
| C₅ | 0,22 µF | Supply voltage bypass | — | Danger of oscillation |
| C₆ | 0,22 µF | Frequency stability | — | Danger of oscillation |
| C₇ | 1 / (2πBR₅) | Upper frequency cutoff | Smaller bandwidth | Larger bandwidth |
| D₁, D₂ | 1N4001 | To protect the device against output voltage spikes | — | — |

Closed loop gain must be higher than 24 dB.

EDA: Kicad 6.0.11