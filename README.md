
# pnflow – Classical Pore-Network (Extraction and) Flow Simulation

This repository contains **pnflow**, a classical pore-network flow simulation code.  
For network extraction from micro-CT images, the companion tool **[pnextract](https://github.com/aliraeini/pnextract)** is included here in the [`pnextract`](./pnextract) folder for convenience.  
Together, `pnflow` and `pnextract` form the **Pore-Network Model (PNM)** suite.

> 💡 **Note**: `pnflow` is a cleaned-up and restructured version of the original [poreflow code](https://www.imperial.ac.uk/earth-science/research/research-groups/pore-scale-modelling/software/two-phase-network-modelling-code) by [Valvatne & Blunt (2004)](https://doi.org/10.1029/2003WR002627). It was later extended for compatibility with the generalized network model ([Raeini et al., 2018](https://doi.org/10.1103/PhysRevE.97.023308)), sponsored by [TOTAL](https://www.total.com).

Recent validations of both `pnflow` and `pnextract` are published in:
- [Bultreys et al. (2018)](https://doi.org/10.1103/PhysRevE.97.053104)
- [Foroughi et al. (2020)](https://doi.org/10.1103/PhysRevE.102.023302)
- [Foroughi et al. (2021)](https://doi.org/10.1007/s11242-021-01609-y)

---

## 📦 Release Notes

- **2020–2021**: Major refactoring sponsored by [Wintershall Dea](https://wintershalldea.com) to align with internal private codes and the closed-source generalized network model.  
  ⚠️ This public version **lags behind** the author’s local development branch.  
  → If you’re interested in contributing or accessing newer features, please **contact the maintainer** (see below).

- **Input format changed**: Keywords in `input_pnflow.dat` were updated for compatibility with the generalized model.  
  See the example file: [`doc/input_pnflow.dat`](doc/input_pnflow.dat)

- Full change history: [`pnflow/ChangeLog`](pnflow/ChangeLog)

> 🔙 Need the older version? Use the [`pnm2019` branch](https://github.com/aliraeini/pnflow/tree/pnm2019).

---

## ▶️ Quick Start (Windows)

1. Copy the sample input file [`src/doc/input_pnflow.dat`](src/doc/input_pnflow.dat) and your extracted network files (`*_link1.dat`, `*_node1.dat`, etc.) into a new folder.
2. Edit `input_pnflow.dat`:
   - Set the `NETWORK` keyword to your network prefix.
   - Adjust flow parameters as needed.
3. Open **Command Prompt** in that folder:
   - Hold `Shift` + right-click → **"Open Command Window Here"**
4. Run:
   ```bat
   PATH\TO\bin\pnflow.exe input_pnflow.dat
   ```
   Replace `PATH\TO\bin\` with the actual path to `pnflow.exe`.

> ✅ On Linux, source the environment script:
> ```bash
> source PATH/TO/src/script/bashrc
> ```

---

## 🔧 Build Instructions

Precompiled Windows executables (`pnextract.exe`, `pnflow.exe`) are available in [`bin.7z`](../../bin.7z) (MinGW-built, Win64).

To build from source:
- See [`README.md`](README.md)
- Dependencies (including [Hypre](https://github.com/LLNL/hypre)) are provided in [`pkgs/`](pkgs)

---

## 📄 License

This software is released under a **zlib-style license**.  

---

## 📬 Contact & Support

- **Project Website**: [Imperial College Pore-scale Modelling Consortium](https://www.imperial.ac.uk/earth-science/research/research-groups/pore-scale-modelling)
- **Issues**: Please open a GitHub issue and mention:
  - [@ForoughiSajjad](https://github.com/ForoughiSajjad)
  - [@MingLiang-Qu](https://github.com/MingLiang-Qu)
  - [@yojeep](https://github.com/yojeep)

- **Email** (for collaboration or questions):
  - Sajjad Foroughi: `s.foroughi@imperial.ac.uk`
  - (Also reachable at: `12227053@zju.edu.cn`, `mingliangqu@zju.edu.cn`)

> 💌 *We welcome academic collaborations and bug reports!*