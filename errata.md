# Errata for *Programming with 64-Bit ARM Assembly Language*


On **page 14** [technical accuracy]:
 
The caption for Figure 1-3 is “Instruction format for data processing instructions” And the text discusses bits in ARM instructions. But the figure shows command line instructions for compiling and running a program.
]

***

On **page 54** [code]:
 
In the commented line:

// W0 is the return code and will be what we

W0 register is not used in the source code, X0 is rather used and the line should display `// X0 is the return code and will be what we`
]

***

On **page 148** [code]:
 
In the lines:

STR   W1, [FP, #-4]    // Store b
STR   W2, [FP, #-8]    // Store c

The offsets should be positive, not negative because FP was initialized with `SUB   FP, SP, #16` . In listing 6-6, the FP offsets are correctly positive.
]

***

On **page 165** [Code, Technical Accuracy]:
 
The code "ldr X1, =timespecsec" uses the incorrect lable. It should be "ldr X1, =timespecnano".
]
