# System Check & Tool Installation

> Part of the **RISC‑V Reference SoC Tapeout Program**

This repository documents the initial system setup and required tool installations. Ensures your environment is ready for the RTL → GDSII flow.

---

## 🧩 Project Structure

```
system‑check‑and‑tools/
├── README.md                  # This file
├── snapshots/                 # Screenshots of installations
└── notes/                     # Video summaries / setup notes
```

---

## 🎯 Objectives

- Get the development environment ready by performing system checks.  
- Install essential open‑source tools: **Yosys**, **Icarus Verilog**, **GTKWave**.  
- Capture snapshots / evidence of correct installation.  
- Prepare for the next steps in the RISC‑V SoC design & tapeout flow.

---

## 🛠 System Requirements

| Component       | Minimum Specification        |
|------------------|-----------------------------|
| RAM              | 6 GB                        |
| Free Disk Space  | ≥ 50 GB                    |
| CPU              | 4 vCPUs                    |
| Operating System | Ubuntu 20.04 or newer (works on VM or WSL2) |

---

## 🔧 Installation & Setup Guide

These commands are to be run in a Linux shell (Ubuntu). Whether in a VM (Oracle VirtualBox), or WSL2, the process should work similarly.

### 1. Update System  
```bash
sudo apt-get update
sudo apt-get upgrade -y
```

### 2. Install Yosys  
```bash
sudo apt-get install -y build-essential clang bison flex libreadline-dev     gawk tcl-dev libffi-dev git graphviz xdot pkg-config python3     libboost-system-dev libboost-python-dev libboost-filesystem-dev zlib1g-dev

git clone https://github.com/YosysHQ/yosys.git
cd yosys
make config-gcc
make
sudo make install
cd ..
```

### 3. Install Icarus Verilog (iverilog)  
```bash
sudo apt-get update
sudo apt-get install -y iverilog
```

### 4. Install GTKWave  
```bash
sudo apt-get update
sudo apt-get install -y gtkwave
```

---

## 📋 Verification

After installation, verify that tools are properly installed:

```bash
yosys -V         # should display version
iverilog -V      # should display version
gtkwave --version  # should display version
```

Also, check the snapshots folder for terminal outputs and screenshots to confirm installations.

---

## 🔍 What’s Next

- Proceed with RTL design and simulation once environment is fully ready.  
- Share any issues or missing dependencies in `notes/`.  
- Keep versions updated as you progress.

---

## 🤝 Contribution / Help

If you find better instructions, additional useful tools, or ways to streamline setup, feel free to open a pull request or issue!

---

## 📜 License

MIT License — see [`LICENSE`](LICENSE) for full details.
