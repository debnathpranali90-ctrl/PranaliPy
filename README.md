# PranaliPy – Bytecode Insight Mode

My customized Python flavour based on CPython 3.12.

## Changes Made
- Modified `Python/bytecodes.c`.
- Added a diagnostic message in the `BINARY_OP` execution logic.
- Regenerated `Python/generated_cases.c.h`.

## Diagnostic Message
`[PranaliPy] Executing BINARY_OP`

## Build and Test
The customized CPython interpreter was built using Visual Studio Build Tools on Windows.

The runtime test produced the correct output: `42`.

## Source
Original CPython repository: https://github.com/python/cpython

## Author
Pranali Debnath