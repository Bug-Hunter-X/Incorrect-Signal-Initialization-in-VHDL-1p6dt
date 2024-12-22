# Incorrect Signal Initialization in VHDL

This repository demonstrates a common but subtle error in VHDL code: incorrect signal initialization. The example shows a simple process that registers input data and outputs the registered value. However, the initial value assigned to the internal signal is incorrect, leading to potential issues.

## Bug Description
The signal `data_reg` is initialized to `x"00"`, which might not be appropriate for all possible data types. If `data_reg` is meant to be an unsigned or signed type, then it should be initialized to a valid value for that type.

## Solution
The solution provides the correct initialization of the signal depending on whether it's intended to be a standard logic vector, unsigned, or signed type.