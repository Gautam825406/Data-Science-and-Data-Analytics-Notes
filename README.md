# 🐍 Python Interview Preparation – Core Concepts

This repository contains **detailed, interview-oriented explanations of Python fundamentals**.  
Each topic is written in a **clear, concise, and human-friendly manner**, suitable for **technical interviews and concept revision**.

---

## ❓ What are the Key Features of Python?

Python is a versatile and popular programming language known for its **simplicity, elegant syntax, and vast ecosystem of libraries**.  
Below are the key features that make Python stand out.

### 🔹 Key Features of Python

1. **Interpreted and Interactive**  
   Python uses an interpreter, which executes code line by line. This makes it ideal for rapid prototyping, testing, and debugging.

2. **Easy to Learn and Read**  
   Python’s syntax closely resembles plain English, reducing cognitive load for beginners and improving maintainability for experienced developers.

3. **Cross-Platform Compatibility**  
   Python runs seamlessly on Windows, Linux, and macOS without requiring platform-specific changes.

4. **Modular and Scalable**  
   Code can be organized into reusable modules and packages, making applications scalable and easier to maintain.

5. **Rich Library Ecosystem**  
   The Python Package Index (PyPI) hosts over **260,000 libraries**, supporting web development, data science, automation, and AI.

6. **Exceptionally Versatile**  
   Python is widely used in web development, scientific computing, machine learning, data analytics, and automation.

7. **Automatic Memory Management**  
   Python handles memory allocation and deallocation internally, shielding developers from low-level memory concerns.

8. **Dynamically Typed**  
   Variable types are determined at runtime, simplifying variable declaration and manipulation.

9. **Object-Oriented**  
   Python follows object-oriented principles where everything is treated as an object with attributes and methods.

10. **Extensible**  
    Python can integrate with C/C++ using its C-language API for performance-critical components.

---

## ⚙️ How Is Python Executed?

Python follows a **compile-and-interpret** execution model.

### 🔹 Compilation & Interpretation

- **Bytecode Compilation**  
  Python source code is compiled into platform-independent bytecode.

- **On-the-fly Interpretation**  
  The Python Virtual Machine (PVM) executes the bytecode line by line.

This dual approach ensures portability and ease of debugging.

---

### 🔹 Bytecode vs Machine Code

- Python compiles to bytecode, not machine code.
- Bytecode is executed by the PVM.
- This may be slower than direct machine code execution but ensures cross-platform compatibility.

---

### 🔹 Source Code to Bytecode: Compilation Steps

1. **Lexical Analysis** – Breaks code into tokens  
2. **Syntax Parsing** – Builds parse trees  
3. **Semantic Analysis** – Validates logical correctness  
4. **Bytecode Generation** – Produces executable bytecode

---

### 🔹 Just-In-Time (JIT) Compilation

JIT optimizes performance by compiling frequently executed code sections into machine code at runtime, improving execution speed.

---

### 🔹 Bytecode Disassembly Example


import dis

def example_func():
    return 15 * 20

dis.dis(example_func)


LOAD_CONST 300
RETURN_VALUE


What is PEP 8 and Why Is It Important?

PEP 8 is Python’s official style guide, promoting readability, consistency, and maintainability.

🔹 Key Design Principles

Readability

Consistency

One clear way to write code

🔹 Base Rules

Indentation: 4 spaces

Line length: 79 characters

Use blank lines appropriately

🔹 Naming Conventions

Classes: CamelCase

Functions & variables: snake_case

Modules: lowercase

🔹 PEP 8 Example
import os

def walk_directory(path):
    for dirpath, dirnames, filenames in os.walk(path):
        for filename in filenames:
            file_path = os.path.join(dirpath, filename)
            print(file_path)

walk_directory('/path/to/directory')

🧠 Memory Allocation & Garbage Collection in Python
🔹 Memory Allocation

Objects are stored in the heap

Small objects handled by obmalloc

Large memory blocks obtained from OS

🔹 Garbage Collection

Python uses:

Reference Counting

Cycle-Detecting Garbage Collector

🔹 Python vs C/C++

Python: Automatic, safer, slower

C/C++: Manual, faster, error-prone

📦 Built-in Data Types in Python
🔹 Immutable Data Types

int, float, complex

bool

str

tuple

frozenset

bytes

NoneType

🔹 Mutable Data Types

list

set

dict

bytearray

memoryview

🔁 Mutable vs Immutable Objects
🔹 Key Distinctions

Mutable: Can be modified

Immutable: Cannot be modified

🔹 Examples

Mutable: list, set, dict

Immutable: tuple, string, int

# Immutable
text = "Hello"
# text[0] = "M"  # TypeError

# Mutable
my_list = [1, 2, 3]
my_list.append(4)

⚠️ Exception Handling in Python
🔹 Components

try

except

else

finally

🔹 Example
try:
    risky_operation()
except IndexError:
    handle_index_error()
except Exception as e:
    handle_generic_error()
finally:
    cleanup()

🔹 Raising Exceptions
def divide(a, b):
    if b == 0:
        raise ZeroDivisionError("Divisor cannot be zero")
    return a / b

🔹 Resource Management with with
with open("example.txt", "r") as file:
    data = file.read()

📋 Difference Between List and Tuple
Feature	List	Tuple
Mutability	Mutable	Immutable
Performance	Slower	Faster
Syntax	[]	()
🗂️ How Do You Create a Dictionary in Python?
🔹 Dictionary Creation Methods
# Literal
student = {"name": "John", "age": 21}

# Using dict()
student = dict(name="John", age=21)

# Using zip()
keys = ["a", "b"]
values = [1, 2]
dict(zip(keys, values))

### ⚖️ Difference Between == and is

== → Compares values

is → Compares memory addresses (identity)

🔹 Best Practice

Use == for value comparison

Use is for None checks







🎯 Purpose of This Repository

✔ Interview preparation
✔ Concept clarity
✔ Python fundamentals
✔ Clean explanations




