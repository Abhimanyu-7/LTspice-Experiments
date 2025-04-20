# 🧪 Experiment 01: Inverting & Non-Inverting Op-Amp 

> 🧠 A self-driven analog electronics experiment to simulate op-amp circuits using LTspice.  
> Part of my personal electronics journey, documented to track learning and share curiosity 🔧⚡

---

## 📚 Table of Contents  
- [🎯 Objective](#objective)  
- [📚 Theory](#theory)  
- [🛠️ LTspice Circuit Diagrams](#ltspice-circuit-diagrams)  
- [📈 Simulation Results](#simulation-results)  
- [📝 Observations](#observations)  
- [💭 Personal Notes](#personal-notes)  
- [📎 Files Included](#files-included)  
- [🚀 Run It Yourself](#run-it-yourself)  
- [📌 Why LTspice?](#why-ltspice)  
- [❤️ Purpose of This Repo](#purpose-of-this-repo)


---

## 🎯 Objective  
- Simulate and understand the behavior of::
  - Inverting Op-Amp  
  - Non-Inverting Op-Amp  
- Observe and verify the voltage gain for different resistor ratios.  
- Get comfortable using LTspice for analog signal visualization.  

---

## 📚 Theory  

### 🔄 Inverting Op-Amp  
\[
V_{out} = -\left(\frac{R_f}{R_{in}}\right) \cdot V_{in}
\]

> A signal inversion occurs due to the negative feedback to the inverting terminal.

### 🔼 Non-Inverting Op-Amp  
\[
V_{out} = \left(1 + \frac{R_f}{R_{in}}\right) \cdot V_{in}
\]

> Output remains in phase with the input. Gain starts from 1 even if \( R_f = 0 \).

---

## 🛠️ LTspice Circuit Diagrams  
- [x] Inverting Op-Amp  
- [x] Non-Inverting Op-Amp  
- Included `.asc` schematic files for simulation  
- Default op-amp used: `uA741` or equivalent model  

---

## 📈 Simulation Results  
- Input: 1V sine wave (or AC step)  
- Output waveform confirms theoretical gain:  
  - Inverting: \( V_{out} = -10 \cdot V_{in} \)  
  - Non-Inverting: \( V_{out} = 10 \cdot V_{in} \)  
- Signals visible in waveform viewer 📊

---

## 📝 Observations  
- Gain values match expected formulas  
- Inverting output is 180° out of phase  
- LTspice waveform plots help visualize real-time gain behavior  

---

## 💭 Personal Notes  
> I'm doing this in my free time to explore analog electronics deeply.  
> I try to study at least a small concept every day — this repo keeps me accountable 🔁

---

## 📎 Files Included  
