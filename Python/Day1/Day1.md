# Day 1 — Setup + Python Basics

## Goal for Day 1

Learn how to:

- Install Python
- Install VS Code
- Install Git
- Run Python programs
- Understand variables
- Use input and output
- Practice 10 beginner scripts

---

# 1. Install Required Tools

## Install Python

Download and install Python:

https://www.python.org/downloads/

### Important

During installation:

✔ Check **Add Python to PATH**

---

## Install VS Code

Download:

https://code.visualstudio.com/

Install normally.

Recommended extensions:

- Python
- Pylance

---

## Install Git

Download:

https://git-scm.com/downloads

Install with default settings.

---

# 2. Verify Installation

Open terminal / command prompt.

Run:

```bash
python --version
git --version
```

If Python does not work:

```bash
python3 --version
```

Expected output:

```text
Python 3.x.x
git version x.x.x
```

---

# 3. Create Workspace

Create learning folder:

```bash
mkdir python-journey
cd python-journey
mkdir day1
cd day1
```

Open in VS Code:

```bash
code .
```

---

# 4. First Program — Hello World

Create file:

`hello.py`

Write:

```python
print("Hello, World!")
```

Run:

```bash
python hello.py
```

Output:

```text
Hello, World!
```

---

# 5. Variables

Variables store data.

## Example

```python
name = "Nagesh"
age = 21
height = 5.8
is_student = True

print(name)
print(age)
print(height)
print(is_student)
```

Output:

```text
Nagesh
21
5.8
True
```

---

# 6. Python Data Types

| Type | Example | Meaning |
|------|---------|---------|
| str | "hello" | text |
| int | 10 | integer |
| float | 5.8 | decimal |
| bool | True | true/false |

---

# 7. Check Variable Type

```python
name = "Nagesh"
print(type(name))
```

Output:

```text
<class 'str'>
```

---

# 8. Input

Take value from user.

## Example 1

```python
name = input("Enter name: ")
print(name)
```

---

## Example 2

```python
age = int(input("Enter age: "))
print(age)
```

---

# 9. Output

Print values.

```python
name = "Nagesh"
print(name)
```

---

# 10. Practice Exercises (10 Scripts)

---

## Exercise 1 — Print Your Name

File: `name.py`

```python
print("Nagesh")
```

---

## Exercise 2 — Add Two Numbers

File: `add.py`

```python
a = 10
b = 20
print(a + b)
```

---

## Exercise 3 — User Name Input

File: `input_name.py`

```python
name = input("Enter your name: ")
print(name)
```

---

## Exercise 4 — Age After 5 Years

File: `future_age.py`

```python
age = int(input("Enter age: "))
print(age + 5)
```

---

## Exercise 5 — Square Number

File: `square.py`

```python
n = int(input("Enter number: "))
print(n * n)
```

---

## Exercise 6 — Celsius to Fahrenheit

File: `temp.py`

```python
c = float(input("Enter Celsius: "))
f = (c * 9/5) + 32
print(f)
```

---

## Exercise 7 — Swap Variables

File: `swap.py`

```python
a = 5
b = 10

a, b = b, a

print(a)
print(b)
```

---

## Exercise 8 — Simple Interest

File: `interest.py`

```python
p = 1000
r = 5
t = 2

si = (p * r * t) / 100

print(si)
```

---

## Exercise 9 — Full Name

File: `fullname.py`

```python
first = input("First name: ")
last = input("Last name: ")

print(first + " " + last)
```

---

## Exercise 10 — Mini Calculator

File: `calculator.py`

```python
a = int(input("Enter first number: "))
b = int(input("Enter second number: "))

print("Add:", a + b)
print("Sub:", a - b)
print("Mul:", a * b)
print("Div:", a / b)
```

---

# 11. Git Practice

Inside `day1` folder run:

```bash
git init
git add .
git commit -m "Day 1 Python basics"
```

---

# 12. End of Day Checklist

Complete these:

- [ ] Python installed
- [ ] VS Code installed
- [ ] Git installed
- [ ] Hello World done
- [ ] Variables understood
- [ ] Input/output understood
- [ ] 10 scripts completed
- [ ] Git commit completed

---

# 13. Extra Practice (Optional)

Do these if time remains.

---

## Reverse Name

```python
name = input("Enter name: ")
print(name[::-1])
```

---

## Area of Rectangle

```python
length = float(input("Length: "))
width = float(input("Width: "))

area = length * width

print(area)
```

---

## Average of 3 Numbers

```python
a = int(input())
b = int(input())
c = int(input())

avg = (a + b + c) / 3

print(avg)
```

---

# 14. Day 1 Outcome

After Day 1 you can:

- Write basic Python scripts
- Take input
- Print output
- Use variables
- Run Python files
- Start coding daily
- Save work using Git