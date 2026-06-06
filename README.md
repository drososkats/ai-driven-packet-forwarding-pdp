# AI-Driven Packet Forwarding with Programmable Data Plane

![LaTeX](https://img.shields.io/badge/LaTeX-Beamer-008080?style=flat-square&logo=latex&logoColor=white)
![License](https://img.shields.io/badge/License-CC%20BY--SA%204.0-lightgrey?style=flat-square)
![University](https://img.shields.io/badge/University-Harokopio%20Athens-005A8C?style=flat-square)
![Course](https://img.shields.io/badge/Course-Next%20Gen%20Networks-4A90B8?style=flat-square)
![Status](https://img.shields.io/badge/Status-Complete-27AE60?style=flat-square)
![IEEE](https://img.shields.io/badge/Paper-IEEE%20COMST%202023-E67E22?style=flat-square&logo=ieee)

> **MSc Presentation** — Next Generation Network Infrastructures and Services  
> Harokopio University of Athens | Department of Informatics and Telematics  
> Academic Year 2025–2026 | Supervisor: Dr. Liotou Eirini

---

## Overview

This repository contains the full **LaTeX Beamer source code** for the MSc presentation on:

> *"AI-Driven Packet Forwarding With Programmable Data Plane: A Survey"*  
> Based on: **Quan et al., IEEE Communications Surveys & Tutorials, Vol. 25, No. 1, 2023**  
> DOI: [10.1109/COMST.2022.3217613](https://ieeexplore.ieee.org/document/9931326)

The presentation covers how **Artificial Intelligence (AI)** and **Programmable Data Planes (PDP)** can be combined to achieve intelligent, wire-speed packet forwarding — moving AI decision-making from a centralized SDN controller directly **inside the switch**.

---

## Presentation Structure

| Section | Title | Slides |
|---------|-------|--------|
| 1 | Introduction & Motivation | 3 |
| 2 | Background: PDP & P4 | 3 |
| 3 | AI Integration in the Data Plane | 3 |
| 4 | Taxonomy of AI-Driven Forwarding | 1 |
| 5 | Key Use Cases & Applications | 3 |
| 6 | Open Challenges & Limitations | 1 |
| 7 | Future Directions & Conclusion | 3 |
| — | Closing (References, Repo, Thank You) | 3 |
| — | Appendix (Abbreviations) | 1 |
| **Total** | | **~21 slides** |

---

## Key Topics Covered

- **SDN vs PDP** — architectural shift from centralized to distributed AI
- **P4 Language** — protocol-independent packet processing and Match-Action pipeline
- **AI Integration Workflow** — 5-step process from data collection to wire-speed deployment
- **Hardware Constraints** — SRAM limits, no floating point, stateless pipeline stages
- **Taxonomy** — four performance dimensions: Delay, Throughput, Security, Reliability
- **Use Cases** — Congestion Control (RL), DDoS Defense (RF), Ransomware Detection (RF)
- **Open Challenges** — translation gap, adversarial ML, lack of standardization
- **Future Directions** — 6G architectures, collaborative security, IoT/Industrial scenarios

---

## Repository Structure

```
ai-driven-packet-forwarding-pdp/
│
├── presentation.tex          # Main file — compile this
├── references.bib            # BibTeX bibliography
│
├── contents/                 # Section index files
│   ├── section1.tex
│   ├── section2.tex
│   ├── section3.tex
│   ├── section4.tex
│   ├── section5.tex
│   ├── section6.tex
│   ├── section7.tex
│   └── closing.tex
│
├── section1/                 # Introduction & Motivation
│   ├── s1_motivation.tex
│   ├── s1_problem.tex
│   └── s1_objectives.tex
│
├── section2/                 # Background: PDP & P4
│   ├── s2_sdn_vs_pdp.tex
│   ├── s2_arch_shift.tex
│   └── s2_p4_language.tex
│
├── section3/                 # AI Integration
│   ├── s3_integration.tex
│   ├── s3_fig4.tex
│   └── s3_delay.tex
│
├── section4/                 # Taxonomy
│   └── s4_taxonomy.tex
│
├── section5/                 # Use Cases
│   ├── s5_usecase1.tex
│   ├── s5_usecase2.tex
│   └── s5_usecase3.tex
│
├── section6/                 # Open Challenges
│   └── s6_challenges.tex
│
├── section7/                 # Future Directions & Conclusion
│   ├── s7_fig12.tex
│   ├── s7_directions.tex
│   └── s7_conclusion.tex
│
└── figures/                  # All images and diagrams
    ├── hua-logo-english-dit.png
    ├── fig2.png              # Traditional SDN Framework
    ├── fig3.png              # PDP Framework
    ├── fig4.png              # Network Delay Components
    ├── fig6.png              # DDoS Defense Mechanism
    ├── fig7.png              # Ransomware Detection
    ├── fig10.png             # Congestion Control Framework
    ├── fig12.png             # Future Trends Diagram
    └── p4.png                # P4 Pipeline Diagram (custom)
```

---

## How to Compile

### Requirements

- LaTeX distribution: **TeX Live** or **MiKTeX**
- Engine: `pdflatex`
- Required packages: `beamer`, `metropolis`, `tcolorbox`, `xcolor`, `colortbl`, `graphicx`, `hyperref`, `fontawesome5`

### Compile Steps

```bash
# Step 1: First compile
pdflatex presentation.tex

# Step 2: Bibliography
bibtex presentation

# Step 3: Second compile
pdflatex presentation.tex

# Step 4: Final compile
pdflatex presentation.tex
```

### Using Overleaf

1. Download this repository as ZIP
2. Upload to [Overleaf](https://www.overleaf.com)
3. Set compiler to `pdfLaTeX`
4. Click **Compile**

---

## Color Palette

The presentation uses a custom HUA-based color palette:

| Color | Hex | Usage |
|-------|-----|-------|
| `HUAblue` | `#005A8C` | Headers, titles, primary elements |
| `HUAdark` | `#003A5C` | Stat box backgrounds |
| `HUAlight` | `#4A90B8` | Borders, secondary elements |
| `HUApale` | `#D6EAF4` | Card backgrounds |
| `problemorange` | `#E67E22` | Problems, bottlenecks |
| `problemred` | `#C0392B` | Critical issues, threats |
| `solutiongreen` | `#27AE60` | Solutions, results, goals |

---

## References

| | |
|---|---|
| **Survey Paper** | W. Quan et al., *AI-Driven Packet Forwarding With Programmable Data Plane: A Survey*, IEEE COMST, 2023. [Link](https://ieeexplore.ieee.org/document/9931326) |
| **P4 Language** | P4 Language Consortium, *P4 Language Specification v1.2*, 2021. [Link](https://p4.org) |
| **In-Network ML** | Z. Xiong & N. Zilberman, *Do Switches Dream of Machine Learning?*, HotNets 2019. [Link](https://doi.org/10.1145/3365609.3365864) |
| **Course Material** | Dr. Liotou Eirini, *Next Generation Network Infrastructures and Services*, HUA 2025. [eClass](https://eclass.hua.gr/modules/document/?course=DIT318) |

---

## Author

**Katsimpras Drosos**  
MSc in Advances in Computer Science and Informatics Systems  
Department of Informatics and Telematics  
Harokopio University of Athens  
Academic Year 2025–2026

---

## License

This presentation is licensed under [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/).  
The survey paper is © IEEE 2023 — all rights reserved.
