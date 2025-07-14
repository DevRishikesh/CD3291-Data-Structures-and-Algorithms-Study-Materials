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
ADTs are not data structures themselves, but blueprints for data structures.
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
##🔑 Four Main Concepts:
-------------------------------------------------------------------
| Concept        | Meaning                                        |
| Encapsulation  | Keep data + functions in one unit (class)      |
| Abstraction    |	Hide complex code, show only important stuff  |
| Inheritance	   | Child class gets parent class features         |
| Polymorphism	 | Same function, different behavior              |
