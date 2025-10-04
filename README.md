# 🚀 Week 2: BabySoC Fundamentals & Functional Modelling
### *From SoC Theory to Pre-Synthesis Simulation - A Complete Journey*

[![SoC](https://img.shields.io/badge/SoC-BabySoC-blue?style=for-the-badge)](#)
[![RISC-V](https://img.shields.io/badge/RISC--V-RVMYTH-green?style=for-the-badge)](#)
[![Verilog](https://img.shields.io/badge/Verilog-HDL-orange?style=for-the-badge)](#)
[![iVerilog](https://img.shields.io/badge/iVerilog-Simulator-red?style=for-the-badge)](#)
[![GTKWave](https://img.shields.io/badge/GTKWave-Waveform-purple?style=for-the-badge)](#)
[![Week](https://img.shields.io/badge/Week-2-gold?style=for-the-badge)](#)

---

## 🎯 **Week 2 Objective**

Build a comprehensive understanding of System-on-Chip fundamentals and master functional modelling of VSDBabySoC using industry-standard simulation tools (Icarus Verilog & GTKWave).

---

## 📚 **Part 1: Understanding System-on-Chip (SoC) Design**

### **What is a System-on-Chip (SoC)?**

A System-on-Chip (SoC) represents the ultimate integration philosophy in modern electronics - consolidating an entire electronic system onto a single semiconductor die. Rather than requiring multiple discrete components spread across a circuit board, an SoC packages the complete functionality into one compact, efficient chip.

**Core Philosophy**: SoCs embody the principle that integration leads to efficiency. By bringing disparate components into close physical proximity on a single die, we achieve superior performance, reduced power consumption, and minimal form factor - critical requirements for today's mobile and embedded systems.

### **Key Components of a Typical SoC**

**1. Central Processing Unit (CPU) - The Digital Brain**
- Executes instructions and manages computational tasks
- Handles decision-making, data processing, and application logic
- In modern SoCs, often multi-core for parallel processing capabilities

**2. Memory Subsystem - Data Storage Hierarchy**
- **RAM (Random Access Memory)**: Volatile, high-speed temporary storage for active operations
- **ROM/Flash**: Non-volatile storage retaining data when power is removed
- Cache hierarchies for optimized data access patterns

**3. Input/Output (I/O) Interfaces - External Communication**
- Bridges between the SoC and external world
- Includes: USB controllers, camera interfaces, audio ports, display controllers
- Protocol-specific engines (UART, SPI, I2C, PCIe)

**4. Graphics Processing Unit (GPU) - Visual Rendering Engine**
- Specialized parallel processor for graphics and multimedia
- Handles complex visual computations, gaming, video processing
- Increasingly used for general-purpose parallel computing (GPGPU)

**5. Digital Signal Processor (DSP) - Specialized Signal Processing**
- Optimized for real-time signal processing operations
- Critical for audio enhancement, video codecs, and communications
- Performs filtering, transformations, and signal conditioning

**6. Power Management Unit (PMU) - Energy Optimization**
- Regulates voltage and current distribution across the SoC
- Implements dynamic power scaling and sleep states
- Essential for battery-powered device longevity

**7. Interconnect Fabric - Internal Communication Network**
- High-speed buses (AXI, AHB, APB in ARM ecosystems)
- Enables efficient data transfer between components
- Critical for overall system performance

**8. Specialized IP Blocks**
- Wi-Fi and Bluetooth radios for wireless connectivity
- Security engines (encryption, authentication)
- Hardware accelerators for domain-specific tasks
- Sensor interfaces and analog front-ends

### **Why SoCs Matter: The Integration Advantage**

**Space Efficiency**: By collapsing multiple chips into one, SoCs enable the miniaturization that defines modern electronics - from smartphones to wearables to IoT sensors.

**Energy Optimization**: Reduced interconnect distances dramatically lower power consumption. On-chip communication is orders of magnitude more efficient than inter-chip data transfer.

**Performance Enhancement**: Proximity eliminates long wire delays, enabling higher clock frequencies and lower latency. Integrated components communicate faster than discrete systems.

**Cost Reduction**: Single-chip manufacturing amortizes costs across the entire system. Fewer components mean simpler PCB design and assembly.

**Reliability**: Fewer physical connections translate to fewer potential failure points. SoCs are inherently more robust than multi-chip solutions.

### **VSDBabySoC: A Learning-Focused SoC Implementation**

VSDBabySoC serves as an educational platform that distills SoC design principles into a manageable, comprehensible system. While simplified compared to commercial SoCs, it preserves the essential architectural concepts and design challenges.

**Core Components of VSDBabySoC:**

**1. RVMYTH - RISC-V Based CPU Core**
- Educational implementation of the RISC-V instruction set architecture
- Demonstrates fundamental processor design: fetch, decode, execute pipeline
- Provides hands-on experience with open-source CPU architectures
- Written in Transaction-Level Verilog (TL-Verilog) for clarity

**2. PLL (Phase-Locked Loop) - Clock Generation**
- Generates stable, synchronized clock signals from reference input
- 8x frequency multiplication capability
- Essential for understanding timing and synchronization in digital systems
- Bridges the analog-digital interface in mixed-signal design

**3. 10-bit DAC (Digital-to-Analog Converter) - Analog Interface**
- Converts digital processor output to analog signals
- Enables communication with real-world analog devices
- Demonstrates mixed-signal design principles
- 10-bit resolution provides 1024 discrete output levels

**System Integration**: These three IP blocks work in concert - the PLL provides synchronized timing, RVMYTH processes digital data, and the DAC interfaces with the analog domain, creating a complete functional system.

### **BabySoC's Role in the Learning Journey**

**Conceptual Foundation**: BabySoC provides a concrete implementation to anchor abstract SoC concepts. Theory becomes tangible when you can simulate, verify, and understand each component's function.

**Design Flow Experience**: Working with BabySoC exposes the complete digital design flow:
- **Functional Modelling** (RTL simulation - our current focus)
- **Synthesis** (logic optimization and technology mapping)
- **Physical Design** (placement, routing, timing closure)
- **Verification** (functional and timing validation)

**Mixed-Signal Understanding**: The integration of digital (RVMYTH) and analog (PLL, DAC) components teaches crucial mixed-signal design concepts often missing from purely digital curricula.

**Industry-Relevant Skills**: Despite its educational focus, BabySoC uses industry-standard tools (Icarus Verilog, GTKWave, Yosys) and methodologies, building directly transferable skills.

### **The Importance of Functional Modelling**

Functional modelling - simulating RTL behavior before synthesis - is the foundation of reliable digital design. It serves multiple critical purposes:

**Early Bug Detection**: Catching functional errors at the RTL stage is exponentially cheaper than finding them post-silicon. A bug caught in simulation might take hours to fix; the same bug found in fabricated silicon could cost millions.

**Design Verification**: Systematic testbench-driven verification ensures the design meets specifications before committing to physical implementation.

**Architectural Exploration**: Simulation enables rapid iteration on architectural decisions without the overhead of full synthesis and physical design.

**Understanding System Behavior**: Waveform analysis provides deep insight into how data flows through the system, how components interact, and where bottlenecks or timing issues might arise.

**Regression Testing**: Automated simulation suites catch regressions when design changes are made, ensuring new features don't break existing functionality.

### **From Theory to Practice: Our Week 2 Journey**

Understanding these fundamentals provides context for our hands-on work. We're not just running simulations - we're engaging with the core principles that govern modern digital system design. Each waveform we analyze, each signal transition we observe, represents these abstract concepts manifesting in concrete, verifiable behavior.

---

## 🛠️ **Part 2: VSDBabySoC Functional Simulation**

### **Environment Setup & Project Initialization**

**Step 1: Repository Cloning**

We begin by cloning the VSDBabySoC repository to establish our working environment:

```bash
cd ~
git clone https://github.com/manili/VSDBabySoC.git
cd VSDBabySoC/
```

<p align="center">
   <img src="Images/i4.png" alt="Cloning VSDBabySoC repository" width="90%">
</p>

*Successfully cloned the VSDBabySoC repository containing all required IP cores, testbenches, and design files.*

---

### **Step 2: TL-Verilog to Verilog Conversion**

The RVMYTH core is written in Transaction-Level Verilog (TL-Verilog), which provides higher abstraction but requires conversion to standard Verilog for simulation.

**Installing Dependencies:**
```bash
sudo apt update
sudo apt install python3-venv python3-pip

# Create virtual environment
python3 -m venv sp_env
source sp_env/bin/activate

# Install SandPiper-SaaS converter
pip install pyyaml click sandpiper-saas
```

<p align="center">
   <img src="Images/i5.png" alt="Python environment setup for SandPiper" width="90%">
</p>

*Setting up Python virtual environment and installing SandPiper-SaaS for TL-Verilog conversion.*

**Converting rvmyth.tlv to rvmyth.v:**
```bash
sandpiper-saas -i ./src/module/*.tlv -o rvmyth.v --bestsv --noline -p verilog --outdir ./src/module/
```

<p align="center">
   <img src="Images/i6.png" alt="TL-Verilog to Verilog conversion" width="90%">
</p>

*SandPiper-SaaS successfully converted rvmyth.tlv into synthesizable Verilog (rvmyth.v), ready for simulation.*

---

### **Step 3: Pre-Synthesis Functional Simulation**

Pre-synthesis simulation validates RTL functionality in an idealized zero-delay environment, focusing purely on logical correctness before timing considerations.

**Creating Output Directory & Running Simulation:**
```bash
mkdir -p output/pre_synth_sim

iverilog -o output/pre_synth_sim/pre_synth_sim.out \
    -DPRE_SYNTH_SIM \
    -I src/include \
    -I src/module \
    src/module/testbench.v

cd output/pre_synth_sim
./pre_synth_sim.out
```

<p align="center">
   <img src="Images/i1.png" alt="Pre-synthesis simulation execution" width="90%">
</p>

*Icarus Verilog compiles and executes the testbench, generating pre_synth_sim.vcd for waveform analysis.*

---

### **Step 4: Waveform Analysis in GTKWave**

**Opening the VCD File:**
```bash
gtkwave output/pre_synth_sim/pre_synth_sim.vcd
```

**Initial Waveform View - Digital Signals:**

<p align="center">
   <img src="Images/i2.png" alt="GTKWave showing digital signals" width="90%">
</p>

*Key signals displayed: **CLK** (stable clock from PLL), **reset** (system initialization), **RV_TO_DAC[9:0]** (10-bit RVMYTH output), and **OUT** (DAC output in digital view).*

---

**Analog Waveform Visualization:**

To properly view the DAC's analog output behavior, we change the display format:
1. Select the **OUT** signal
2. Right-click → Data Format → Analog → Step

<p align="center">
   <img src="Images/i3.png" alt="Changing OUT signal to analog view" width="90%">
</p>

*Configuring GTKWave to display the DAC OUT signal in analog step format for realistic visualization.*

---

**Final Analog Waveform:**

<p align="center">
   <img src="Images/i7.png" alt="DAC output in analog representation" width="90%">
</p>

*DAC output displayed as analog waveform showing the staircase conversion of digital values from RVMYTH's register r17 into analog voltage levels. The stepping behavior clearly demonstrates the 10-bit quantization of the digital-to-analog conversion process.*

---

## 🔍 **Signal Analysis & Interpretation**

### **Key Observations from Waveform Analysis:**

**CLK (Clock Signal)**:
- Stable periodic square wave generated by the PLL
- Provides timing reference for all synchronous operations
- 8x multiplication of input reference frequency

**reset (Reset Signal)**:
- Active-high initialization signal
- Ensures deterministic startup state
- Clears internal registers and state machines

**RV_TO_DAC[9:0] (RVMYTH Output)**:
- 10-bit digital data from RVMYTH's register r17
- Cycles through programmed values in the processor
- Represents processed data ready for analog conversion

**OUT (DAC Output - Analog)**:
- Real-valued analog signal reflecting DAC conversion
- Staircase pattern demonstrates discrete 10-bit quantization levels
- Each step corresponds to a change in RV_TO_DAC input
- Simulates real-world analog voltage output

### **System Behavior Verification:**

The waveforms confirm proper functional operation:
1. **Clock Domain Synchronization**: All signals properly aligned with CLK edges
2. **Reset Functionality**: System initializes correctly and begins operation post-reset
3. **Data Flow Integrity**: Digital values from RVMYTH successfully propagate through DAC
4. **Analog Conversion**: DAC accurately translates digital inputs to analog levels

---

## 🎯 **Key Learnings & Takeaways**

### **SoC Design Principles:**
- Integration of heterogeneous components (digital CPU, analog PLL/DAC) on a single system
- Importance of clock generation and distribution for synchronous operation
- Mixed-signal interface challenges and solutions

### **Functional Modelling Methodology:**
- Pre-synthesis simulation validates logic before physical implementation
- Testbench-driven verification ensures comprehensive functional coverage
- Waveform analysis provides critical insight into system behavior

### **Tool Proficiency:**
- **Icarus Verilog**: Open-source HDL simulation at RTL level
- **GTKWave**: Powerful waveform visualization and debugging
- **SandPiper-SaaS**: TL-Verilog abstraction for cleaner CPU design

### **Design Flow Understanding:**
- Conversion from high-level HDL to synthesizable RTL
- Importance of early functional verification in reducing downstream costs
- Iterative refinement through simulation-based debugging

---

## ✅ **Week 2 Achievements**

**Theoretical Foundation:**
- [x] Comprehensive understanding of SoC architecture and components
- [x] Recognition of integration advantages and design tradeoffs
- [x] Understanding of VSDBabySoC's educational role

**Practical Implementation:**
- [x] Successfully cloned and set up VSDBabySoC environment
- [x] Converted TL-Verilog RVMYTH core to standard Verilog
- [x] Executed pre-synthesis functional simulation
- [x] Analyzed waveforms in GTKWave (digital and analog views)
- [x] Verified correct operation of integrated PLL-CPU-DAC system

**Skills Developed:**
- [x] SoC architectural analysis and component integration
- [x] RTL simulation methodology and testbench usage
- [x] Mixed-signal design concepts (digital-analog interfacing)
- [x] Waveform interpretation and functional debugging
- [x] Industry-standard EDA tool operation

---

## 🚀 **Next Steps: Path Forward**

With solid functional modelling completed, the next phases of the journey include:

1. **RTL Synthesis**: Converting verified RTL to gate-level netlists
2. **Post-Synthesis Simulation (GLS)**: Validating synthesis correctness and timing
3. **Physical Design**: Floorplanning, placement, and routing
4. **Static Timing Analysis**: Ensuring timing closure across all paths
5. **Physical Verification**: DRC/LVS checks for manufacturability

---

<div align="center">

### 🎖️ **WEEK 2 STATUS: FUNCTIONAL MODELLING MASTERED**
*"From SoC fundamentals to successful pre-synthesis simulation - Foundation established!"*

[![Status](https://img.shields.io/badge/Week%202-COMPLETE-brightgreen?style=for-the-badge)](#)
[![Understanding](https://img.shields.io/badge/SoC%20Theory-MASTERED-blue?style=for-the-badge)](#)
[![Simulation](https://img.shields.io/badge/Functional%20Sim-VERIFIED-gold?style=for-the-badge)](#)

**🎯 Ready for Synthesis and Physical Design Challenges! 🚀**

</div>

---

## 📚 **References**

- **VSDBabySoC Repository**: [https://github.com/manili/VSDBabySoC](https://github.com/manili/VSDBabySoC)
- **SoC Design Fundamentals**: [SFAL-VSD SoC Journey](https://github.com/hemanthkumardm/SFAL-VSD-SoCJourney/tree/main/11.%20Fundamentals%20of%20SoC%20Design)
- **RISC-V ISA**: [https://riscv.org/](https://riscv.org/)
- **TL-Verilog**: [Redwood EDA Documentation](https://www.redwoodeda.com/)
- **Icarus Verilog**: [http://iverilog.icarus.com/](http://iverilog.icarus.com/)
- **GTKWave**: [http://gtkwave.sourceforge.net/](http://gtkwave.sourceforge.net/)

---

*This documentation represents Week 2 of the SFAL-VSD SoC Design Journey - From architectural understanding to functional verification.*
