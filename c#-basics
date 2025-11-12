# 🧩 **C# Fundamentals & Syntax Mastery**

C# is a **strongly typed**, **object-oriented**, and **modern** programming language developed by Microsoft.
It’s the core of the **.NET ecosystem** and used for web apps, games, cloud, desktop, and more.

---

## 🧠 1. **Data Types, Variables, Operators, Conditionals, Loops**

---

### 🔹 **Variables**

Variables are containers for storing data.
You must **declare a type** before using a variable.

```csharp
int age = 25;
string name = "Alice";
bool isActive = true;
```

C# is **strongly typed**, meaning:

* Once a type is declared, it cannot change.
* The compiler checks type consistency at compile time.

You can also use **implicit typing** with `var`:

```csharp
var city = "London"; // Compiler infers string
```

---

### 🔸 **Common Data Types**

| Category       | Examples                       | Description                                 |
| -------------- | ------------------------------ | ------------------------------------------- |
| Integer        | `int`, `long`, `short`, `byte` | Whole numbers                               |
| Floating point | `float`, `double`, `decimal`   | Numbers with decimals (`decimal` for money) |
| Boolean        | `bool`                         | `true` or `false`                           |
| Character      | `char`                         | Single character `'A'`                      |
| String         | `string`                       | Text                                        |
| Object         | `object`                       | Base type of all data in C#                 |

---

### 🔹 **Operators**

Used to perform operations on variables and values.

| Type                  | Examples            | Description             |    |                         |
| --------------------- | ------------------- | ----------------------- | -- | ----------------------- |
| Arithmetic            | `+ - * / %`         | Math operations         |    |                         |
| Comparison            | `== != > < >= <=`   | Compare values          |    |                         |
| Logical               | `&&                 |                         | !` | Combine boolean results |
| Assignment            | `= += -= *= /=`     | Assign or modify values |    |                         |
| Increment / Decrement | `++ --`             | Add or subtract 1       |    |                         |
| Ternary               | `condition ? a : b` | Short if-else           |    |                         |

Example:

```csharp
int x = 10;
string result = (x > 5) ? "Big" : "Small";
```

---

### 🔸 **Conditionals**

Used to make decisions in code.

```csharp
if (age >= 18)
    Console.WriteLine("Adult");
else if (age > 13)
    Console.WriteLine("Teenager");
else
    Console.WriteLine("Child");
```

`switch` statement:

```csharp
switch (day)
{
    case "Mon": Console.WriteLine("Start of week"); break;
    case "Fri": Console.WriteLine("Weekend soon"); break;
    default: Console.WriteLine("Midweek"); break;
}
```

---

### 🔹 **Loops**

Used to repeat actions.

**For loop:**

```csharp
for (int i = 0; i < 5; i++)
    Console.WriteLine(i);
```

**While loop:**

```csharp
int i = 0;
while (i < 5)
{
    Console.WriteLine(i);
    i++;
}
```

**Foreach loop:**

```csharp
string[] fruits = { "Apple", "Banana", "Cherry" };
foreach (var f in fruits)
    Console.WriteLine(f);
```

---

## ⚙️ 2. **Functions, Parameters, Return Types**

Functions (or methods) are **blocks of reusable code**.

```csharp
int Add(int a, int b)
{
    return a + b;
}
```

**Calling the method:**

```csharp
int sum = Add(3, 5);
Console.WriteLine(sum);
```

### 🔸 Parameter Types

* **By Value (default)** → a copy of data is passed.
* **By Reference (`ref`, `out`)** → changes affect the original variable.

```csharp
void DoubleIt(ref int number)
{
    number *= 2;
}
```

### 🔹 Return Types

* Every method declares a **return type**.
* Use `void` if no value is returned.

---

## 🧱 3. **Classes, Objects, Constructors, Properties**

---

### 🔹 **Classes**

A class defines a **blueprint** for creating objects.

```csharp
public class Person
{
    public string Name;
    public int Age;

    public void Greet()
    {
        Console.WriteLine($"Hello, my name is {Name}.");
    }
}
```

### 🔸 **Objects**

An object is an **instance** of a class.

```csharp
Person p = new Person();
p.Name = "Alice";
p.Age = 30;
p.Greet();
```

