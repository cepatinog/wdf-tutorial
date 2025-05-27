# Wave Digital Filters (WDF) – Practical Tutorial & Simulation Framework

This repository provides a step-by-step, theory-driven and audio-oriented tutorial on **Wave Digital Filters (WDF)** using Python. It is based on Kurt James Werner’s dissertation and aims to bridge the gap between academic theory and practical implementation in audio DSP systems.

We combine:

*  **Jupyter Notebooks** for interactive theoretical explanations, derivations, visualizations, and prototyping.
*  **Python modules** for reusable WDF components, enabling real-time processing and future plugin development.

---

## 📂 Project Structure

```
TUTORIAL-WDF/
├── audio_files/                  # Input/output WAV and MP3 files for audio testing
├── filters/                      # Modular Python implementations of WDF-based filters
│   ├── rc_lowpass.py            # First-order RC low-pass filter
│   ├── rc_highpass.py           # First-order RC high-pass filter
│   ├── rc_1st2ndorder_bandpass.py  # First- and second-order band-pass filters
├── ltspice/eval/                # Exported frequency analysis results from LTSpice
│   └── frequency_analysis_dc_100hz_1st_order_lpf.txt
├── notebooks/                   # Clean notebooks combining theory, derivations, and experiments
│   ├── 01_Ports_and_Waves.ipynb                     # Fundamentals of WDF (ports, wave variables, passivity)
│   ├── 02_A_Algebraic_One_Port_Elements.ipynb       # Theoretical derivation of algebraic one-ports
│   └── 02_B_Algebraic_One_Port_Elements.ipynb       # Practical simulations and audio examples
├── old_notebooks/               # First versions and extended working drafts (kept for traceability)
├── requirements.txt             # Dependencies (e.g., pywdf, numpy, matplotlib)
├── README.md                    # You are here
```

---

## ✅ Status

### ✔ Implemented

* ✅ Wave variables: theory, definitions, and physical interpretation
* ✅ Energy-based reasoning, power and passivity visualization
* ✅ Algebraic one-port components: resistor, short, open, voltage sources, switch
* ✅ Modular implementation of RC filters (low-pass, high-pass, band-pass)
* ✅ Comparison with LTSpice

### 🔜 Coming next

* ⏳ Reactive components (capacitor and inductor): discretization, delays, state
* ⏳ Composite WDF trees: adaptors and connection strategies
* ⏳ Audio plugin integration (JUCE/VST)

---

## 🛠 Requirements

To install dependencies:

```bash
pip install -r requirements.txt
```

Also clone `pywdf` manually:

```bash
git clone https://github.com/gusanthon/pywdf
cd pywdf
pip install -e .
```

---

## 📚 References

* Kurt James Werner – *Virtual Analog Modeling of Audio Circuitry Using Wave Digital Filters* (PhD Thesis, 2016)
* [pywdf GitHub repo](https://github.com/gusanthon/pywdf)


---

## 👨‍🔬 Author

**Carlos Eduardo Patiño Gómez**
Master's Student in Music Computing @ UPF, Trombonist, and DSP Enthusiast.

Open to feedback, collaboration, and improvements!

---
