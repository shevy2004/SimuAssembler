# Assembler Project
The Assembler Project is a tool designed to simplify the process of assembling code written in a
custom assembly-like language. It facilitates encoding instructions, handling parameters, and
managing various aspects of assembly code.

## Features
Instruction Encoding: Implement an efficient encoding mechanism for assembly instructions 
using a custom format. This encoding process is designed to support a 15-bit instruction set,
where designated bit positions are allocated for fixed patterns, addressing methods, and opcodes.

Custom Assembly Language: Utilize a specialized assembly language that enables the definition
and manipulation of instructions and operands tailored to specific requirements.

Parameter Handling: Manage a variety of parameter types, including immediate values,
register-based operands, and memory addresses, all in accordance with a predefined bit structure.

Debugging and Error Handling: Provide comprehensive error handling and debugging capabilities to ensure 
precise instruction processing and facilitate effective troubleshooting throughout the development process.

## Key Files
**run:** The compiled assembler executable.  
**makefile:** Defines the build process.

## Build the Project
To build the project, use the provided Makefile:
> make
This will compile all the necessary files and create the shevy.as executable.

## Running the Project
To run the project, use the following command:
./run file1 file2 ... fileN 
Important Note on File Names:

When specifying input files, omit the .as suffix. The assembler will automatically
add .as to the input file names.Important Note on File Names.

## Input Files
Input files should be in .as format and must include valid assembly
code that adheres to the specified language syntax.

## Output Files
For each input file, the assembler generates the following output files:

- .am file: Contains the input file after macro expansion.
- .ob file: The object file that includes the compiled machine code.
- .ent file: Lists the entry points defined in the assembly code (if any).
- .ext file: Details external references used in the assembly code (if any).

## Binary Translation Process
- During the assembly process, each instruction in the source code is
converted into binary machine code through the following steps:

- Instruction Encoding: Each instruction is transformed into binary, with both the operation 
code (opcode) and operands encoded based on the chosen addressing mode (e.g., immediate, direct, or indirect).

- Label Resolution: Operands that are labels are replaced with their respective memory
addresses from the symbol table. External references are noted and marked in the binary output.

- A, R, E Fields: Each binary word includes A, R, and E fields to facilitate proper linkage and loading
of the machine code.

## Error Handling
The assembler incorporates comprehensive error checking to identify and report issues such as syntax errors,
undefined symbols, undefined operations, and other problems encountered during the assembly process.

## Memory Management
The project demonstrates advanced memory management techniques in C, including:

Efficient allocation and deallocation of memory
Effective use of dynamic memory allocation
Prevention of memory leaks through meticulous resource management
Optimization of data structures to minimize memory usage
