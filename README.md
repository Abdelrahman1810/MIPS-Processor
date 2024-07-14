# MIPS Processor Verilog Design

This repository contains the Verilog implementation of a MIPS processor core with pipeline, hazard solution, and exception handling, along with the corresponding testbenches.
## Imge Arch
![Architecture](Documents/Architecture.png)

## Features

- **MIPS Processor Core**: The processor core is implemented in Verilog, supporting the following MIPS instructions:
  - Arithmetic and Logical Instructions: `ADD`, `ADDI`, `SUB`, `AND`, `OR`, `NOR`, `SLT`, `SLTI`
  - Load and Store Instructions: `LW`, `SW`
  - Branch Instructions: `BEQ`, `BNE`
- **Pipeline Architecture**: The processor core is designed with a 5-stage pipeline (Fetch, Decode, Execute, Memory, Writeback) to improve performance.
- **Hazard Detection and Forwarding**: The pipeline design includes hazard detection and forwarding mechanisms to handle data hazards and control hazards.
- **Exception Handling**: The processor core can handle exceptions, such as illegal instructions and address errors, and provides a dedicated exception handler.

## Directory Structure

- `RTL/`: Contains the Verilog source files for the MIPS processor core, including the pipeline stages and hazard detection logic.
- `testbench/`: Includes the Verilog testbench files for testing the MIPS processor core, covering both normal operation and exception handling.
- `DataMemory.dat`: Initial data memory content.
- `ExceptionInstruction.dat`: Initial instruction memory content for exception handling.
- `ExceptionRegisterData.dat`: Initial register file content for exception handling.
- `InstructionData.dat`: Initial instruction memory content.
- `RegisterData.dat`: Initial register file content.
- `TestCode.s`: MIPS assembly code for testing the processor core.
- `Exception_TestCode.s`: MIPS assembly code for testing the exception handling.
- `run.tcl`: Tcl script for running the normal operation testbench.
- `runException.tcl`: Tcl script for running the exception handling testbench.

## Assembly Code Description

The two MIPS assembly code files, TestCode.s and Exception_TestCode.s, are used to test the functionality of the MIPS processor core.

1. TestCode.s:
- This file contains a set of MIPS instructions that test the basic functionality of the processor, including arithmetic, logical, load, store, and branch operations.
- The code performs various calculations, loads and stores data, and tests the branch instructions.
- That MIPS assembly code performs the following tasks:
    * Initializes an array with 6 elements: 5, 9, 19, 12, 1, and 15.
    * Finds the maximum (MAX) and minimum (MIN) values in the array and stores it in registers ($t2) and ($t3) in order.
    * Calculates the sum of all elements in the array and stores it in registers ($s0).

2. Exception_TestCode.s:
- This file contains a set of MIPS instructions that test the exception handling capabilities of the processor core.
- That MIPS assembly code tests two types of exceptions:

    1. Overflow Exception: The code intentionally causes an overflow exception by adding a large value to a register, causing the result to exceed the maximum representable value.
    2. Invalid Instruction Exception: The code uses an invalid instruction (*SWL*) to trigger an exception.

## Getting Started
To get started with this repository, follow these steps:
> [!IMPORTANT]
> You need to have [QuestaSim](https://support.sw.siemens.com/en-US/) installed on your machine or any other Verilog simulator.

1. Clone the repository:

   ```ruby
   git clone https://github.com/Abdelrahman1810/MIPS-Processor-Verilog.git
   ```

2. Navigate to the project directory:

3. Run the normal operation testbench:
   ```ruby
   do run.tcl
   ```

4. Run the exception handling testbench:
   ```ruby
   do runException.tcl
   ```

The testbench outputs will display the results of the MIPS processor core execution, including any exceptions that may occur.
you can check wave for *Instruction* and *regmem*

## Contributing
If you find any issues or have suggestions for improvement, feel free to submit a pull request or open an issue in the repository. Contributions are always welcome!

## Contact info 💜
<a href="https://linktr.ee/A_Hassanen" target="_blank">
  <img align="left" alt="Linktree" width="180px" src="https://app.ashbyhq.com/api/images/org-theme-wordmark/b3f78683-a307-4014-b236-373f18850e2c/d54b020a-ff53-455a-9d52-c90c0f4f2081.png" />
</a> 
<br>
