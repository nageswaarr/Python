# Python Mastery Roadmap

> A topic-first curriculum for becoming job-ready in Python — covering core language, intermediate patterns, data structures, and professional-grade development.

---

## Phase 1 — Core Python

### 1. Python Basics

The foundation of everything. Master these before moving on.

- Variables, data types, and `None`
- Type conversion (`int()`, `str()`, `float()`, etc.)
- Operators and operator precedence
- Input / output (`input()`, `print()`, f-strings)
- String methods and formatting
- Truthiness and boolean logic

**Tools:** Python REPL, VS Code, Git  
**Resources:** [Python Official Tutorial](https://docs.python.org/3/tutorial/) · [Corey Schafer – YouTube](https://www.youtube.com/c/Coreyms)

---

### 2. Data Structures

Python's built-in collections are central to almost every program.

- Lists — indexing, slicing, mutation
- Tuples — immutability and packing/unpacking
- Sets — uniqueness and set operations
- Dictionaries — key-value access, `.get()`, `.items()`
- Slicing syntax and sequence unpacking (`a, *b = ...`)

**Tools:** Python REPL  
**Resources:** [Python Data Structures Docs](https://docs.python.org/3/tutorial/datastructures.html)

---

### 3. Control Flow

Shape how your programs make decisions and repeat work.

- `if` / `elif` / `else`
- `for` loops (iterating lists, ranges, dicts)
- `while` loops
- `break`, `continue`, `pass`
- Nested loops and pattern printing

**Tools:** LeetCode (Easy), HackerRank  
**Resources:** [Exercism – Python Track](https://exercism.org/tracks/python) · [Codewars](https://www.codewars.com/)

---

### 4. Functions

Write reusable, composable logic.

- Defining and calling functions
- Positional args, `*args`, keyword args, `**kwargs`
- Default parameter values
- Return values and early returns
- Lambda functions
- List / dict / set comprehensions

**Tools:** LeetCode (Easy–Medium)  
**Resources:** [Python Functions Docs](https://docs.python.org/3/tutorial/controlflow.html#defining-functions) · [Corey Schafer](https://www.youtube.com/c/Coreyms)

---

### 5. Recursion

A pattern that unlocks tree traversal, divide-and-conquer, and backtracking.

- Base case and recursive case
- Call stack mental model
- Factorial, Fibonacci, and sum of digits
- Recursive list flattening
- Memoisation basics

**Tools:** LeetCode, Pen and paper for stack tracing

---

### 6. Files and Error Handling

Read, write, and protect your programs from failure.

- Opening files — `open()`, modes (`r`, `w`, `a`)
- The `with` statement (context managers)
- Reading lines, writing text, working with paths
- `try` / `except` / `else` / `finally`
- Raising and creating custom exceptions
- `pathlib` for cross-platform file paths

**Tools:** VS Code, Terminal  
**Resources:** [Python I/O Docs](https://docs.python.org/3/tutorial/inputoutput.html)

---

### 7. Modules and Packages

Organise code properly and leverage the ecosystem.

- `import` and `from ... import`
- Standard library highlights — `os`, `sys`, `math`, `datetime`, `random`, `json`
- Installing packages with `pip`
- Creating and using virtual environments (`venv`)
- Structuring your own modules

**Tools:** pip, venv, Terminal  
**Resources:** [PyPI](https://pypi.org/) · [Python Modules Docs](https://docs.python.org/3/tutorial/modules.html)

---

## Phase 2 — Intermediate Python + DSA

### 8. Object-Oriented Programming (OOP)

Model real-world problems as objects and classes.

- Classes, instances, and `__init__`
- Instance vs. class attributes
- Inheritance and `super()`
- Polymorphism and method overriding
- Encapsulation — public, protected, private conventions
- Dunder / magic methods (`__str__`, `__repr__`, `__len__`, `__eq__`)

**Tools:** VS Code, GitHub  
**Resources:** [Corey Schafer – OOP](https://www.youtube.com/watch?v=ZDa-Z5JzLYM) · [Python Classes Docs](https://docs.python.org/3/tutorial/classes.html)

---

### 9. Advanced Python Features

Power features used in production code and libraries.

- Iterators and the iterator protocol (`__iter__`, `__next__`)
- Generators and `yield` — lazy evaluation
- Decorators — wrapping functions and preserving metadata (`@functools.wraps`)
- Context managers — `__enter__` / `__exit__` and `contextlib`
- `logging` module — levels, handlers, formatters
- Type hints and `typing` module

**Tools:** VS Code, pytest  
**Resources:** [Real Python](https://realpython.com/) · [Python Docs](https://docs.python.org/3/)

---

### 10. Data Structures and Algorithms (DSA)

Core computer science knowledge for technical interviews and efficient code.

| Topic | Key Concepts |
|---|---|
| Arrays | Two pointers, sliding window, binary search |
| Sorting | Bubble, selection, insertion, merge, quick sort |
| Stack & Queue | `collections.deque`, monotonic stack |
| Linked List | Singly linked, reversal, cycle detection |
| Hash Maps | Frequency counting, anagram detection |
| Trees | BFS, DFS, BST operations |
| Recursion | Backtracking, divide and conquer |
| Complexity | Big-O time and space analysis |

**Tools:** LeetCode, NeetCode, HackerRank  
**Resources:** [NeetCode Roadmap](https://neetcode.io/) · [LeetCode](https://leetcode.com/)

---

### 11. Databases and SQL

Store and query structured data from Python programs.

- SQLite — lightweight embedded database
- CRUD — `CREATE`, `READ`, `UPDATE`, `DELETE`
- SQL joins — `INNER`, `LEFT`, `RIGHT`
- Aggregation — `GROUP BY`, `COUNT`, `SUM`, `AVG`
- MySQL / PostgreSQL connection from Python
- SQLAlchemy ORM — models, sessions, queries

**Tools:** SQLite, MySQL, SQLAlchemy  
**Resources:** [SQLite Docs](https://www.sqlite.org/docs.html) · [SQLAlchemy Docs](https://docs.sqlalchemy.org/)

---

## Phase 3 — Professional Python

### 12. Automation and Scripting

Automate the boring stuff — files, the web, and the system.

- `requests` library — HTTP GET/POST, working with JSON APIs
- Web scraping with `BeautifulSoup` — parsing HTML, extracting data
- Selenium WebDriver — browser automation, filling forms
- File and folder automation — renaming, sorting, watching directories
- Task scheduling — `schedule` library and cron jobs
- Email automation with `smtplib` and `email`

**Tools:** requests, BeautifulSoup, Selenium, schedule  
**Resources:** [Selenium Docs](https://www.selenium.dev/documentation/) · [Real Python](https://realpython.com/)

---

### 13. Backend Web Development — Flask

Build HTTP APIs and web applications.

- Flask app structure and factory pattern
- Routes — path parameters, query strings, HTTP methods
- Jinja2 templating — variables, loops, template inheritance
- REST API design — status codes, JSON responses
- Request/response lifecycle
- Basic authentication — sessions and JWT

**Tools:** Flask, Postman, SQLite  
**Resources:** [Flask Docs](https://flask.palletsprojects.com/) · [freeCodeCamp Flask](https://www.freecodecamp.org/)

---

### 14. Data Analysis

Work with data using Python's scientific stack.

- NumPy — arrays, vectorised operations, broadcasting
- Pandas — DataFrames, Series, indexing with `.loc` / `.iloc`
- Data cleaning — handling nulls, duplicates, type conversion
- Grouping and aggregation — `groupby`, `pivot_table`
- Matplotlib and Seaborn — line, bar, scatter, histogram charts
- Reading and writing CSV / Excel files

**Tools:** NumPy, Pandas, Matplotlib, Jupyter Notebook  
**Resources:** [Pandas Docs](https://pandas.pydata.org/docs/) · [NumPy Docs](https://numpy.org/doc/)

---

### 15. Concurrency and Async

Write programs that do multiple things at once.

- `threading` module — when to use threads, `Thread`, `Lock`
- `multiprocessing` — bypassing the GIL, `Pool`, shared memory
- `asyncio` — event loop, `async def`, `await`
- `aiohttp` — async HTTP client for high-throughput scraping/requests
- Choosing the right tool — I/O-bound vs. CPU-bound tasks

**Tools:** asyncio, aiohttp, concurrent.futures  
**Resources:** [Python asyncio Docs](https://docs.python.org/3/library/asyncio.html) · [Real Python – Async IO](https://realpython.com/async-io-python/)

---

### 16. Testing and Debugging

Write code you can trust and fix bugs with confidence.

- `unittest` — `TestCase`, setup/teardown, assertions
- `pytest` — fixtures, parametrize, marks, plugins
- Mocking with `unittest.mock` — patching, side effects
- VS Code debugger — breakpoints, watch expressions, call stack
- Code profiling — `cProfile`, `timeit`, identifying bottlenecks

**Tools:** pytest, VS Code debugger, cProfile  
**Resources:** [PyTest Docs](https://docs.pytest.org/) · [Real Python – Testing](https://realpython.com/pytest-python-testing/)

---

### 17. Deployment and DevOps Basics

Ship your code to production.

- Git branching strategies — feature branches, PRs, merge vs. rebase
- Environment variables and `.env` files (`python-dotenv`)
- Docker basics — `Dockerfile`, images, containers
- Deploying to Railway / Heroku / Render
- GitHub Actions — CI/CD pipelines, running tests on push

**Tools:** Docker, GitHub Actions, Railway, python-dotenv  
**Resources:** [Docker Docs](https://docs.docker.com/) · [GitHub Actions Docs](https://docs.github.com/en/actions)

---

## High-ROI Topics (Top 20%)

These appear most frequently in real projects and interviews. Prioritise these if time is limited.

| Priority | Topic |
|---|---|
| ★★★ | Dictionaries and data structures |
| ★★★ | Functions, args, and comprehensions |
| ★★★ | OOP — classes, inheritance, dunder methods |
| ★★★ | Exception handling |
| ★★★ | `requests` and REST APIs |
| ★★★ | SQL CRUD and joins |
| ★★★ | Pandas fundamentals |
| ★★ | File handling |
| ★★ | Flask routing and REST API design |
| ★★ | Decorators and context managers |
| ★★ | Debugging and testing |
| ★★ | Git and GitHub |

---

## Capstone Projects

Build these to demonstrate end-to-end skills for your portfolio.

1. **File Organiser** — scans a folder, sorts files by type/date, generates a log report
2. **CLI Expense Tracker** — CRUD app with SQLite, categories, monthly summaries
3. **REST API** — Flask task manager with auth, JSON endpoints, and pytest coverage
4. **Automation Bot** — scrapes data from a site, cleans it with Pandas, emails a daily report
5. **Full-stack App** — Flask backend + Jinja2 frontend, deployed to Railway with GitHub Actions CI

---

## Practice Platforms

| Platform | Best For |
|---|---|
| [LeetCode](https://leetcode.com/) | DSA and interview prep |
| [HackerRank](https://www.hackerrank.com/) | Domain-specific challenges |
| [Codewars](https://www.codewars.com/) | Short kata-style problems |
| [Exercism](https://exercism.org/tracks/python) | Mentored, concept-driven practice |
| [Project Euler](https://projecteuler.net/) | Math + algorithm problems |

---

## Recommended GitHub Structure

```
python/
├── phase1_core/
├── phase2_intermediate/
├── phase3_professional/
├── projects/
├── challenges/
└── README.md
```

---

## Job-Ready Checklist

- [ ] 4 public projects on GitHub with READMEs
- [ ] Daily commits — consistent green contribution graph
- [ ] 100+ coding problems solved (LeetCode / HackerRank)
- [ ] 2 projects deployed (Railway, Heroku, or Render)
- [ ] Can explain your code and walk through it in an interview
- [ ] Have read other people's Python code on GitHub
- [ ] Comfortable debugging with breakpoints (not just `print`)
- [ ] Know how to write a test for any function you write
