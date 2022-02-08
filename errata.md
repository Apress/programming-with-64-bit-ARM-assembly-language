# Errata for *Programming with 64-Bit ARM Assembly Language*


On **page 14** [technical accuracy]:
 
The caption for Figure 1-3 is “Instruction format for data processing instructions” And the text discusses bits in ARM instructions. But the figure shows command line instructions for compiling and running a program.
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

***

On **page 284** [Code, Technical Accuracy]:
 
The code `B.LE  notequal` should be replaced by `B.GE  notequal`. The existing code returns incorrect result (i.e., 0 if they are equal, else 1).
]

***

On **page 285** [Code]:
 
Immediately after the loop (i.e., after `B.NE  loop`), the code should store S1 to memory at location runsum. This is necessary for the right values to be passed to fpcomp function later on.
]
