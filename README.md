This repository demonstrates a subtle memory management bug in Objective-C related to weak properties and custom setters.  The bug arises when a custom setter for a weak property doesn't properly handle the case where the new value is the same as the old value.  This can lead to premature release of the referenced object, causing crashes or unexpected behavior.

The `bug.m` file contains the buggy code. The solution, presented in `bugSolution.m`, addresses the issue by only releasing the old reference when assigning a new value.

This example highlights the importance of careful memory management when working with weak references in Objective-C.  Always ensure your custom setters correctly manage the lifecycle of the object referenced by the property.