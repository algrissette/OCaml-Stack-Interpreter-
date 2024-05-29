# OCaml-Stack-Interpreter-
# Stack-Based Interpreter

## Overview
This project involves creating a stack-based interpreter for a high-level programming language. The interpreter should correctly execute a series of programs and generate the expected trace outputs. The programs are written in a concrete syntax, and interpreting their compiled commands should yield specific sequences of traces.

## Setup
1. **Download and Unzip**: Download the interpreter project from the provided link and unzip it.
2. **Directories**: The project contains the following directories: `src`, `data`, and `lib`.

### Moving Files to the Right Place
1. **Source Code**:
   - Create a new package called `interpreter` in your workspace.
   - Place the source files in this package.
   - Ensure that the interpreter code is placed in the `src/interpreter` directory.

2. **Data**:
   - Copy the contents of the `data` directory to the `data` folder in your workspace.

3. **Library**:
   - If any external libraries are required, add them to the `lib` directory and include them in your project's build path.

### Modifying the .xml Files
- If necessary, modify the XML configuration files to specify custom settings or input parameters.

### Run Configurations
- Create run configurations as needed to execute the interpreter with different inputs or settings.

## Example Programs
In this section, we present some programs written in the concrete syntax of the high-level language along with their expected traces. Interpreting their compiled commands using the stack interpreter should yield the same trace.

### Sequence of Traces
- **Expected Trace:** `["2" :: "1" :: ε]`

#### Factorial
- **Expected Trace:** `["3628800" :: ε]`
```ocaml
let rec fact x =
  if x <= 0 then 1
  else x * fact (x - 1)
in trace (fact 10)
