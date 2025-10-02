

	<summary>Task 1 and 2  </summary>
	
# Day 0 
We start by creating a high-level model of the entire RISC-V processor using C code, which acts as a clear specification of how the processor should behave. Using tools like RISC-V GCC, we compile and run applications on this model to verify that it works correctly. Once we are confident that the C model accurately represents the processor, we transition to writing the actual hardware description in Verilog. This Verilog code includes only the processor’s core logic and instruction set, while peripherals and other modules—called IP blocks—are kept separate and reused as needed. These IP blocks may include analog components, pre-designed macros, or gate-level netlists that have already been proven and validated. By integrating the processor core with these peripherals and IP blocks, we build a complete System on Chip (SoC). To ensure everything functions as expected, we run the same applications on the Verilog hardware model and check that its output matches the behavior of the original C specification. It’s important to note the key difference between microcontrollers and microprocessors: microcontrollers are complete systems on a single chip, including CPU, memory, and peripherals, optimized for embedded, specific tasks with low cost and power consumption; microprocessors, on the other hand, consist only of the CPU core and require external memory and peripherals, making them more powerful and flexible for complex systems like PCs. After the Verilog RTL is finalized, it’s converted into gate-level logic—made up of AND, OR gates, flip-flops, and transistors—without any high-level constructs like if-statements. This stage involves placing and routing these gates to create a physical layout, which is saved in a GDSII file. The GDSII file contains the necessary information for the chip fabricator to manufacture the design. Before sending to the factory (a step called “tape-out”), the design undergoes strict checks such as Design Rule Checks (DRC) and Layout Versus Schematic (LVS). Once the chips are produced (“tape-in”), they are connected to peripherals and programmed. We verify that the output from the physical chip matches the expected outputs from previous stages, ensuring consistency. The entire process typically takes about 14 months due to testing and production cycles, and our processors usually run at speeds between 100 MHz and 130 MHz. Interestingly, the original Arduino boards used a RISC-V chip as well.


## Yosys

<img width="575" alt="yosys" src="Photos/Screenshot from 2025-09-20 21-01-08.png">
<img width="575" alt="yosys" src="Photos/Screenshot from 2025-09-20 21-02-48.png">

## Iverilog

<img width="702" alt="iverilog" src="Photos/Screenshot from 2025-09-20 21-03-36.png">
<img width="702" alt="iverilog" src="Photos/Screenshot from 2025-09-20 21-04-25.png">

## NGSpice

<img width="702" alt="iverilog" src="Photos/Screenshot from 2025-09-20 21-22-51.png">

## GTKWave

<img width="604" alt="gtkwave2" src="Photos/Screenshot from 2025-09-20 23-31-01.png">


## Magic

<img width="604" alt="gtkwave2" src="Photos/Screenshot from 2025-09-20 21-29-20.png">

<img width="1008" alt="gtkwave1" src="Photos/Screenshot from 2025-09-20 21-29-53.png">
<img width="1008" alt="gtkwave1" src="Photos/Screenshot from 2025-09-20 21-29-56.png">


# Open Lane

## Dependencies 

<img width="604" alt="gtkwave2" src="Photos/Screenshot from 2025-09-20 21-35-18.png">
<img width="1008" alt="gtkwave1" src="Photos/Screenshot from 2025-09-20 21-36-25.png">
<img width="1008" alt="gtkwave1" src="Photos/Screenshot from 2025-09-20 21-36-34.png">

## PDK Tools

<img width="604" alt="gtkwave2" src="Photos/Screenshot from 2025-09-20 22-49-43.png">

<img width="1008" alt="gtkwave1" src="Photos/Screenshot from 2025-09-20 22-49-52.png">

