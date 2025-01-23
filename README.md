# Tcl Proc Unexpected Return Value

This repository demonstrates a subtle bug in a Tcl procedure.  The `get_value` procedure is intended to return 0 when the input is 0 and 1 otherwise. However, due to a minor error in the conditional statement, it always returns 1.

The `bug.tcl` file contains the erroneous code, and `bugSolution.tcl` provides the corrected version.

## Bug Description

The issue lies in the conditional statement `if {$x == 0}`.  While seemingly correct, the problem arises when the input `x` is explicitly 0. A more robust approach is needed.