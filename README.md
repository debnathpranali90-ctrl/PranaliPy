# PranaliPy – Bytecode Insight Mode

A customised CPython 3.12 flavour created as a Python Flavour assignment.

PranaliPy adds a diagnostic message to the `BINARY_OP` bytecode execution logic. This helps observe an internal part of Python's execution process.

## Project Flow

Python Source Code → Compilation → Bytecode → CPython Evaluation Loop → BINARY_OP → Diagnostic Message → Result

## Customisation

File modified: `Python/bytecodes.c`

Added code:

```c
PySys_WriteStderr("[PranaliPy] Executing BINARY_OP\n");
```

This message is displayed whenever the interpreter executes the `BINARY_OP` instruction.

## Generated File

`Python/generated_cases.c.h`

This file was regenerated after modifying the bytecode definition.

## Example

```python
A = type('A', (), {'__add__': lambda self, other: 42})
print(A() + A())
```

Output:

```text
42
```

PranaliPy also displays its diagnostic message during execution.

## Build

```cmd
PCbuild\build.bat -p x64
```

## Test

```cmd
PCbuild\amd64\python.exe -c "A=type('A',(),{'__add__':lambda self,other:42}); print(A()+A())"
```

## Learning Outcomes

- Understanding CPython source code
- Exploring Python bytecode
- Modifying the interpreter
- Regenerating source files
- Building and testing customised CPython

## Original Source

https://github.com/python/cpython

## Author

Pranali Debnath  
B.Tech Computer Science and Engineering  
ICFAI University, Tripura
