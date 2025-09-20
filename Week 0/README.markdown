# 🚀 Week 0: VLSI System Design (VSD) Program Foundation & Tool Setup

![VLSI](https://img.shields.io/badge/VLSI-System-blue)  ![System Design](https://img.shields.io/badge/System-Design-darkblue)  ![Week 0](https://img.shields.io/badge/Week-0-orange)  ![Status](https://img.shields.io/badge/Status-Complete-brightgreen)
---
Welcome to my **VLSI System Design (VSD) Program** repository! This week focuses on **setting up the development environment** and installing essential open-source tools for synthesis, simulation, and layout design.

---

## 🎯 System and Virtual Machine Configuration

To ensure optimal performance, I configured a **Virtual Machine (VM)** with the following specifications:

| Specification | Details |
| --- | --- |
| Operating System | Ubuntu 20.04+ |
| RAM | 6 GB |
| Storage | 50 GB HDD |
| vCPUs | 4 |

> 💡 **Pro Tip**: This setup guarantees sufficient resources for handling toolchain demands and running simulations smoothly.

---

## ⚙ Tool Installation & Verification

The following tools were installed for **RTL synthesis, simulation, circuit analysis, and layout design**. Below are the installation commands and verification steps.

### 🧠 1. Yosys – RTL Synthesis

**Installation:**

```bash
git clone https://github.com/YosysHQ/yosys.git
cd yosys
sudo apt install make build-essential clang bison flex \
libreadline-dev gawk tcl-dev libffi-dev git \
graphviz xdot pkg-config python3 libboost-system-dev \
libboost-python-dev libboost-filesystem-dev zlib1g-dev -y

make config-gcc
git submodule update --init --recursive
make -j$(nproc)
sudo make install
```

**Verification:**

```bash
yosys
```
![Alt text](yosys.png)
### 📟 2. Icarus Verilog

**Installation:**

```bash
sudo apt update
sudo apt install iverilog -y
```

**Verification:**

```bash
iverilog -V
```
![Alt text](iverilog.png)
### 📊 3. GTKWave

**Installation:**

```bash
sudo apt update
sudo apt install gtkwave -y
```

**Verification:**

```bash
gtkwave --version
```
![Alt text](gtkwave_1.png)
### ⚡ 4. Ngspice

**Installation:**

```bash
sudo apt update
sudo apt install ngspice -y
```

**Verification:**

```bash
ngspice -v
```
![Alt text](ngspice.png)
### 🎨 5. Magic VLSI

**Installation:**

```bash
sudo apt install m4 tcsh csh libx11-dev tcl-dev tk-dev \
libcairo2-dev mesa-common-dev libglu1-mesa-dev libncurses-dev -y

git clone https://github.com/RTimothyEdwards/magic
cd magic
./configure
make -j$(nproc)
sudo make install
```

**Verification:**

```bash
magic
```

---
![Alt text](tkcon.png)
## ✅ Summary of Installed Tools

| Tool | Status | Purpose |
| --- | --- | --- |
| Yosys | Installed | RTL Synthesis |
| Icarus Verilog | Installed | Functional Simulation |
| GTKWave | Installed | Waveform Viewer |
| Ngspice | Installed | Analog Simulation |
| Magic VLSI | Installed | Layout Design |

---

**Repository**: Kavisha_RSIC-V_Tapeout_VSD\
**Author**: Kavisha2035\
**Program**: VLSI System Design (VSD)
