# 🚀 NHSS-Quantum-Computing
### A new quantum computing paradigm based on Non-Hermitian dynamics and Exceptional Points (EPs)

**NHSS (Non-Hermitian Spectral Steering)** introduces a fundamentally new way of performing quantum computation by steering quantum states through **Exceptional Points (EPs)** using **measurement-induced non-unitary evolution**.

Unlike traditional quantum computing—where unitary gates are used and noise must be suppressed—NHSS intentionally **uses decoherence, dissipation, and measurement feedback** as computational resources.

This repository provides the **first full implementation** of NHSS concepts using **IBM Quantum Dynamic Circuits**, including the definition of the **Ep-bit**, a new information unit based on topological state transitions.

---

# 🧠 What is NHSS?

### In standard quantum computing:
- Information is stored in amplitudes of |0⟩ and |1⟩  
- Operations must be reversible and unitary  
- Noise is a problem that must be minimized  

### In NHSS:
- Information is stored in **topological properties** of an effective non-Hermitian Hamiltonian  
- Measurement + feedback drives **non-unitary evolution**  
- Noise becomes part of an **effective computational engine**  

### Effective model:
```
H_eff = H + i·γ·Z
```

---

# 🔥 What is an Ep-bit?

An **Ep-bit (Exceptional Point bit)** is a new logical information unit defined by the system’s *position relative to an Exceptional Point*.

When the system encircles an EP:
- **1 loop (~2π)** → eigenstate switching  
- **2 loops (~4π)** → return to original state  

This switching behavior acts like a **logical bit flip**, driven by **topological phase transitions**, not quantum amplitudes.

➡ **Ep-bit = topological quantum memory.**

---

# 🧩 Why NHSS is different (and important)

| Traditional QC | NHSS |
|----------------|------|
| Uses unitary operations | Uses non-unitary evolution |
| Noise = error | Noise = part of computation |
| Info encoded in amplitudes | Info encoded in topology |
| Gates act locally | EP loops act globally |
| Hard to scale robustly | Topology potentially increases stability |

NHSS represents a **new paradigm**, not a variant of the gate model.

---

# 🧱 Repository Contents

```
NHSS-Quantum-Computing/
│
├── README.md
├── LICENSE
├── .gitignore
│
├── docs/
│   ├── theory_summary.md
│   ├── epbit_model.md
│   ├── device_requirements.md
│   └── NHSS_Whitepaper.md
│
├── src/
│   ├── nhss_simulator.py
│   ├── ibm_device_experiment.py
│   └── utils/
│       ├── measurement_feedback.py
│       └── parameter_sweep.py
│
└── examples/
    ├── epbit_basic_demo.py
    └── exceptional_point_scan.py
```

---

# ⚙️ Installation

### 1) Clone the repository
```bash
git clone https://github.com/<your-username>/NHSS-Quantum-Computing.git
cd NHSS-Quantum-Computing
```

### 2) Create a virtual environment

**Windows:**
```bash
python -m venv .venv
.venv\Scripts\activate
```

**macOS / Linux:**
```bash
python3 -m venv .venv
source .venv/bin/activate
```

### 3) Install dependencies
```bash
pip install --upgrade pip
pip install qiskit qiskit-aer qiskit-ibm-runtime
```

---

# ▶️ Run NHSS Simulations (AerSimulator)

### Basic Ep-bit demonstration:
```bash
python examples/epbit_basic_demo.py
```

### EP trajectory scan:
```bash
python examples/exceptional_point_scan.py
```

These simulations visualize how **measurement + feedback** induces EP-like state transitions.

---

# ▶️ Run on IBM Quantum Hardware

### 1) Add your IBM API token  
Edit:
```
src/ibm_device_experiment.py
```

Replace:
```python
MY_IBM_TOKEN = "PUT-YOUR-TOKEN-HERE"
```

### 2) Run real-device experiment:
```bash
python src/ibm_device_experiment.py
```

The script will:
- Connect to **ibm_fez** or **ibm_torino**
- Build the NHSS circuit  
- Sweep γ parameters  
- Print measurement results  
- Reveal EP-like eigenstate switching  

---

# 📚 Documentation Overview

- **docs/theory_summary.md** → NHSS physics & non-Hermitian Hamiltonians  
- **docs/epbit_model.md** → Ep-bit definition & behavior  
- **docs/device_requirements.md** → IBM hardware requirements  
- **docs/NHSS_Whitepaper.md** → Compact whitepaper of the NHSS paradigm  

---

# 🧪 Research Status

NHSS is:
- A **new theoretical paradigm**  
- Experimentally implementable on IBM hardware  
- Based on **non-Hermitian topology** instead of Hilbert-space amplitudes  
- Introducing **Ep-bits** as new quantum information units  

The goal of this repository is to make NHSS **reproducible, testable, and extendable** by the research community.

---

# 🤝 Contributions

Contributions are welcome in:
- Non-Hermitian quantum mechanics  
- Exceptional Point physics  
- Measurement-based quantum control  
- IBM quantum hardware experiments  
- Topological quantum computing  

Feel free to open an issue or pull request.
