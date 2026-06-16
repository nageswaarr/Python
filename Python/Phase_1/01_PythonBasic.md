# Python Basics

> Beginner-to-advanced roadmap for mastering Python Basics — the core syntax, built-in types, operators, and I/O that every Python program is built on.

---

## Table of Contents

1. [Introduction](#1-introduction)
2. [Fundamentals](#2-fundamentals)
3. [Core Concepts](#3-core-concepts)
4. [Intermediate Concepts](#4-intermediate-concepts)
5. [Advanced Concepts](#5-advanced-concepts)
6. [Ecosystem & Tooling](#6-ecosystem--tooling)
7. [Architecture & Patterns](#7-architecture--patterns)
8. [Performance & Optimization](#8-performance--optimization)
9. [Security & Best Practices](#9-security--best-practices)
10. [Debugging & Developer Tooling](#10-debugging--developer-tooling)
11. [Related Technologies](#11-related-technologies)
12. [Learning Resources](#12-learning-resources)

---

## 1. Introduction

### What is Python Basics

- Python is a high-level, interpreted, general-purpose programming language
- Designed for readability — uses indentation instead of braces for code blocks
- Dynamically typed — variable types are resolved at runtime
- Batteries-included — ships with a rich standard library

### Core Purpose & Problem It Solves

- Eliminates the boilerplate of lower-level languages for scripting and automation
- Bridges the gap between readable pseudocode and executable programs
- Single language usable across scripting, data, backend, and tooling

### Where It Fits in the Stack

- Scripting layer — automating tasks, file processing, CLI tools
- Backend — web servers, APIs, microservices
- Data layer — analysis, ML pipelines, notebooks
- Glue language — orchestrating other tools and processes

### Key Use Cases

- Automation scripts and file manipulation
- REST API development
- Data cleaning and analysis
- CLI tooling
- Rapid prototyping

### Environment & Runtime Overview

- CPython — the reference interpreter (most common)
- Python version management via `pyenv`
- Interactive REPL via `python3` in the terminal
- Script execution via `python3 script.py`

### Installation & Setup Basics

- Install Python 3.x from `python.org` or via OS package manager
- Verify with `python3 --version`
- Set up `venv` for isolated environments *(see `Modules & Packages/`)*
- Configure VS Code with the Python extension

### Workflow Basics

- Write `.py` files in an editor (VS Code, PyCharm)
- Run scripts directly from the terminal
- Use the REPL for quick experimentation
- Commit working code to Git after each feature

---

## 2. Fundamentals

### Syntax Rules

- Indentation (4 spaces) defines code blocks — not braces or keywords
- Statements end with a newline — no semicolons required
- Comments start with `#`
- Multi-line statements use `\` or implicit continuation inside brackets

### Variables

- Assignment with `=` — no `var`, `let`, or `const`
  - `name = "Alice"`
  - `count = 0`
  - `pi = 3.14`
- Variable names — lowercase with underscores (`snake_case`)
- Multiple assignment — `x, y, z = 1, 2, 3`
- Augmented assignment — `+=`, `-=`, `*=`, `/=`

### Built-in Data Types

- `int` — whole numbers: `42`, `-7`, `0`
- `float` — decimal numbers: `3.14`, `-0.5`, `1e10`
- `str` — text: `"hello"`, `'world'`
- `bool` — `True` or `False`
- `NoneType` — the `None` singleton, represents absence of value

### Type Conversion

- `int("42")` → `42`
- `float("3.14")` → `3.14`
- `str(100)` → `"100"`
- `bool(0)` → `False`, `bool(1)` → `True`
- `type(value)` — returns the type of any object

### Truthiness

- Falsy values: `0`, `0.0`, `""`, `[]`, `{}`, `None`, `False`
- Truthy values: any non-zero number, non-empty string, non-empty collection
- Used implicitly in `if` conditions

### Input and Output Basics

- `print()` — writes to stdout
  - `print("Hello, world!")`
  - `print(name, age, sep=", ")`
  - `print("done", end="")`
- `input()` — reads a line from stdin as a string
  - `name = input("Enter your name: ")`
  - Always returns `str` — convert explicitly when needed

---

## 3. Core Concepts

### Strings

- String literals
  - Single quotes: `'hello'`
  - Double quotes: `"hello"`
  - Triple quotes for multi-line: `"""..."""`
- String operations
  - Concatenation: `"Hello" + " " + "World"`
  - Repetition: `"ab" * 3` → `"ababab"`
  - Membership: `"ell" in "hello"` → `True`
- Indexing and slicing
  - `s[0]` — first character
  - `s[-1]` — last character
  - `s[1:4]` — characters at index 1, 2, 3
  - `s[::2]` — every second character
- Common string methods
  - `.upper()`, `.lower()`, `.title()`
  - `.strip()`, `.lstrip()`, `.rstrip()`
  - `.replace(old, new)`
  - `.split(sep)`, `sep.join(iterable)`
  - `.startswith(prefix)`, `.endswith(suffix)`
  - `.find(sub)`, `.count(sub)`
  - `.isdigit()`, `.isalpha()`, `.isspace()`

### String Formatting

- f-strings (preferred): `f"Hello, {name}!"`
  - Inline expressions: `f"{2 + 2}"` → `"4"`
  - Format spec: `f"{price:.2f}"` → `"3.14"`
- `.format()` method: `"Hello, {}".format(name)`
- `%` formatting (legacy): `"Hello, %s" % name`

### Operators

- Arithmetic — `+`, `-`, `*`, `/`, `//`, `%`, `**`
  - `/` always returns `float`
  - `//` floor division (returns `int` for `int` operands)
  - `%` modulo — remainder after division
  - `**` exponentiation: `2 ** 10` → `1024`
- Comparison — `==`, `!=`, `<`, `>`, `<=`, `>=`
  - Always return `bool`
- Logical — `and`, `or`, `not`
  - Short-circuit evaluation
- Assignment — `=`, `+=`, `-=`, `*=`, `/=`, `//=`, `%=`, `**=`
- Identity — `is`, `is not`
  - Compares object identity, not value
  - Use `is None`, never `== None`
- Membership — `in`, `not in`

### Operator Precedence

- High to low: `**` → unary `-`/`+` → `*`, `/`, `//`, `%` → `+`, `-` → comparisons → `not` → `and` → `or`
- Use parentheses to make intent explicit

### `None` and Null Safety

- `None` is a singleton — test with `is None`
- Default return value of functions that have no `return` statement
- Common in optional parameters and uninitialized state

---

## 4. Intermediate Concepts

### Advanced String Techniques

- Raw strings — `r"\n"` treats backslash literally
- Byte strings — `b"hello"` for binary data
- String interning — identical string literals may share memory
- `str.encode()` / `bytes.decode()` — converting between `str` and `bytes`
- `textwrap.dedent()` — normalising indentation in multi-line strings

### Numeric Types and Precision

- `int` in Python 3 has arbitrary precision — no overflow
- `float` follows IEEE 754 — subject to floating-point rounding
- `decimal.Decimal` — exact decimal arithmetic for financial calculations
- `fractions.Fraction` — exact rational arithmetic
- `complex` — built-in complex numbers: `3 + 4j`

### Dynamic Typing and Type Checking

- Variables are labels — they can be rebound to any type
- `isinstance(obj, type)` — preferred type check (supports inheritance)
- `type(obj) is SomeType` — exact type check (ignores subclasses)
- Duck typing — "if it walks like a duck, it's a duck"
- Type hints for documentation *(see `Advanced Python/`)*

### Mutability vs. Immutability

- Immutable types: `int`, `float`, `str`, `tuple`, `frozenset`, `bytes`
  - Cannot be changed after creation — operations return new objects
- Mutable types: `list`, `dict`, `set`, `bytearray`
  - Changed in-place — beware of shared references
- Implications for function arguments and default parameter values

### Scope and Variable Lookup (LEGB)

- Local — variables defined in the current function
- Enclosing — variables in an outer (enclosing) function
- Global — module-level variables
- Built-in — Python's built-in names (`len`, `print`, `range`)
- `global` keyword — declares a variable as module-level inside a function
- `nonlocal` keyword — binds to the nearest enclosing scope variable

### `print()` and `input()` in Depth

- `print(sep=" ", end="\n", file=sys.stdout, flush=False)` — all parameters
- Redirecting output: `print("msg", file=sys.stderr)`
- `input()` always returns `str` — always convert explicitly
- `sys.stdin.read()` — reading multi-line input in competitive programming

---

## 5. Advanced Concepts

### Python's Data Model

- Everything is an object — `int`, `str`, `function`, `class` are all objects
- `id()` — returns the memory address of an object
- Reference counting and the garbage collector (`gc` module)
- `__slots__` — restricting instance attributes to save memory

### Interning and Object Caching

- Small integers (`-5` to `256`) are cached by CPython
- Short strings may be interned — `sys.intern(s)` forces interning
- `is` on strings can give surprising results due to interning
- Implications for identity vs. equality checks

### Bitwise Operators

- `&` — bitwise AND
- `|` — bitwise OR
- `^` — bitwise XOR
- `~` — bitwise NOT
- `<<` — left shift
- `>>` — right shift
- Use cases: flag masking, permission systems, low-level data processing

### The Global Interpreter Lock (GIL)

- CPython's GIL prevents true parallel execution of Python threads
- Impact on CPU-bound multithreading *(see `Concurrency/`)*
- No GIL impact on I/O-bound threading
- GIL-free alternatives: `multiprocessing`, PyPy, sub-interpreters (Python 3.12+)

### Memory Management Internals

- Reference counting — objects are freed when count reaches 0
- Cycle collector — breaks reference cycles
- Memory arenas — CPython allocates memory in blocks
- `sys.getrefcount(obj)` — inspect the reference count of an object
- `weakref` module — references that don't prevent garbage collection

### Operator Overloading

- Implementing `__add__`, `__sub__`, `__mul__`, `__truediv__` for custom types
- `__eq__` and `__hash__` — must be consistent for use in sets and dicts
- `__lt__`, `__le__` etc. for custom ordering
- `functools.total_ordering` — auto-derive comparison methods from `__eq__` + one other

---

## 6. Ecosystem & Tooling

### Interpreters & Runtime

| Tool / Library | Description |
| -------------- | ----------- |
| `CPython`      | The reference interpreter — default on all platforms |
| `PyPy`         | JIT-compiled Python — faster for CPU-heavy code |
| `IPython`      | Enhanced REPL with syntax highlighting and magic commands |
| `Jupyter`      | Notebook-based interactive Python environment |
| `pyenv`        | Manage multiple Python versions on one machine |

### Formatters & Linters

| Tool / Library | Description |
| -------------- | ----------- |
| `black`        | Opinionated, zero-config code formatter |
| `isort`        | Sorts and organises import statements automatically |
| `flake8`       | Linter combining `pyflakes`, `pycodestyle`, and `mccabe` |
| `pylint`       | Comprehensive static analysis with scoring |
| `ruff`         | Fast Rust-based linter and formatter, superset of `flake8` |

### Editors & IDE Integration

| Tool / Library | Description |
| -------------- | ----------- |
| VS Code + Python extension | IntelliSense, debugging, linting in one editor |
| PyCharm        | Full-featured Python IDE with refactoring tools |
| Vim / Neovim   | Terminal-based editing with `python-lsp-server` |

### Package Management

| Tool / Library | Description |
| -------------- | ----------- |
| `pip`          | Default package installer for Python packages |
| `venv`         | Built-in virtual environment creation *(see `Modules & Packages/`)* |
| `pipx`         | Install CLI tools in isolated environments |
| `poetry`       | Dependency management and packaging with lock files |
| `uv`           | Ultra-fast pip/venv replacement written in Rust |

---

## 7. Architecture & Patterns

### Script Structure

- Shebang line — `#!/usr/bin/env python3` for executable scripts
- Module docstring at the top of the file
- Imports grouped: standard library → third-party → local
- `if __name__ == "__main__":` guard — prevents code running on import

### Naming Conventions (PEP 8)

- Variables and functions — `snake_case`
- Constants — `UPPER_SNAKE_CASE`
- Classes — `PascalCase`
- Private names — `_single_underscore` prefix
- Name mangling — `__double_underscore` prefix

### Single-Responsibility Scripts

- One script = one clear purpose
- Configuration at the top (constants), logic in functions, execution at the bottom
- Avoid global mutable state in scripts

### Constants and Configuration

- Module-level constants in `UPPER_CASE`
- Group related constants in a dedicated `config.py` or `constants.py`
- Use `os.environ` or `.env` files for environment-specific values *(see `Deployment/`)*

### Guard Clauses

- Return early on invalid conditions rather than deeply nesting `if` blocks
- Reduces cognitive complexity and right-drift

### EAFP vs. LBYL

- EAFP (Easier to Ask Forgiveness than Permission) — `try/except` style (Pythonic)
- LBYL (Look Before You Leap) — check conditions before acting
- Python culture prefers EAFP for most cases

---

## 8. Performance & Optimization

### String Concatenation

- Avoid `+` in loops — each creates a new string object
- Use `"".join(list_of_strings)` for building strings iteratively
- f-strings are faster than `.format()` and `%` for formatting

### Integer and Float Operations

- Integer operations are exact — prefer `int` over `float` when possible
- Avoid repeated `float` comparisons — use `math.isclose()` instead
- `decimal.Decimal` adds precision at the cost of performance

### Avoiding Repeated Global Lookups

- Local variable access is faster than global or built-in lookups in hot loops
- Cache `len`, `range`, or other built-ins as local references in tight loops

### REPL and Script Startup

- `python -c "..."` for single-line execution without a file
- `python -O` strips `assert` statements and `__debug__` blocks for production
- `python -m cProfile script.py` — profile script execution *(see Section 10)*

### Efficient I/O

- `print()` with `flush=False` (default) — buffered output is faster
- Read files in chunks rather than loading entire file into memory
- `sys.stdout.write()` is faster than `print()` in tight output loops

---

## 9. Security & Best Practices

### Input Validation

- Never trust `input()` — always validate and convert explicitly
- Use `int(input())` inside a `try/except ValueError` block
- Never use `eval()` or `exec()` on user-supplied strings

### `eval()` and `exec()` Dangers

- `eval()` executes arbitrary Python expressions — never on untrusted input
- `exec()` executes arbitrary statements — same risk, greater scope
- Alternatives: `ast.literal_eval()` for safely parsing Python literals only

### Avoiding Mutable Default Arguments

- `def fn(items=[])` — the list is shared across all calls (common bug)
- Use `None` as default, then assign inside the function body

### Environment and Secrets

- Never hardcode credentials or API keys in `.py` files
- Use environment variables (`os.environ["KEY"]`)
- `.env` files via `python-dotenv` — exclude from version control *(see `Deployment/`)*

### Dependency Awareness

- Pin dependencies in `requirements.txt` or `pyproject.toml`
- Audit packages with `pip-audit` before adding them
- Prefer well-maintained packages with active communities

### Code Maintainability

- Follow PEP 8 — use `black` to enforce automatically
- Write docstrings for every public function and module
- Avoid single-letter variable names outside of loop counters and math formulas
- Keep functions short — one clear purpose per function

---

## 10. Debugging & Developer Tooling

### Built-in Debugging

- `print()` debugging — quick but remove before committing
- `breakpoint()` — built-in since Python 3.7, drops into `pdb`
- `pdb` commands: `n` (next), `s` (step), `c` (continue), `p expr` (print), `q` (quit)
- `python -m pdb script.py` — start script under the debugger

### VS Code Debugger

- Set breakpoints by clicking the gutter in VS Code
- Launch configurations in `.vscode/launch.json`
- Watch expressions, call stack, variable inspector
- Step over / into / out of functions
- Conditional breakpoints for targeted debugging

### Introspection Tools

- `type(obj)` — object's class
- `dir(obj)` — list all attributes and methods
- `help(obj)` — display the docstring in the terminal
- `vars(obj)` — object's `__dict__`
- `id(obj)` — memory address

### Linting and Static Analysis

- `ruff check .` — fast lint and auto-fix
- `flake8` — style and logic warnings
- `pylint` — in-depth analysis with scoring
- `mypy` — static type checking via type hints *(see `Advanced Python/`)*

### Profiling

- `python -m cProfile -s cumtime script.py` — cumulative time per function
- `timeit` module — benchmark small code snippets accurately
- `line_profiler` (`kernprof`) — line-by-line timing
- `memory_profiler` — track memory usage per line

### Logging

- `logging` module — preferred over `print()` for anything beyond scripts
  - Levels: `DEBUG`, `INFO`, `WARNING`, `ERROR`, `CRITICAL`
  - `logging.basicConfig(level=logging.DEBUG)`
  - Formatters, handlers, and rotating file logs *(see `Advanced Python/`)*

---

## 11. Related Technologies

- Control Flow *(see `Control Flow/`)*
- Functions and Recursion *(see `Functions/`)*
- Data Structures — lists, dicts, sets *(see `Data Structures/`)*
- File and Error Handling *(see `Files & Errors/`)*
- Modules and Packages *(see `Modules & Packages/`)*
- Object-Oriented Programming *(see `OOP/`)*
- Advanced Python features *(see `Advanced Python/`)*
- Type hints and static analysis *(see `Advanced Python/`)*
- Concurrency and the GIL *(see `Concurrency/`)*
- Deployment and environment variables *(see `Deployment/`)*

---

## 12. Learning Resources

### Official Documentation

| Resource                              | URL                                                          |
| ------------------------------------- | ------------------------------------------------------------ |
| Python 3 Official Tutorial            | https://docs.python.org/3/tutorial/                          |
| Python Built-in Types Reference       | https://docs.python.org/3/library/stdtypes.html              |
| Python Built-in Functions Reference   | https://docs.python.org/3/library/functions.html             |
| PEP 8 — Style Guide for Python Code   | https://peps.python.org/pep-0008/                            |
| PEP 257 — Docstring Conventions       | https://peps.python.org/pep-0257/                            |

### Guides & Tutorials

| Resource                              | URL                                                          |
| ------------------------------------- | ------------------------------------------------------------ |
| Corey Schafer — Python Beginner Series | https://www.youtube.com/playlist?list=PL-osiE80TeTt2d9bfVyTiXJA-UTHn6WwU |
| freeCodeCamp — Python Full Course     | https://www.youtube.com/watch?v=rfscVS0vtbw                  |
| Real Python — Python Basics           | https://realpython.com/python-basics/                        |
| Programming with Mosh — Python        | https://www.youtube.com/watch?v=_uQrJ0TkZlc                  |
| Tech With Tim — Python Beginner       | https://www.youtube.com/c/TechWithTim                        |

### References

| Resource                              | URL                                                          |
| ------------------------------------- | ------------------------------------------------------------ |
| Python Cheatsheet (gto76)             | https://github.com/gto76/python-cheatsheet                  |
| Comprehensive Python Cheatsheet       | https://www.pythoncheatsheet.org/                            |
| W3Schools Python Reference            | https://www.w3schools.com/python/                            |
| Programiz Python Reference            | https://www.programiz.com/python-programming                 |

### Ecosystem & Tooling Resources

| Resource                              | URL                                                          |
| ------------------------------------- | ------------------------------------------------------------ |
| Black Formatter Docs                  | https://black.readthedocs.io/en/stable/                      |
| Ruff Linter Docs                      | https://docs.astral.sh/ruff/                                 |
| pyenv GitHub                          | https://github.com/pyenv/pyenv                               |
| pip User Guide                        | https://pip.pypa.io/en/stable/user_guide/                    |
| VS Code Python Extension Docs         | https://code.visualstudio.com/docs/python/python-tutorial    |

### Practice Resources

| Resource                              | URL                                                          |
| ------------------------------------- | ------------------------------------------------------------ |
| Exercism — Python Track               | https://exercism.org/tracks/python                           |
| Codewars — Python Kata                | https://www.codewars.com/kata/search/python                  |
| HackerRank — Python Domain            | https://www.hackerrank.com/domains/python                    |
| LeetCode — Easy Problems              | https://leetcode.com/problemset/?difficulty=EASY             |
| Project Euler                         | https://projecteuler.net/                                    |