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
  
  🔹 Simulator

Tool that mimics hardware behavior of HDL (Verilog/SystemVerilog) code.

Lets you check functionality before actual hardware implementation.

🔹 Design

Your RTL/Verilog/SystemVerilog code (the circuit you want to build).

Example: counter, ALU, FSM, etc.

🔹 Testbench

A verification code that stimulates the design with inputs.

Checks whether outputs match expected behavior.

Doesn’t synthesize → used only for simulation.

🔹 How Simulator Works

Compiles both design and testbench.

Executes testbench inputs on design.

Produces output + optional waveform data.

🔹 Icarus Verilog (iverilog) Simulation Flow

Write design + testbench.

Compile: iverilog -o sim_out design.v testbench.v

Run: vvp sim_out

Generate waveform (VCD): $dumpfile("wave.vcd"); $dumpvars; inside testbench.

🔹 VCD File (Value Change Dump)

File format storing signal transitions over time.

Generated during simulation for waveform viewing.

🔹 GTKWave

GUI tool to visualize VCD files.

Run: gtkwave wave.vcd

Lets you see signals, timing, glitches, and debug your logic.

  <img width="1312" height="610" alt="image" src="https://github.com/user-attachments/assets/b1a950f0-d1d0-4978-b5aa-508c7e0a1721" />


### 🔹 Labs using Iverilog and GTKWave  
- **3-SKY130RTL D1SK2 L1** → Lab1: Introduction to lab

Design And Testbench Of 2:1 Multiplexer (MUX) Using Iverilog & GTKWAVE

Circuit Function: A multiplexer selects one input from multiple inputs based on a control signal.

Working:

If sel = 0 → Output y = a

If sel = 1 → Output y = b

Use Case: Data selection, routing signals, implementing logic functions.

Simulation: Implemented in Verilog with a testbench; simulated using Icarus Verilog (iverilog) and waveform observed in GTKWave.

  <img width="1230" height="592" alt="image" src="https://github.com/user-attachments/assets/0d920834-6006-4dce-9c6f-94209eb83d9a" />

- **4-SKY130RTL D1SK2 L2** → Lab2: Iverilog & GTKWave (Part 1)
  
  Commands Snapshot Of Implementation Of Commands To Run Mux Design
  
  <img width="1232" height="573" alt="image" src="https://github.com/user-attachments/assets/70d71cb7-45d0-4b9b-a57e-4b62ef7aebce" />

  Output Of Mux In GTKWAVE

  <img width="1257" height="365" alt="image" src="https://github.com/user-attachments/assets/a9f7ec2a-0cb6-48ff-abcd-970e8c494726" />


- **5-SKY130RTL D1SK2 L3** → Lab2: Iverilog & GTKWave (Part 2)
  
  Iverilog Code and Test Bench For Mux Design
  
  <img width="588" height="457" alt="image" src="https://github.com/user-attachments/assets/e39e770a-8e46-4f2d-a38b-a21b57feb51d" />


### 🔹 Introduction to Yosys and Logic Synthesis  
- **6-SKY130RTL D1SK3 L1** → Introduction to Yosys
  Yosys

What it is: Open-source framework for RTL synthesis.

Use: Converts Verilog RTL code into a gate-level netlist.

Flow:

Read design (read_verilog)

Run synthesis (synth)

Map to standard cells (abc, dfflibmap)

Write output netlist (write_verilog)

Supports: FPGA flows + ASIC flows (like SKY130).

Why important: First step in RTL → GDSII design flow.

  <img width="1308" height="675" alt="image" src="https://github.com/user-attachments/assets/59dc3b02-59ea-4f82-aa6a-f727f8a0998a" />

🔹 Verifying Synthesis with Icarus Verilog & GTKWave

Step 1: Simulate RTL design with testbench → generate wave.vcd → check logic in GTKWave.

Step 2: Run synthesis in Yosys → get gate-level netlist.

Step 3: Simulate the netlist with same testbench using iverilog → generate new wave.vcd.

Step 4: Compare RTL waveform vs Gate-level waveform in GTKWave.

If both match → synthesis is correct.

  <img width="1311" height="673" alt="image" src="https://github.com/user-attachments/assets/638d40e7-7172-4a7f-8c29-47b811164cf2" />


- **7-SKY130RTL D1SK3 L2** → Logic Synthesis (Part 1)

🔹 Synthesis

Definition: Process of converting RTL (Register Transfer Level) design into a gate-level representation using standard cell library.

Input:

Verilog RTL code

Technology library (.lib)

Constraints (timing, area, power)

Output:

Gate-level netlist (Verilog)

Reports (timing, area, power)

  <img width="985" height="672" alt="image" src="https://github.com/user-attachments/assets/d35a28e1-e94c-4a0d-a4d7-d8b8f2c00c7b" />

  🔹 What is .lib?

A timing library file used in synthesis.

Describes each standard cell:

Function (logic equation)

Timing (delay, setup, hold)

Power consumption

