# VHDL Integer Range and Signal Assignment Subtlety

This repository demonstrates a subtle bug in VHDL related to the use of integer ranges and signal assignments.  The code appears to be a simple counter, but it fails to function correctly due to an oversight in how the integer range is handled.

## Bug Description

The provided VHDL code implements a counter that counts from 0 to 15.  While the code seems logically sound, it may not simulate correctly or synthesize into working hardware. The issue stems from the way the `internal_count` signal is handled within the `process`.  The problem is a common one when dealing with integer ranges. The solution involves explicitly handling the upper bound of the range to prevent potential overflow issues.