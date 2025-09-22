# Java Notes 

## Table of Contents
- [Procedural vs. Object-Oriented Programming](#procedural-vs-object-oriented-programming)
- [Classes and Objects](#classes-and-objects)
- [Data Types and Variables](#data-types-and-variables)
- [Constants and Best Practices](#constants-and-best-practices)
- [Methods](#methods)
- [Reflection: Encapsulation, Data Hiding, and Modular Methods in Teamwork](#reflection-encapsulation-data-hiding-and-modular-methods-in-teamwork)

---

## Procedural vs. Object-Oriented Programming
Procedural programming solves problems with **step-by-step instructions**, keeping functions and data separate.  
Object-oriented programming organizes code into **classes** that bundle data (fields) and behavior (methods).  

**Encapsulation** hides internal details and exposes only what is necessary through controlled methods. This makes programs:  
- More secure  
- Easier to maintain  
- Less prone to unintended changes  
- Easier to use  

---

## Classes and Objects
A **class** is a blueprint that defines attributes (fields) and behaviors (methods).  
An **object** is an instance of a class with actual values.  

**Example:**  
- Class → `Laptop` with attributes: brand, model, storage  
- Object → Apple MacBook Pro, black, 15 GB  

The class defines the template, while the object represents a specific real-world example.  

---

## Data Types and Variables
Java enforces **explicit variable types** to ensure type safety, catch errors early, and make programs easier to read.  

**Strong typing** prevents invalid operations (like adding a number to text). Without it, programs would be harder to debug, less predictable, and more error-prone.  

Because Java knows the exact type at **compile time**, the compiler can:  
- Allocate the right amount of memory  
- Prevent illegal operations (e.g., adding a `String` to an `int`)  
- Generate faster machine code  

**Benefits:**  
- **Self-documenting** → the type tells humans what kind of data it holds  
- **Optimization** → compiler makes the program safer and faster  

---

## Constants and Best Practices
**Named constants** make programs easier to read, maintain, and update.  

**Example in Java:**  
```java
final double CLOTHES_DISCOUNT = 0.20;
```

**Advantages:**
- Defined once, used everywhere
- Changing it updates all references
- Prevents accidental changes
- Makes the program self-explanatory

## Methods

**A method declaration includes:**
- Access specifier → public, private
- Return type → int, double, void, etc.
- Method name → describes its purpose
- Parameters → inputs the method needs
- Body → statements that define the behavior

**Why modularization is best practice:**
- Breaks programs into smaller, reusable, and testable pieces
- Improves clarity and debugging
- Supports teamwork (each method does one job well)
- Keeps code simple, readable, and maintainable

---

## Reflection: Encapsulation, Data Hiding, and Modular Methods in Teamwork
Encapsulation, data hiding, and modular methods all create a structure that makes collaboration smoother and code safer in software projects.

- **Encapsulation** bundles fields and methods together inside classes, so a developer working on one class doesn’t need to worry about the internal details of another. This prevents accidental interference and allows teammates to focus on their own modules.
- **Data hiding** (through private fields and controlled access methods) prevents unauthorized or unintended changes. If every teammate can directly edit shared variables, bugs and inconsistencies spread quickly. With hidden data, the program only changes in predictable ways, reducing errors and making debugging easier.
- **Modular methods** break large tasks into smaller, reusable pieces. In a team, this means developers can divide responsibilities—one person writes input methods, another handles calculations, another manages display. Each piece can be tested independently, which speeds up debugging and integration.
