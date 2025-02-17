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


#TASK 6 -TO BUILD AN APPLICATION


**Automatic Light System** 

 **Project Description**  
 This project implements an **Automatic Light System** that turns lights ON or OFF based on ambient light conditions. It uses an **LDR (Light Dependent Resistor) and a microcontroller (such as Arduino)** to automate lighting based on the environment's brightness. The system is useful for energy efficiency and smart home automation.

**Features**  
✅ Automatic switching of lights based on ambient light intensity  
✅ Low power consumption  
✅ Adjustable sensitivity  
✅ Can be extended for IoT-based remote control  

**Hardware Requirements**  
- Arduino Uno / ESP8266 (or any microcontroller)  
- Light Dependent Resistor (LDR)  
- Relay module  
- LED or 230V bulb (with proper relay)  
- Resistors (10kΩ, 1kΩ)  
- Power supply (5V or as required)  

**Software Requirements**  
- Arduino IDE  

**Usage**  
 Open the code in **Arduino IDE**  
 Upload the code to **Arduino**  
 Connect the circuit as per the diagram  
 Observe the light turning ON/OFF automatically based on brightness  

**Code Explanation**  
- Reading sensor values from LDR  
- Decision-making using threshold values  
- Controlling relay module for light operation  

// Define pins
const int LDR_PIN = A0;    // LDR sensor connected to analog pin A0
const int RELAY_PIN = 7;   // Relay connected to digital pin 7

// Set the threshold value for darkness (Adjust based on testing)
const int THRESHOLD = 500; // Lower value means less light

void setup() {
    pinMode(RELAY_PIN, OUTPUT); // Set relay pin as output
    digitalWrite(RELAY_PIN, HIGH); // Initially turn OFF the light (Relay is active LOW)
    Serial.begin(9600); // Initialize Serial Monitor
}

void loop() {
    int ldrValue = analogRead(LDR_PIN); // Read LDR sensor value
    Serial.print("LDR Value: ");
    Serial.println(ldrValue); // Print LDR value for debugging

    if (ldrValue < THRESHOLD) {
        digitalWrite(RELAY_PIN, LOW); // Turn ON the light
        Serial.println("Light ON");
    } else {
        digitalWrite(RELAY_PIN, HIGH); // Turn OFF the light
        Serial.println("Light OFF");
    }

    delay(500); // Small delay to avoid rapid switching
}