Area

Input to synthesis → helps tool map RTL to real gates.

Why Different Flavours of Gates?

Same logic gate (e.g., NAND2) can have different drive strengths/sizes (like NAND2_X1, NAND2_X2, NAND2_X4).

Reason:

Faster cells → handle high load but consume more area/power.

Slower cells → smaller area, less power, but higher delay.

Synthesis tool chooses based on timing + power constraints.


<img width="985" height="638" alt="image" src="https://github.com/user-attachments/assets/cd6c3d71-4b54-4a07-9f51-d62a3ed2d5a8" />

 Why We Need Slower Cells?

Hold Violation: Happens when data travels too fast and reaches the next flip-flop before the hold time is satisfied.

Fix: Add delay in the path → one way is to use slower cells instead of fast cells.

Result: Slower cells increase path delay, preventing data from arriving too early → hold violation removed.

- **8-SKY130RTL D1SK3 L3** → Logic Synthesis (Part 2)

🔹 Fast Cells vs Slow Cells

| Feature               | Fast Cell                             | Slow Cell                                  |
| --------------------- | ------------------------------------- | -------------------------------------------- |
| **Delay**             | Low (quick switching)                 | High (slower switching)                      |
| **Power Consumption** | High (more dynamic power)             | Low (less power)                             |
| **Area**              | Large (bigger transistors)            | Small (smaller transistors)                  |
| **Use Case**          | Critical paths (timing-sensitive)     | Non-critical paths (hold/power optimization) |
| **Hold/Setup Effect** | May cause hold violations if too fast | Helps fix hold violations by adding delay    |


### 🔹 Labs using Yosys and Sky130 PDKs  
- **9-SKY130RTL D1SK4 L1** → Lab3: Yosys Good Mux (Part 1)

 1. Start Yosys
yosys

2. Read your Verilog design
read_verilog design.v

3. Run generic synthesis
synth

4. Map to a standard cell library (example: SKY130)
dfflibmap -liberty sky130_fd_sc_hd__tt_025C_1v80.lib
abc -liberty sky130_fd_sc_hd__tt_025C_1v80.lib

 5. Check design
stat

 6. Write gate-level netlist
write_verilog gatelevel.v

7. Visualize netlist
show gatelevel.v

  Snap Shot Of Commands To invoke Yosys
  
  <img width="1256" height="546" alt="image" src="https://github.com/user-attachments/assets/2e56b5c6-aef4-44f5-9ed6-4b72d269eacb" />

  
- **10-SKY130RTL D1SK4 L2** → Lab3: Yosys Good Mux (Part 2)

<img width="1190" height="363" alt="image" src="https://github.com/user-attachments/assets/96ebefb2-4a4f-403c-8368-8cadf6d9138a" />

  This is a gate-level netlist view from Yosys showing technology mapping. Here’s a short explanation of the mapping shown in your image:

Inputs & Buffers

i0, i1, and sel are inputs.

Each input goes through a BUF (buffer) which strengthens the signal for further gates.

Mapped Standard Cells

$53 → sky130_fd_sc_hd__clkinv_1 : This is an inverter applied on i0.

$54 → sky130_fd_sc_hd__nand2_1 : This is a 2-input NAND gate applied on i1 and sel.

AOI Gate (Complex Mapping)

$55 → sky130_fd_sc_hd__o21ai_0 : Yosys has mapped the combination of inverter and NAND into a complex gate (OR-AND-Invert) to optimize area/delay.

Inputs A1, A2, B1 are connected from previous cells.

Output Buffer

The final output y goes through a BUF for clean output drive.

✅ Summary:

Yosys converts RTL (like assign y = sel ? i1 : i0) into standard cells.

Simple logic (i0 inverter, i1 NAND) is mapped to basic cells.

Logic combination is optimized into complex cells (o21ai) to reduce area/delay.

Buffers are added for proper driving of signals.

- **11-SKY130RTL D1SK4 L3** → Lab3: Yosys Good Mux (Part 3)
  
This file is a gate‑level Verilog netlist written by a synthesis tool after mapping RTL to real SKY130 standard cells.

The top comment records the synthesis tool/version; the module line shows the block name and its ports (inputs like i0, i1, sel and outputs like y).

Internal wire declarations create nets that connect the pins of instantiated cells inside the design.

Instances such as clkinv (inverter), nand2 (2‑input NAND), and o21ai (Y = NAND(OR(A1,A2), B1)) implement the logic using SKY130 HD cells.

Pin maps like .A(sig) or .A1(sig) connect signals to each cell’s pins; each instance drives or consumes the declared wires.

Final assign statements hook the module’s outputs to the appropriate internal nets driven by those cell instances.

Functionally, this particular mix realizes a 2:1 mux structure, so tracing from inputs through these gates to the outputs reveals the mux behaviour


  <img width="901" height="503" alt="image" src="https://github.com/user-attachments/assets/3f888ce5-f776-40e9-8601-6cf03e741823" />


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

