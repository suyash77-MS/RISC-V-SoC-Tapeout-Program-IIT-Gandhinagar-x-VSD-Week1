🏆 #IIT Gandhinagar – VSD RISC-V SoC Tapeout Program

🚀 Overview

A silicon-proven, open-source SoC design journey where I learned the complete RTL-to-GDS flow on Sky130 PDK, starting from Verilog RTL, simulation, synthesis, optimizations, GLS, and tapeout methodologies.
This program by VSD and IIIT Gandhinagar gave me hands-on exposure to industry-grade open-source EDA tools and real fabrication-ready workflows.

🔧 Tools & Technologies Used


<img height="28" src="https://img.shields.io/badge/Icarus%20Verilog-FF4500?logo=verilog&logoColor=white"> <img height="28" src="https://img.shields.io/badge/GtkWave-4B8BBE?logo=waveform&logoColor=white"> <img height="28" src="https://img.shields.io/badge/Yosys-FFD700?logo=logic&logoColor=black"> <img height="28" src="https://img.shields.io/badge/OpenSTA-1E90FF?logo=timing&logoColor=white"> <img height="28" src="https://img.shields.io/badge/OpenROAD-228B22?logo=flow&logoColor=white"> <img height="28" src="https://img.shields.io/badge/Magic%20VLSI-6A0DAD?logo=magic&logoColor=white"> <img height="28" src="https://img.shields.io/badge/KLayout-FF0000?logo=layout&logoColor=white"> <img height="28" src="https://img.shields.io/badge/OpenLane-007ACC?logo=eda&logoColor=white"> <img height="28" src="https://img.shields.io/badge/SKY130%20PDK-FF6600?logo=chip&logoColor=white">


📚 Key Concepts Learned

📐 Verilog RTL Design & Simulation

RTL coding best practices (blocking vs non-blocking, sensitivity lists)

Writing testbenches with Icarus Verilog

Waveform analysis & debugging with GTKWave

⚙️ Logic Synthesis & Mapping

RTL → Gate-level mapping using Yosys

Flat vs Hierarchical synthesis

Timing-aware synthesis using Sky130 standard cells

⏱ Timing & Libraries

Understanding .lib files (TT, SS, FF)

Setup, hold, and timing arcs with OpenSTA

Effect of timing constraints on synthesis

🔄 Optimizations

Combinational optimizations → boolean simplification, dead logic removal

Sequential optimizations → retiming, removal of unused flops

Power–delay–area trade-offs with different coding styles

🧩 Simulation Mismatches & GLS

Gate-level simulation with back-annotated netlists

Debugging simulation-synthesis mismatches

Blocking vs Non-blocking pitfalls

🏭 RTL to GDSII Flow

Placement & routing with OpenROAD/OpenLane

Layout vs schematic (LVS) checks with Magic + Netgen

DRC, parasitic extraction, and timing closure

Tapeout preparation (Sky130 PDK signoff flow)

🧪 Lab Work Done

Verilog RTL Labs → designed good_mux, counters, flops with proper coding styles

Yosys Synthesis Labs → synthesized mux, flops, if/case constructs

Timing Labs → analyzed .lib, TT/SS/FF timing variations

Optimization Labs → experimented with combinational + sequential optimizations

GLS Labs → verified gate-level netlists and mismatches

RTL-GDS Flow Labs → ran OpenLane flow on synthesized blocks, viewed layouts in Magic/KLayout



📝 Projects & Contributions

RTL & GLS Verification → clean Verilog + gate-level validated designs

Synthesis Reports → timing, area, and power comparisons

Optimization Studies → coding styles impact on synthesis results

RTL-to-GDSII Demo → complete flow on Sky130 using OpenLane

# RISC-V Tapeout SoC by VSD and IIT Gandhinagar

**Program:** RISC-V Reference SoC Tapeout Program  
**Organized by:** VSD & IIT Gandhinagar  

---

