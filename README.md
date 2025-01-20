# Streaming Decryption Machine Security Project

## Overview
This repository contains the implementation and analysis of a **Streaming Decryption Machine**, developed as part of the coursework for **EL 9453: Introduction to Hardware Security and Trust (2023)** at NYU Tandon School of Engineering. The project focuses on exploring both the implementation and attack of cryptographic systems using AES, DES, and XOR encryption algorithms. The work is organized into a red-team/blue-team format, involving both the design for security and security analysis.

## Repository Structure

```
Streaming_Decryption_Machine/
├── Attacks/
│   ├── Codes/
│   │   ├── ChipWhisperer Firmware Upgrade.ipynb
│   │   ├── CPA_tutorial_on_AES.ipynb
│   │   ├── m2_aes_code.ipynb
│   │   ├── m2_des_code.ipynb
│   │   ├── m2_xor_code.ipynb
│   │   ├── PA_CPA_2-Manual_CPA_Attack.ipynb
│   │   └── PJM1.ipynb
│   ├── HexFiles/
│   ├── ghidra_project.zip
│   └── Keys.txt
├── Security_Hardening/
│   ├── Codes/
│   │   ├── aes_code.ipynb
│   │   ├── des_code.ipynb
│   │   └── xor_code.ipynb
├── HWSec_Project_M3_Report.pdf
├── LICENSE
└── README.md
```

### Key Folders and Files:
1. **Attacks/**
   - Contains code and resources related to cryptographic attacks, including power analysis and CPA (Correlation Power Analysis).
   - Files include:
     - `m2_aes_code.ipynb`: Attack implementation for AES.
     - `m2_des_code.ipynb`: Attack implementation for DES.
     - `m2_xor_code.ipynb`: Attack implementation for XOR encryption.
     - Other tutorials and tools for analysis.

2. **Security_Hardening/**
   - Contains security-hardened implementations of AES, DES, and XOR decryption engines, focusing on mitigating side-channel attacks.

3. **HWSec_Project_M3_Report.pdf**
   - The final project report summarizing milestones, experiments, and findings.

4. **HexFiles/** and **ghidra_project.zip**
   - Reverse engineering and firmware analysis resources.

5. **Keys.txt**
   - Key material used in the decryption implementations and testing.

## Milestones

### Milestone 1: Asset Analysis and System Design
- **Objective**: Understand the system's security properties, identify threats, and implement the streaming decryption engine.
- **Deliverables**:
  - AES, DES, and XOR decryption engines.
  - Embedded decryption keys within firmware.

### Milestone 2: Implementation Attacks
- **Objective**: Perform side-channel attacks on the encryption engines to extract keys.
- **Techniques**:
  - Correlation Power Analysis (CPA)
  - Firmware reverse engineering
  - Hypothesis testing using captured power traces.

### Milestone 3: Security Hardening
- **Objective**: Harden the system against known attacks and reflect on findings.
- **Deliverables**:
  - Updated and documented security-hardened source code.
  - Final report analyzing weaknesses and defenses.

## How to Use

1. **Dependencies**:
   - Python with Jupyter Notebooks
   - ChipWhisperer hardware and software tools
   - STM32F042 development board

2. **Setup**:
   - Use `pyserial` to communicate with the decryption engine via UART.
   - Follow the attack implementation tutorials in the `Attacks/` folder.

3. **Running the Code**:
   - Load the `.ipynb` notebooks to implement or analyze the streaming decryption engine.
   - Test decryption functionality using provided scripts and keys.

## Final Report Highlights
- A comprehensive analysis of side-channel vulnerabilities in cryptographic implementations.
- Detailed discussion on how to secure systems against implementation attacks.
- Recommendations for improving hardware-level cryptographic security.

## License
This project is licensed under the MIT License. See the `LICENSE` file for details.