---

### 🔹 **Constructors**

Special methods that run when a class is created.

```csharp
public class Car
{
    public string Brand { get; set; }

    // Constructor
    public Car(string brand)
    {
        Brand = brand;
    }
}
```

```csharp
var car = new Car("Toyota");
Console.WriteLine(car.Brand);
```

---

### 🔸 **Properties**

Safer way to expose class fields (encapsulation).

```csharp
public class Student
{
    public string Name { get; set; }
    public int Age { get; private set; } // Read-only from outside

    public Student(string name, int age)
    {
        Name = name;
        Age = age;
    }
}
```

---

## 🧬 4. **Static vs Instance, Encapsulation, Inheritance, Polymorphism**

---

### 🔹 **Static vs Instance**

* **Instance members** belong to an object.
* **Static members** belong to the class itself.

```csharp
public class MathHelper
{
    public static double Pi = 3.14;

    public static int Square(int n) => n * n;
}
```

Usage:

```csharp
Console.WriteLine(MathHelper.Pi);
Console.WriteLine(MathHelper.Square(5));
```

---

### 🔸 **Encapsulation**

Hiding internal details — exposing only what’s necessary.

Use **private fields** + **public properties**:

```csharp
public class BankAccount
{
    private decimal balance;

    public void Deposit(decimal amount)
    {
        if (amount > 0)
            balance += amount;
    }

    public decimal GetBalance() => balance;
}
```

---

### 🔹 **Inheritance**

A class can inherit from another class to reuse and extend behavior.

```csharp
public class Animal
{
    public void Eat() => Console.WriteLine("Eating...");
}

public class Dog : Animal
{
    public void Bark() => Console.WriteLine("Barking...");
}
```

Usage:

```csharp
var d = new Dog();
d.Eat(); // inherited
d.Bark(); // own
```

---

### 🔸 **Polymorphism**

Same method name, different behaviors.

```csharp
public class Animal
{
    public virtual void Speak() => Console.WriteLine("Animal sound");
}

public class Dog : Animal
{
    public override void Speak() => Console.WriteLine("Woof!");
}

Animal a = new Dog();
a.Speak(); // Output: Woof!
```

➡️ “Many forms” — allows flexibility when working with base class references.

---

## 📚 5. **Collections (List, Dictionary, HashSet)**

Collections store multiple objects in memory.

---

### 🔹 **List<T>**

Dynamic array that can grow or shrink.

```csharp
var numbers = new List<int> { 1, 2, 3 };
numbers.Add(4);
numbers.Remove(2);

foreach (var n in numbers)
    Console.WriteLine(n);
```

---

### 🔸 **Dictionary<TKey, TValue>**

Stores key-value pairs (like a map).

```csharp
var capitals = new Dictionary<string, string>
{
    ["France"] = "Paris",
    ["Japan"] = "Tokyo"
};

Console.WriteLine(capitals["France"]); // Paris
```

---

### 🔹 **HashSet<T>**

Stores unique values only (no duplicates).

```csharp
var names = new HashSet<string> { "Alice", "Bob", "Alice" };
Console.WriteLine(names.Count); // 2
```

---

## ⚠️ 6. **Exception Handling**

Used to catch and handle runtime errors safely.

```csharp
try
{
    int x = int.Parse("abc"); // Invalid
}
catch (FormatException ex)
{
    Console.WriteLine($"Error: {ex.Message}");
}
finally
{
    Console.WriteLine("Always runs");
}
```

* `try` → Code that may throw errors
* `catch` → Handle the error
* `finally` → Always executes (optional)

You can also **throw** custom exceptions:

```csharp
throw new InvalidOperationException("Invalid state");
```

---

## 📂 7. **Basic File I/O**

C# provides easy file reading/writing using the `System.IO` namespace.

```csharp
using System.IO;

// Write to a file
File.WriteAllText("note.txt", "Hello world!");

// Read from a file
string text = File.ReadAllText("note.txt");
Console.WriteLine(text);
```

**Asynchronous versions:**

```csharp
await File.WriteAllTextAsync("data.txt", "Async write");
string content = await File.ReadAllTextAsync("data.txt");
```

---
