# Performance Benchmark in RMLL
**Performance Benchmark in RMLL** is an experimental benchmark test written in RMLL (Reduced-Multipurpose Low Level Language). It counts how much simple additions the CPU can do in a second four times, then counts how much simple+complex math calculations (add,remove,multiply,divide,sin,cos,exponential) it can do under a second four times.

## What it does & Features

- Calculate how much additions the CPU can do under a second four times
- Calculate how much set of math instructions (add,remove,multiply,divide,sin,cos,exponential) the CPU can do under a second)
- Support for x86_64 CPUs (No support on recent compilers) and LPP_EXP (Lythe's Portable Picocomputer Experimental)

## Planned Features

- ~~Multicore (Multiprocessing) support in x86_64 and~~ support to benchmark both microGPUs on LPP_EXP
- RAM Performance Testing
- Configurable test cycle count
- Bus latency testing between CPU, Memory Controller and both microGPU (Only for LPP_EXP)
- Simple graphics testing with both of LPP's microGPUs

## Usage
Simply load the bin file to the lpp emulator and run.
x86_64 code will remain for legacy purposes incase the compiler development will progress with that architecture too but with current plans x86_64 development for the compiler is indefinitely halted.

- ~~On x86_64 use the compiled file or use the interpreter.~~
- On LPP emulator simply load the compiled .bin file into the Program ROM slot.

## Personal Notes
RMLL and the LPP_EXP will evolve together as RMLL meant to be mostly for LPP, the reason I went with RMLL is cause I needed something faster to work with than machine code and pure ASM but something which wouldn't require engineering complexity of making a custom C compiler just for my hardware or customizing one to be able to use my FPGA based memory controller, while the target hardware is nowhere in release condition it's likely I'll be able to release an emulator for it next year and finish either the compiler or interpreter enough to release for the public later this year or early next year! In a way it's my entry attempt to studying hardware design and step-up from my recent low-level programming challenges like creating keygens for challenges and early 2000s games whose owners give me permission to practice my reverse engineering skills on their abandonware products.
RMLL supposed to be close to instruction level like ASM but while offering many advantages of low level languages which is why it won't feature loops, try-catch functions natively but support direct register manipulation in LPP and simulated registry manipulation in x86_64.
