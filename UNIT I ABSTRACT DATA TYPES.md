# ✅ 1. Abstract Data Types (ADTs)
## 🔹 What is it?
- An Abstract Data Type is a logical description of how data is stored and what operations can be performed on it without worrying about how it's implemented in code.
---
## 🧠 Real-Life Example:
- Think of a Stack (like a pile of books):
- You can only add a book on top or remove the top book.
- You don’t care how the stack is implemented internally (array, linked list, etc.), just how you can use it.
---
## ✍️ Key Point:
- ADTs are not data structures themselves, but blueprints for data structures.
---
# ✅ 2. ADTs and Classes
## 🔹 Explanation:
- In programming, we use classes to implement ADTs.

## 🧠 Example:
- An ADT says: “This is a stack. It should allow `push`, `pop`, and `peek`.”

- A Python class can define exactly how those operations work using lists or other structures.
```Python
class Stack:
    def __init__(self):
        self.items = []

    def push(self, item):
        self.items.append(item)
    
    def pop(self):
        return self.items.pop()
```
---
# ✅ 3. Introduction to OOP (Object-Oriented Programming)
## 🔹 What is it?
- OOP is a way of writing code using objects and classes that mimic real-world things.
---
## 🔑 Four Main Concepts:
 
| Concept        | Meaning                                        |
|----------------|------------------------------------------------|
| Encapsulation  | Keep data + functions in one unit (class)      |
| Abstraction    | Hide complex code, show only important stuff   |
| Inheritance	 | Child class gets parent class features         |
| Polymorphism	 | Same function, different behavior              |
---
# ✅ 4. Classes in Python
## 🔹 What is a class?
-  A class is a template to create objects.
---
## 🧠 Example:
```python
class Student:
    def __init__(self, name):
        self.name = name
    
    def say_hello(self):
        print("Hello, I'm", self.name)

s = Student("Rishi")
s.say_hello()  # Output: Hello, I'm Rishi
```
---
# ✅ 5. Inheritance
## 🔹 What is it?
- Inheritance lets you create a new class using features of an existing class.
---
## 🧠 Example:
```python
class Animal:
    def speak(self):
        print("Some sound")

class Dog(Animal):
    def speak(self):
        print("Bark")

d = Dog()
d.speak()  # Output: Bark
```
- `Dog` reuses code from `Animal` but can also override behavior.
# ✅ 6. Namespaces
## 🔹 What is a namespace?
- A namespace is a space where names (like variable names) are stored.
---
## 🧠 Types in Python:
|Namespace	|Example|
|-----------|--------|
|Local	|Inside a function|
|Global|	Top of a file|
|Built-in	|Python keywords like `print()`, `len()`|
```python
x = 10  # global

def func():
    x = 5  # local
    print(x)

func()  # Output: 5
print(x)  # Output: 10
```
---
# ✅ 7. Shallow and Deep Copying
## 🔹 Shallow Copy:
- Only copies the reference (pointer), not the actual inner values.
```python
import copy

a = [[1, 2], [3, 4]]
b = copy.copy(a)
a[0][0] = 99
print(b)  # Output: [[99, 2], [3, 4]]
```
## 🔹 Deep Copy:
- Copies everything, including nested items.
```python
c = copy.deepcopy(a)
a[0][0] = 42
print(c)  # Output: [[99, 2], [3, 4]] → Still has old values
```
---
# ✅ 8. Introduction to Analysis of Algorithms
## 🔹 Why analyze algorithms?
- To check how fast and efficient your algorithm is in terms of:

- Time (how many steps it takes)

- Space (how much memory it uses)
---

## 🧠 Simple:
- You compare algorithms to choose the best one.
---
# ✅ 9. Asymptotic Notations
## 🔹 Used to describe algorithm speed:

|Notation|	Meaning	|Example|
|-------|---------|------|
|O(n)	|Worst-case time	|Linear search|
|Ω(n)	|Best-case time|	Best case in linear search|
|Θ(n)	|Average-case time	|Typical behavior|
---
## 🧠 Example:
```text
Linear Search → O(n)
Binary Search → O(log n)
Bubble Sort → O(n^2)
```
---
# ✅ 10. Divide and Conquer
## 🔹 What is it?
- An algorithm design method:

  - Divide the problem into smaller parts.

  - Solve each part (recursively).

  - Combine the results.
---

## 🧠 Example:
- Merge Sort:

  - Divide the array in half

  - Sort each half

  - Merge them together
---
# ✅ 11. Recursion
## 🔹 What is it?
- A function that calls itself to solve smaller versions of a problem.
---
## 🧠 Example:
```python
def countdown(n):
    if n == 0:
        print("Done!")
    else:
        print(n)
        countdown(n-1)

countdown(3)
```
# ✅ 12. Analyzing Recursive Algorithms
## 🔹 What do you analyze?
- How many times the function calls itself.

- How much work is done in each call.

## 🧠 Example:
For Binary Search, if the input size is n:
```text
T(n) = T(n/2) + 1 → O(log n)
```
For Merge Sort:
```text
T(n) = 2T(n/2) + n → O(n log n)
```
