# VHDL Counter Bug
This repository demonstrates a common bug in VHDL code: a missing 'else' statement in a 'case' or 'if' statement within a process.  The bug can lead to unexpected behavior or off-by-one errors.

## The Bug
The `buggy_counter.vhdl` file contains a counter that increments on each rising clock edge. However, it only handles the case when the internal counter reaches its maximum value; it is missing an `else` clause to handle other cases. This omission can result in incorrect counting or simulation behavior.

## The Solution
The `fixed_counter.vhdl` file provides a corrected version. The addition of an `else` statement ensures that the counter always behaves predictably.

## How to Reproduce
1.  Simulate `buggy_counter.vhdl` using a VHDL simulator (like ModelSim, GHDL, etc.).
2.  Observe the counter's behavior.  It might not increment correctly, stall, or exhibit unexpected behavior.
3.  Simulate `fixed_counter.vhdl`. The counter will increment correctly.

## Lesson Learned
Always ensure that all conditions within an 'if' or 'case' statement within a VHDL process are handled properly with an appropriate 'else' or 'when others' statement, to prevent unexpected behavior or bugs.