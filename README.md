# Java Notes 

## Table of Contents
- [Procedural vs. Object-Oriented Programming](#procedural-vs-object-oriented-programming)
- [Classes and Objects](#classes-and-objects)
- [Data Types and Variables](#data-types-and-variables)
- [Constants and Best Practices](#constants-and-best-practices)
- [Methods](#methods)
- [Reflection: Encapsulation, Data Hiding, and Modular Methods in Teamwork](#reflection-encapsulation-data-hiding-and-modular-methods-in-teamwork)
- [Chapter 4: Using Classes and Objects](#chapter-4-using-classes-and-objects)

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

---

## Visual: Information Hiding Diagram

```
+------------------------------+
|          Employee            |
+------------------------------+
|  - empNum   (private)        |
|  - name     (private)        |
+------------------------------+
|  + getEmpNum()   (public)    |
|  + setEmpNum()   (public)    |
|  + getName()     (public)    |
|  + setName()     (public)    |
+------------------------------+
```

- `-` = private (hidden inside the class)  
- `+` = public (accessible outside the class)  

### How it works
- Outside code cannot directly touch `empNum` or `name`.  
- It must go through public methods (`getEmpNum`, `setEmpNum`, etc.).  
- Those methods can enforce rules (e.g., no negative employee numbers).  


### Analogy
Think of the class as a **bank vault**:  
- The money (`empNum`, `name`) is **locked inside** (`private`).  
- You interact with the vault only through **tellers (methods)**, who follow strict rules.  

---

## Chapter 4: Using Classes and Objects

**Important Concepts**

- **Classes and Objects**: A class is a blueprint; an object is an instance created from it.
  ```
  class Laptop { 
      String brand; 
      int storage; 
  }
  Laptop myLaptop = new Laptop();
  ```

- **Creating a Class**: Classes contain fields (attributes) and methods (behaviors).
  ```
  public class Car {
      String make;
      int year;
      void honk() {
          System.out.println("Beep!");
      }
  }
  ```

- **Instance Methods**: Require an object to be called; operate on instance fields.
  ```
  Car myCar = new Car();
  myCar.honk();  // calls instance method
  ```

- **Declaring Objects**: Use the `new` keyword and dot operator to create and access objects.
  ```
  Car car1 = new Car();
  car1.make = "Toyota";
  ```

- **Classes as Data Types**: User-defined classes act as new data types.
  ```
  Book myBook = new Book();
  ```

- **Constructors**: Special methods used to initialize objects. Can be default (no parameters) or parameterized. Can also be overloaded.
  ```
  public class Book {
      String title;
      Book(String t) {
          title = t;
      }
  }
  Book b1 = new Book("Anne of Green Gables");
  ```

- **this Reference**: Refers to the current object; used to differentiate fields from parameters and for constructor chaining.
  ```
  public class Student {
      String name;
      Student(String name) {
          this.name = name;
      }
  }
  ```

- **Static Fields and Methods**: Belong to the class, not individual objects. Shared across all instances (e.g., `Math.PI`).
  ```
  System.out.println(Math.PI);  // static field
  ```

- **Imported Constants and Methods**: Java API classes (e.g., `Math`, `Scanner`) provide reusable constants and methods.
  ```
  import java.util.Scanner;
  Scanner sc = new Scanner(System.in);
  ```

- **Composition**: A class containing objects of another class.
  ```
  class Engine { }
  class Car {
      Engine engine = new Engine();
  }
  ```

- **Nested Classes**: Classes defined inside another class to logically group functionality.
  ```
  class Outer {
      class Inner {
          void display() {
              System.out.println("Nested class");
          }
      }
  }
  ```
