# 🧪 Experiment 4: Differential Amplifier 

## 📌 Objective
To simulate and analyze the behavior of a ** Differential Amplifier** using **LTspice**, and to study the differential-mode and common-mode responses of the circuit.

---

## 📚 Theory

A **Differential Amplifier** amplifies the **difference** between two input signals. It is a key building block in analog integrated circuits such as operational amplifiers.

In a CMOS implementation:
- **NMOS transistors (M1 & M2)** form the differential input pair.
- **PMOS transistors (M3 & M4)** act as active loads to increase gain.
- **M5 & M6** act as current sources using **bias voltages**.
- This structure avoids resistors, making it compact and power-efficient for IC fabrication.

### Key Features:
- High Common Mode Rejection Ratio (CMRR)
- Low power consumption
- High gain due to active load

---

## 🔧 Tools & Environment
- **Software:** [LTspice XVII](https://www.analog.com/en/design-center/design-tools-and-calculators/ltspice-simulator.html)
- **Simulation Type:** Transient and DC Operating Point Analysis
- **Design Style:** CMOS level implementation (no resistors)

---

## 🖥️ Circuit Configuration

### Schematic Components:
- NMOS: M1, M2, M5, M6
- PMOS: M3, M4
- Voltage Sources:
  - `VDD` = 1V (Positive Supply)
  - `VB1` = 543 mV (Bias for M5)
  - `VB2` = 361 mV (Bias for M6)
  - `Vin1` = SINE(500m 5m 1k) — Input 1
  - `Vin2` = SINE(500m 5m 1k 0 0 180) — Input 2 (180° phase-shifted)

### Transistor Sizes:
- M1, M2: W = 2.5 μm, L = 100 nm
- M3, M4: W = 5 μm, L = 100 nm
- M5, M6: W = 5 μm, L = 100 nm

### Output:
- `Vout` taken from drain of M2 (single-ended output)

---

## ⚙️ Simulation Steps in LTspice

1. Open LTspice and create a **New Schematic**.
2. Use the **nmos** and **pmos** symbols for transistors.
3. Define **model files** for the NMOS and PMOS devices (`N_50n` and `P_50n` respectively).
4. Add voltage sources for VDD, VB1, VB2, Vin1, and Vin2.
5. Add `.tran 0 10m` for transient analysis.
6. Add `.dc` or `.op` command for DC operating point analysis.
7. Wire the components as per the schematic.
8. Run the simulation and probe `Vout`.

---

## 📊 Expected Observations

| Parameter         | Expected Behavior                     |
|------------------|----------------------------------------|
| Vout waveform     | Amplified sine wave with differential phase |
| DC operating point| Shows bias currents and voltages at each node |
| CMRR             | High — common mode signals are rejected |
| Gain             | High due to active PMOS load            |

---

## 📈 Sample Output Waveform

- You should observe a sine wave at `Vout` whose **amplitude** depends on the difference between `Vin1` and `Vin2`.
- The phase of `Vout` may resemble the **in-phase component** of `Vin1 - Vin2`.

---

## ✅ Results

- Successfully simulated a CMOS differential amplifier using LTspice.
- Verified differential operation by applying 180° out-of-phase inputs.
- Observed high gain and high CMRR.
- Achieved full CMOS implementation without any resistors.

---

## 📎 Files Included

- `differential_amplifier.asc` – LTspice schematic file
- `differential_amplifier.raw` – Output waveform data
- `README.md` – This documentation file

---

## 📖 References

- R. Jacob Baker, *CMOS: Circuit Design, Layout, and Simulation*
- Sedra & Smith, *Microelectronic Circuits*
- LTspice official documentation: [Analog Devices](https://www.analog.com/en/design-center/design-tools-and-calculators/ltspice-simulator.html)

---

## 💡 Future Extensions

- Add a differential to single-ended converter stage.
- Implement a differential amplifier with tail current source using current mirror.
- Perform noise and frequency response analysis.

---

## ✍️ Author

**Name:** Abhimanyu Kumar  
**Experiment Number:** 4  
**Course:** Analog Electronics Lab  
**Institute:** Thapar Institute of Engineering and Technology

---

