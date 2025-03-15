# Plotting Tools 🛠️📈

A collection of Python scripts for generating interactive and static plots for visualizing computational chemistry output data (from ORCA) and experimental spectra

---

## Features ✨
- 📊 **Interactive MO Energy Diagrams**  
  Plotly Dash app for interactively visualizing MO energy levels and selecting energy windows.
  
- 🖼️ **Static MO Energy Diagrams (Matplotlib)**  
  High-quality static plots suitable for publications.

- 🎛️ **Customizable Parameters**  
  Easily specify orbital numbers, SOMO levels, energy windows, and more.

---

## Prerequisites 🔧
- Python 3.7+
- Packages:
  - `pandas`
  - `plotly`
  - `dash`
  - `matplotlib` (for static plots)

👉 Install all dependencies:
```bash
pip install -r requirements.txt

📂 Repository Structure

plotting-tools/
├── src/
│   └── plottingtools/
│       ├── interactive_mo_diagram.py
│       └── static_mo_diagram.py (coming soon)
├── README.md
└── requirements.txt

🛠️ Tools
1. interactive_mo_diagram.py

An interactive Dash + Plotly app to visualize MO energy levels, select a window, and export an energy range for further plotting.

Usage example:
```
python src/plottingtools/interactive_mo_diagram.py \
  --csv /path/to/VOMnt-cpcm-tddft-1sulfur-hfx25.15_orbital_energies.csv \
  --alpha-somo 84 \
  --beta-somo 87
```
    After running, a browser window will open automatically.
    You can zoom in on a region of the energy diagram.
    Click Save Energy Window to export your current window as energy_window.json in your working directory.

2. static_mo_diagram.py (coming soon)

A static Matplotlib version of the MO energy diagram, designed for use in publications. Accepts an energy window (either manually specified or imported from energy_window.json).

📄 Example CSV Format

The scripts expect a CSV file with the following headers (as output from getorbs.sh in https://github.com/josephzsombor/cc-scripts/blob/newstart/hfx/getorbs.sh):
```
Spin,NO,OCC,E(Eh),E(eV)
```

