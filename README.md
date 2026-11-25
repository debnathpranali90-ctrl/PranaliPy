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
# PranaliPy
Customized CPython 3.12 — Bytecode Insight Mode
 0671071fcfe8c7c7d2c6faffd5de15034d93f12c
