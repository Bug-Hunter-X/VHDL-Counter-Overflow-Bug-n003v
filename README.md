# VHDL Counter Overflow Bug

This repository demonstrates a common error in VHDL: an integer counter that doesn't handle potential overflow. The `buggy_counter.vhdl` file contains the buggy code, while `fixed_counter.vhdl` provides a corrected version.

## Problem

The original code increments the counter without checking whether it has reached its maximum value.  When the counter reaches 15, the next increment results in an overflow. The behavior after overflow is implementation-defined and could lead to unpredictable results, including incorrect counting, simulation errors, or even synthesis issues.

## Solution

The `fixed_counter.vhdl` file shows the corrected implementation.  It checks if the counter has reached the maximum value before incrementing, preventing overflow and ensuring correct behavior.

This simple example highlights the importance of careful consideration of boundary conditions when designing digital circuits.