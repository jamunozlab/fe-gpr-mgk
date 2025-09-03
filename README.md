# fe-gpr-mgk
# Gaussian Process Regression on Effective Crystal Graphs of BCC Iron

This repository contains the code base and analysis workflows supporting the project:

---

## 📖 Project Overview
We develop and apply **Gaussian Process Regression with a Marginalized Graph Kernel (GPR-MGK)** to investigate the **mechanical stability of body-centered cubic (BCC) iron** at Earth’s core–like pressures and temperatures.  

- **Training data**: Ab initio molecular dynamics (AIMD) simulations of 128-atom supercells of BCC iron across temperatures (800–5000 K) and lattice parameters (2.36 & 2.49 Å).  
- **Models**: Graph-based ML potentials constructed using effective crystal graph representations.  
- **Results**:  
  - RMSE < 5 meV/atom for trained regressors.  
  - Force–displacement analyses identify the role of nearest-neighbor interactions in dynamical stability.  

---

## 📂 Repository Structure
The repository includes Jupyter notebooks used for model training, force prediction, and analysis:

- **`GPR Training.ipynb`** – Builds and trains GPR-MGK models on AIMD data.  
- **`Force Plot.ipynb`** – Generates force–displacement plots for nearest-neighbor stability analysis.  
- **`1NN Numeric Force Prediction_jorge.ipynb`** – First nearest-neighbor force displacement predictions.  
- **`2NN Numeric Force Prediction.ipynb`** – Second nearest-neighbor force displacement predictions.  
- **`3NN Numeric Force Prediction (HCP Transition).ipynb`** – Third nearest-neighbor force predictions, including HCP transition behavior.  
  

---

## ⚙️ Requirements
The notebooks rely on the following Python ecosystem:

- Python ≥ 3.9  
- [ASE](https://wiki.fysik.dtu.dk/ase/) – Atomic Simulation Environment  
- [GraphDot](https://github.com/yhtang/graphdot) – GPU-accelerated marginalized graph kernel  
- NumPy, SciPy, pandas, matplotlib  
- Jupyter Notebook  

To install dependencies:
```bash
pip install ase graphdot numpy scipy pandas matplotlib jupyter

