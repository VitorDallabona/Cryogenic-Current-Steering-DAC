# Cryogenic Current-Steering DAC for Quantum Computing Control

![Status](https://img.shields.io/badge/Status-In%20Development-yellow)
![Technology](https://img.shields.io/badge/Technology-22nm%20FD--SOI-blue)
![Application](https://img.shields.io/badge/Application-Quantum%20Computing-purple)

## 📖 Overview

This repository hosts the design files, simulation scripts, and data analysis code for a personal research project focused on a **Cryogenic 6-bit Current-Steering Digital-to-Analog Converter (DAC)**.

The project addresses the "wiring bottleneck" in superconducting quantum processors by proposing a control interface capable of operating at **4 Kelvin**. The central hypothesis investigates the use of **22nm FD-SOI (Fully Depleted Silicon-on-Insulator)** technology to mitigate severe transistor mismatch at cryogenic temperatures through **Back-Gate Biasing calibration**.

## 🎯 Project Objectives

- **Design:** Implement a binary-weighted current-steering DAC core (6-bit) using 22nm FD-SOI transistor models.
- **Characterization:** Analyze static linearity (INL/DNL) and dynamic performance (SFDR) at 300 K vs. 4 K.
- **Monte Carlo Analysis:** Quantify the impact of cryogenic process variability and mismatch on the output current.
- **Calibration Strategy:** Demonstrate the restoration of linearity (DNL < 1 LSB) using Back-Gate Biasing ($V_{BB}$) tuning.

## 🛠️ Roadmap

### 1: Theoretical Foundations
- [ ] Study **Current-Steering architectures**.
- [x] Analyze **Cryogenic MOSFET physics**: Understand $V_{th}$ shift, mobility increase, and mismatch degradation.
- [x] Understand **22nm FD-SOI mechanics**: Master the Back-Gate Biasing ($\gamma$ factor) for $V_{th}$ compensation.
- [ ] Define **Target Specifications**: Correlate DAC linearity (INL/DNL) with Qubit Gate Fidelity requirements.

### 2: Core Design & DC Analysis
- [ ] Setup simulation environment (PDK/Models).
- [ ] Design the Unit Current Cell (Cascode Topology).
- [ ] Simulate $I_D \times V_{GS}$ and $I_D \times V_{BB}$ curves at 4 K.
- [ ] Verify Back-Gate sensitivity for $V_{th}$ tuning.

### 3: Array Implementation & Linearity
- [ ] Implement the 6-bit Binary-Weighted array.
- [ ] Develop Python/Ocean scripts for static linearity testing (Ramp input).
- [ ] Extract INL and DNL metrics at 300 K.
- [ ] Extract INL and DNL metrics at 4 K (showing degradation).

### 4: Variability & Calibration
- [ ] Run Monte Carlo simulations (500+ runs) to estimate Yield.
- [ ] Implement "In-Silico" calibration: Find optimal $V_{BB}$ to minimize mismatch.
- [ ] Compare SFDR (Spectral Purity) before and after calibration.

### 5: Documentation
- [ ] Data visualization (Histograms, FFT plots).
- [ ] Draft final paper/report.

---

## 📚 Study Resources & Bibliography

### 🎥 Video Lectures
* **Iowa State University - Data Converters Lecture Series:**
    * Comprehensive course on data converter architectures and non-idealities.
    * [Watch on Panopto](https://iastate.hosted.panopto.com/Panopto/Pages/Sessions/List.aspx#folderID=%226af1f806-6a2a-4fc9-8050-b2750130a025%22&page=1)

### 📖 Fundamental Textbooks
The following books are used as the theoretical foundation for the circuit design and analysis:

1.  **Razavi, B.** *Principles of Data Conversion System Design*. IEEE Press, 1995.
2.  **Gustavsson, M., Wikner, J. J., & Tan, N.** *CMOS Data Converters for Communications*. Springer, 2000.
3.  **Maloberti, F.** *Data Converters*. Springer, 2007.

### 📄 Key Papers
* *Zurita et al. (2020)* - "Cryogenic Current Steering DAC With Mitigated Variability".
* *Kapoulea et al. (2025)* - "Cryo-CMOS 0.432mW UHF Filter for Scalable Quantum Computing in 22nm FD-SOI Technology".
* *Chakraborty et al. (2021)* - "Characterization and Modeling of 22 nm FDSOI Cryogenic RF CMOS".
* *Beckers et al. (2019)* - "Characterization and modeling of 28-nm FDSOI CMOS technology down to cryogenic temperatures".
* *Bardin et al. (2019)* - "29.1 A 28nm Bulk-CMOS 4-to-8GHz 2mW Cryogenic Pulse Modulator for Scalable Quantum Computing".
---

## 📂 Repository Structure

_[STILL IN DEVELOPMENT]_

## 📝 License
This project is open-source and available under the MIT License.