## Table of Contents  
- [About](#about)  
- [Day 1 - Introduction to Verilog RTL Design and Synthesis](#day-1---introduction-to-verilog-rtl-design-and-synthesis)  
- [Day 2 - Timing libs, Hierarchical vs Flat Synthesis and Efficient Flop Coding Styles](#day-2---timing-libs-hierarchical-vs-flat-synthesis-and-efficient-flop-coding-styles)  
- [Day 3 - Combinational and Sequential Optimizations](#day-3---combinational-and-sequential-optimizations)  
- [Day 4 - GLS, Blocking vs Non-blocking and Synthesis-Simulation Mismatch](#day-4---gls-blocking-vs-non-blocking-and-synthesis-simulation-mismatch)  
- [Day 5 - Optimization in Synthesis](#day-5---optimization-in-synthesis)  

---

## About  
This repository captures my learning journey through the **RISC-V Reference SoC Tapeout Program** organized by **VSD & IIT Gandhinagar**, covering Verilog RTL design, synthesis, labs, and optimization techniques.  
Here I’ll document lecture notes, labs, examples, code, screenshots, and reflections as I move through each day.

---

# Day 1 - Introduction to Verilog RTL Design and Synthesis  

### 🔹 Introduction to Open-Source Simulator Iverilog  
- **2-SKY130RTL D1SK1 L1** → Introduction to Iverilog: Design & Testbench  

### 🔹 Labs using Iverilog and GTKWave  
- **3-SKY130RTL D1SK2 L1** → Lab1: Introduction to lab  
- **4-SKY130RTL D1SK2 L2** → Lab2: Iverilog & GTKWave (Part 1)  
- **5-SKY130RTL D1SK2 L3** → Lab2: Iverilog & GTKWave (Part 2)  

### 🔹 Introduction to Yosys and Logic Synthesis  
- **6-SKY130RTL D1SK3 L1** → Introduction to Yosys  
- **7-SKY130RTL D1SK3 L2** → Logic Synthesis (Part 1)  
- **8-SKY130RTL D1SK3 L3** → Logic Synthesis (Part 2)  

### 🔹 Labs using Yosys and Sky130 PDKs  
- **9-SKY130RTL D1SK4 L1** → Lab3: Yosys Good Mux (Part 1)  
- **10-SKY130RTL D1SK4 L2** → Lab3: Yosys Good Mux (Part 2)  
- **11-SKY130RTL D1SK4 L3** → Lab3: Yosys Good Mux (Part 3)  

---

# Day 2 - Timing libs, Hierarchical vs Flat Synthesis and Efficient Flop Coding Styles  

### 🔹 Introduction to Timing .libs  
- **12-SKY130RTL D2SK1 L1** → Lab4: Introduction to .lib (Part 1)  
- **13-SKY130RTL D2SK1 L2** → Lab4: Introduction to .lib (Part 2)  
- **14-SKY130RTL D2SK1 L3** → Lab4: Introduction to .lib (Part 3)  

### 🔹 Hierarchical vs Flat Synthesis  
- **15-SKY130RTL D2SK2 L1** → Lab5: Hierarchical vs Flat (Part 1)  
- **16-SKY130RTL D2SK2 L2** → Lab5: Hierarchical vs Flat (Part 2)  

### 🔹 Flop Coding Styles & Optimization  
- **17-SKY130RTL D2SK3 L1** → Why Flops? Flop coding styles (Part 1)  
- **18-SKY130RTL D2SK3 L2** → Flop coding styles (Part 2)  
- **19-SKY130RTL D2SK3 L3** → Lab: Flop synthesis simulations (Part 1)  
- **20-SKY130RTL D2SK3 L4** → Lab: Flop synthesis simulations (Part 2)  
- **21-SKY130RTL D2SK3 L5** → Interesting optimizations (Part 1)  
- **22-SKY130RTL D2SK3 L6** → Interesting optimizations (Part 2)  

---

# Day 3 - Combinational and Sequential Optimizations  

### 🔹 Introduction to Optimizations  
- **23-SKY130RTL D3SK1 L1** → Optimizations (Part 1)  
- **24-SKY130RTL D3SK1 L2** → Optimizations (Part 2)  
- **25-SKY130RTL D3SK1 L3** → Optimizations (Part 3)  

### 🔹 Combinational Logic Optimizations  
- **26-SKY130RTL D3SK2 L1** → Lab6: Combinational Logic (Part 1)  
- **27-SKY130RTL D3SK2 L2** → Lab6: Combinational Logic (Part 2)  

### 🔹 Sequential Logic Optimizations  
- **28-SKY130RTL D3SK3 L1** → Lab7: Sequential Logic (Part 1)  
- **29-SKY130RTL D3SK3 L2** → Lab7: Sequential Logic (Part 2)  
- **30-SKY130RTL D3SK3 L3** → Lab7: Sequential Logic (Part 3)  

### 🔹 Sequential Optimizations for Unused Outputs  
- **31-SKY130RTL D3SK4 L1** → Seq Optimisation unused outputs (Part 1)  
- **32-SKY130RTL D3SK4 L2** → Seq Optimisation unused outputs (Part 2)  

---

# Day 4 - GLS, Blocking vs Non-blocking and Synthesis-Simulation Mismatch  

### 🔹 GLS, Synthesis-Simulation Mismatch and Blocking/Non-blocking Statements  
- **33-SKY130RTL D4SK1 L1** → GLS Concepts & Flow using Iverilog  
- **34-SKY130RTL D4SK1 L2** → Synthesis-Simulation Mismatch  
- **35-SKY130RTL D4SK1 L3** → Blocking vs Non-Blocking Statements in Verilog  
- **36-SKY130RTL D4SK1 L4** → Caveats with Blocking Statements  

### 🔹 Labs on GLS and Synthesis-Simulation Mismatch  
- **37-SKY130RTL D4SK2 L1** → Lab: GLS Synth-Sim Mismatch (Part 1)  
- **38-SKY130RTL D4SK2 L2** → Lab: GLS Synth-Sim Mismatch (Part 2)  

### 🔹 Labs on Synth-Sim Mismatch for Blocking Statements  
- **39-SKY130RTL D4SK3 L1** → Lab: Synth-Sim mismatch (Blocking, Part 1)  
- **40-SKY130RTL D4SK3 L2** → Lab: Synth-Sim mismatch (Blocking, Part 2)  

---

# Day 5 - Optimization in Synthesis  

### 🔹 If-Case Constructs  
- **41-SKY130RTL D5SK1 L1** → IF-CASE Constructs (Part 1)  
- **42-SKY130RTL D5SK1 L2** → IF-CASE Constructs (Part 2)  
- **43-SKY130RTL D5SK1 L3** → IF-CASE Constructs (Part 3)  

### 🔹 Labs on Incomplete If-Case  
- **44-SKY130RTL D5SK2 L1** → Lab: Incomplete IF (Part 1)  
- **45-SKY130RTL D5SK2 L2** → Lab: Incomplete IF (Part 2)  

### 🔹 Labs on Incomplete Overlapping Case  
- **46-SKY130RTL D5SK3 L1** → Lab: Incomplete Overlapping Case (Part 1)  
- **47-SKY130RTL D5SK3 L2** → Lab: Incomplete Overlapping Case (Part 2)  
- **48-SKY130RTL D5SK3 L3** → Lab: Incomplete Overlapping Case (Part 3)  
- **49-SKY130RTL D5SK3 L4** → Lab: Incomplete Overlapping Case (Part 4)  

### 🔹 For Loop and For Generate  
- **50-SKY130RTL D5SK4 L1** → For Loop & For Generate (Part 1)  
- **51-SKY130RTL D5SK4 L2** → For Loop & For Generate (Part 2)  
- **52-SKY130RTL D5SK4 L3** → For Loop & For Generate (Part 3)  

### 🔹 Labs on For Loop and For Generate  
- **53-SKY130RTL D5SK5 L1** → Lab: For & For Generate (Part 1)  
- **54-SKY130RTL D5SK5 L2** → Lab: For & For Generate (Part 2)  
- **55-SKY130RTL D5SK5 L3** → Lab: For & For Generate (Part 3)  
- **56-SKY130RTL D5SK5 L4** → Lab: For & For Generate (Part 4)  

---

