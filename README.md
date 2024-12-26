# Transistor-Level 4-Bit Carry Look-Ahead Adder  

## Overview  
This repository contains the transistor-level design and implementation of a high-speed 4-bit **Carry Look-Ahead Adder (CLA)** using 180nm CMOS technology. The project includes detailed pre- and post-layout simulations, leveraging **NGSPICE** for circuit validation and **MAGIC** for layout design. The design is optimized for low propagation delay and high-speed operation. A Verilog-based structural description is also provided for FPGA implementation and hardware validation.  

---

## Features  
- **Transistor-Level Design**: MOSFET-based implementation of logic gates (NOT, AND, OR, XOR) and D flip-flops using TSPC topology.  
- **High-Speed Performance**: Propagation delay minimized using hierarchical propagate/generate logic.  
- **Pre- and Post-Layout Simulations**:  
  - Pre-layout: Timing and delay analysis using NGSPICE.  
  - Post-layout: MAGIC layout design with area, timing, and power optimizations.  
- **FPGA Validation**: Verilog-based structural modeling with functional verification on FPGA.  
- **Technology Parameters**: Designed using a 180nm process, λ = 0.09μm, VDD = 1.8V.  

---

## Design Highlights  

### Logic Design  
- Carry Look-Ahead Adder implemented to minimize carry propagation delay.  
- Hierarchical computation of generate and propagate signals for parallel carry computation.  

### Gate Design  
- Complementary CMOS logic used for all gates.  
- Sizing optimized for performance: \( W_P/W_N = 20λ/10λ \).  

### Timing Metrics  
- **Setup Time (Tsu)**: 0.13ns  
- **Hold Time (Th)**: 0s  
- **Clock-to-Q Delay (Tcq)**: 0.075ns  
- **Maximum Delay (Tpd)**: 0.56ns  

---

## Pre- vs Post-Layout Comparison  

| Metric                  | Pre-Layout | Post-Layout |  
|-------------------------|------------|-------------|  
| Maximum Rise Time       | 0.58ns     | 0.56ns      |  
| Maximum Fall Time       | 0.52ns     | 0.37ns      |  
| Minimum Clock Period    | 0.785ns    | 0.765ns     |  
| Maximum Clock Frequency | 1.27GHz    | 1.30GHz     |  

---

## Tools Used  
- **NGSPICE**: Pre-layout simulations for functionality and timing analysis.  
- **MAGIC**: Layout design and post-layout simulations.  
- **Verilog**: Structural modeling for FPGA validation.  
- **FPGA Board**: Functional testing and verification with real-time examples.  

---

## Results  
- **Pre-Layout Simulation**: Verified functionality with examples using NGSPICE.  
- **Post-Layout Analysis**: Reduced delay and improved clock frequency.  
- **FPGA Output**: Correct sum and carry outputs verified on FPGA with LEDs.  

---

## Layout Details  
- **Area**: \( 201.78μm × 170.91μm = 34,486.223μm^2 \)  
- **Floor Plan**: Includes hierarchical arrangement of logic gates and flip-flops.  

---

## References  
1. **CMOS VLSI Design**: Weste & Harris  
2. **Digital Integrated Circuits**: Jan Rabaey  
3. **GeeksforGeeks**  

---

For a detailed walkthrough, check the project report.  
