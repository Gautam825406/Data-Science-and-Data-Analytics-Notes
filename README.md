# 🐍 Python Interview Preparation – Complete Notes

This repository contains **all-in-one, detailed, interview-focused notes on Python fundamentals**.  
Each topic is explained in a **clear, concise, and human way**, exactly how you should answer in a **technical interview**.

---

## ❓ What are the Key Features of Python?

Python is a versatile and popular programming language known for its **simplicity, elegant syntax, and vast ecosystem of libraries**.  
Below are the key features that make Python stand out.

### 🔹 Key Features of Python

1. **Interpreted and Interactive**  
   Python uses an interpreter to execute code line by line, making debugging easier and supporting rapid prototyping.

2. **Easy to Learn and Read**  
   Python’s syntax closely resembles plain English, reducing cognitive load for beginners and improving code readability.

3. **Cross-Platform Compatibility**  
   Python runs on Windows, Linux, and macOS without requiring platform-specific changes.

4. **Modular and Scalable**  
   Code can be organized into reusable modules, functions, and packages, enabling scalable application development.

5. **Rich Library Ecosystem**  
   The Python Package Index (PyPI) hosts over **260,000 libraries**, covering web development, data analytics, AI, ML, and automation.

6. **Exceptionally Versatile**  
   Python is used in web applications, scientific computing, data science, machine learning, scripting, and automation.

7. **Automatic Memory Management**  
   Python automatically handles memory allocation and deallocation, freeing developers from low-level memory concerns.

8. **Dynamically Typed**  
   Variable types are determined at runtime, making coding faster and more flexible.

9. **Object-Oriented**  
   Python supports object-oriented programming where everything is treated as an object with attributes and methods.

10. **Extensible**  
    Python can integrate with C/C++ using its C-language API for performance-critical components.

---

## ⚙️ How Is Python Executed?

Python follows a **compile-and-interpret** execution model.

### 🔹 Compilation & Interpretation

- **Bytecode Compilation**  
  Python source code is compiled into platform-independent bytecode.

- **On-the-fly Interpretation**  
  The Python Virtual Machine (PVM) executes bytecode instructions line by line.

This approach provides both **portability and ease of debugging**.

---

### 🔹 Bytecode vs Machine Code

- Python does not compile directly to machine code.
- Bytecode is executed by the PVM.
- This adds portability but can be slower than languages like C/C++.

---

### 🔹 Source Code to Bytecode: Compilation Steps

1. **Lexical Analysis** – Breaks source code into tokens  
2. **Syntax Parsing** – Builds parse trees  
3. **Semantic Analysis** – Validates logical correctness  
4. **Bytecode Generation** – Produces executable bytecode  

---

### 🔹 Just-In-Time (JIT) Compilation

JIT improves performance by compiling frequently executed code segments into machine code at runtime, speeding up execution.

---

### 🔹 Bytecode Disassembly Example

```python
import dis

def example_func():
    return 15 * 20

dis.dis(example_func)
Output:

nginx
Copy code
LOAD_CONST 300
RETURN_VALUE
📘 What is PEP 8 and Why Is It Important?
PEP 8 is Python’s official style guide, ensuring readability, consistency, and maintainability across Python projects.

🔹 Design Principles
Readability

Consistency

One obvious way to do things

🔹 Base Rules
Indentation: 4 spaces

Line length: 79 characters

Use blank lines to separate logical sections

🔹 Naming Conventions
Classes: CamelCase

Functions & variables: snake_case

Modules: lowercase

🔹 PEP 8 Example
python
Copy code
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

Large memory blocks allocated directly from the OS

🔹 Garbage Collection
Python uses:

Reference Counting

Cycle-Detecting Garbage Collector

🔹 Python vs C/C++
Python: Automatic, safer, but slower

C/C++: Manual, faster, but error-prone

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

🔁 Difference Between Mutable and Immutable Objects
🔹 Key Distinctions
Mutable: Can be modified after creation

Immutable: Cannot be modified after creation

🔹 Examples
Mutable: list, set, dict

Immutable: tuple, string, int

python
Copy code
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
python
Copy code
try:
    risky_operation()
except IndexError:
    handle_index_error()
except Exception as e:
    handle_generic_error()
finally:
    cleanup()
🔹 Raising Exceptions
python
Copy code
def divide(a, b):
    if b == 0:
        raise ZeroDivisionError("Divisor cannot be zero")
    return a / b
🔹 Resource Management with with
python
Copy code
with open("example.txt", "r") as file:
    data = file.read()
📋 Difference Between List and Tuple
Feature	List	Tuple
Mutability	Mutable	Immutable
Performance	Slower	Faster
Syntax	[]	()

🗂️ How Do You Create a Dictionary in Python?
python
Copy code
# Literal
student = {"name": "John", "age": 21}

# Using dict()
student = dict(name="John", age=21)

# Using zip()
keys = ["a", "b", "c"]
values = [1, 2, 3]
dict(zip(keys, values))
⚖️ Difference Between == and is
== → Compares values

is → Compares memory addresses (identity)

🔹 Best Practice
Use == for value comparison

Use is for checking None

