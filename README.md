# 16-bit CPU (Verilog)

This is a simple 16-bit CPU designed and implemented using Verilog.

## Features
- ALU with basic operations (ADD, SUB, AND, OR, etc.)
- Register File
- Instruction Decoder
- Control Unit
- Memory Interface

## File Structure
- `alu.v` – ALU module
- `control_unit.v` – Control logic
- `register_file.v` – General purpose registers
- `cpu_top.v` – Top module
- `tb_cpu.v` – Testbench

## How to Run

### ✅ Option 1: Run with Icarus Verilog + GTKWave

#### **Compile and simulate:**
```bash
iverilog -o cpu.vvp cpu_top.v tb_cpu.v
vvp cpu.vvp
```

### ✅ Option 2: Run on ModelSim

#### 🛠️ Step-by-step:

1. **Open ModelSim.**

2. **Create a new project:**
   - Go to `File > New > Project`
   - Set project name: `16_bit_CPU`
   - Choose a location to save the project
   - Uncheck **"Copy project to folder"** (optional)
   - Click **Next** and then **Finish**

3. **Add source files:**
   - Right-click inside the **Project** window
   - Select **Add Existing File...**
   - Add all `.v` files from the `src/` and `tb/` folders

4. **Compile files:**
   - Select all files in the Project tab
   - Right-click > **Compile > Compile Selected**

5. **Simulate the design:**
   - Open your testbench file (e.g., `tb_cpu.v`)
   - Go to `Simulate > Start Simulation`
   - In the **Library** tab, select `work.tb_cpu` (or your testbench module)
   - Click **OK**

6. **View waveforms:**
   - In the transcript window, type:
     ```
     add wave *
     run 500ns
     ```
   - Adjust simulation time as needed.

