# Samsung-RISC-V
 # Samsung RISC-V Talent Development Program - 
 # Task 1-

This repository contains the results of Task 1, which involved setting up the RISC-V development environment and replicating the steps performed in the provided C-based and RISC-V-based lab videos.

*1. Environment Setup*

* *RISC-V Toolchain Installation:* 
    * The RISC-V toolchain was installed following the instructions in the PDF document provided. 
    * The VDI link mentioned in the PDF was used for accessing the necessary resources. 
* *GitHub Repository:* A new GitHub repository named "samsung-riscv" was created to store the results of this task.

*2. Lab Replication*

* *C-based Lab:* 
    * The steps outlined in the C-based lab video were replicated on the local machine. 
    * Snapshots of the k…
# Task2- RISC-V Optimization Analysis

This repository contains the results of an analysis comparing the effects of different optimization levels (-O1 and -Ofast) on the performance of a simple C program when compiled for the RISC-V architecture.

*1. Methodology*

1. *C Program:* A simple C program (see my_program.c) was written for this analysis. 
2. *Compilation:* The C program was compiled using the RISC-V GCC compiler with the following optimization flags:
    * -O1: Enables basic optimizations.
    * -Ofast: Enables aggressive optimizations.
3. *Simulation:* The compiled binaries were executed using the SPIKE simulator. 
4. *Performance Measurement:* Execution time of each program within the SPIKE simulator was measured.
5. *Object Dump Analysis:* 
    * riscv-objdump …
    * 
# Task3-RISC-V Instruction Analysis

This repository contains the results of an analysis of 15 unique RISC-V instructions found within a sample application. 

*Instructions:*

1. *Compilation:* The application was compiled for the RISC-V architecture using riscv64-unknown-elf-gcc.
2. *Disassembly:* riscv-objdump was used to generate assembly code from the compiled binary.
3. *Instruction Identification:* 15 unique instructions were identified from the disassembled output.
4. *Encoding:* For each instruction, the 32-bit instruction code was determined based on the RISC-V instruction encoding specifications.

*Instructions.txt*

This file contains a list of the 15 identified instructions, their types, and their 32-bit instruction codes in hexadecimal format.

*Note:*

* This analysis was performed for a specific application and may vary for different programs.
* Refer to the official RISC-V documentation for the most accurate and up-to-date information on instruction encoding.
