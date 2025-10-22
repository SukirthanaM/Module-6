@@ -0,0 +1,35 @@
# 🐍 Python OOP: Abstract Class & Method Example

## 🎯 AIM

To create an **abstract class** named `Shape` with an **abstract method** `calculate_area`, and implement this method in two subclasses: `Rectangle` and `Circle`.

---

## 🧠 ALGORITHM

1. **Import ABC module**:
   - Use `from abc import ABC, abstractmethod` to define abstract classes and methods.

2. **Create Abstract Class `Shape`**:
   - Define an abstract method `calculate_area()` with `@abstractmethod`.

3. **Create Subclass `Rectangle`**:
   - Set default values for `length` and `breadth`.
   - Override `calculate_area()` to compute the rectangle area.

4. **Create Subclass `Circle`**:
   - Set default value for `radius`.
   - Override `calculate_area()` to compute the circle area.

5. **Create Objects & Call Methods**:
   - Instantiate `Rectangle` and `Circle`.
   - Call their `calculate_area()` methods.

---

## 💻 Program
```
from abc import ABC, abstractmethod
class Shape(ABC):

    @abstractmethod
    def calculate_area(self):
        pass
class Rectangle(Shape):
    def __init__(self, length=5, breadth=3):
        self.length = length
        self.breadth = breadth

    def calculate_area(self):
        area = self.length * self.breadth
        print(f"Area of Rectangle: {area}")
class Circle(Shape):
    def __init__(self, radius=4):
        self.radius = radius

    def calculate_area(self):
        area = 3.14 * self.radius * self.radius
        print(f"Area of Circle: {area}")
rect = Rectangle()
circ = Circle()
rect.calculate_area()
circ.calculate_area()

```
## Output
<img width="297" height="126" alt="image" src="https://github.com/user-attachments/assets/0ff9eb40-b915-4390-ac57-9d14b8be8959" />


## Result
Thus the python program has been executed successfully.

@@ -0,0 +1,29 @@
# 🐍 Python OOP: Encapsulation with Private Members

## 🎯 AIM

To implement **Encapsulation** in Python by defining a class `Rectangle` with **private member variables** `__length` and `__breadth`.

---

## 🧠 ALGORITHM

1. **Define the Class**:
   - Create a class `Rectangle` with two private attributes: `__length` and `__breadth`.

2. **Initialize Variables**:
   - Use the `__init__()` constructor to set initial values for `__length` and `__breadth`.

3. **Print Values**:
   - Display the private variables from within the class to demonstrate access.

4. **Instantiate the Object**:
   - Create an object of the `Rectangle` class to trigger the constructor.

---

## 💻 Program
```
class Rectangle:
    length = 0 
    breadth = 0
    def __init__(self):
        self.length = 5
        self.breadth = 3
        print(self.length)
        print(self.breadth)

obj = Rectangle()

```
## Output
<img width="247" height="148" alt="image" src="https://github.com/user-attachments/assets/365214e0-1df2-4196-8c91-303ffc71de40" />


## Result
Thus the python program has been executed successfully.

@@ -1,4 +1,4 @@
# 🐟 Fish and Shark Class Inheritance in Python
# 🐟 Method Overriding-Fish and Shark Class Inheritance in Python

## 🧠 AIM:
To write a Python program that demonstrates class inheritance by creating a parent class `Fish` with a method `type`, and a child class `Shark` that overrides the `type` method.

## 📋 ALGORITHM:

1. Define the `Fish` class with a method named `type()` that prints `"fish"`.
2. Define the `Shark` class as a subclass of `Fish`, and override the `type()` method to print `"shark"`.
3. Create an instance of the `Fish` class named `obj_goldfish`.
4. Create an instance of the `Shark` class named `obj_hammerhead`.
5. Use a `for` loop to iterate over both objects.
6. Within the loop, call the `type()` method using the loop variable.
7. Output will demonstrate method overriding: printing `"fish"` and `"shark"` accordingly.

## 💻 PROGRAM:
```python
class Fish:
    def type(self):
        print("fish")

class Shark(Fish):
	def type(self):
	    print("shark")

obj_goldfish=Fish()
obj_hammerhead=Shark()

obj_goldfish.type()
obj_hammerhead.type()
```

## OUTPUT
<img width="364" height="123" alt="image" src="https://github.com/user-attachments/assets/c68299e4-433f-4ba3-a67b-8005f42a43d9" />

## Result
Thus the python program has been executed successfully.

@@ -0,0 +1,31 @@
# 🐍 Python OOP: Operator Overloading (Less Than `<`)

## 🎯 AIM

To write a Python program that demonstrates **operator overloading** by overloading the **less than (`<`)** operator using a custom class.

---

## 🧠 ALGORITHM

1. **Create Class `A`**:
   - Define the `__init__()` method to initialize the object with a value `a`.

2. **Overload the `<` Operator**:
   - Define the `__lt__()` method with logic:
     - If `self.a < o.a`, return `"ob1 is less than ob2"`
     - Else, return `"ob2 is less than ob1"`

3. **Create Objects**:
   - Instantiate two objects `ob1` and `ob2` with values.

4. **Use `<` Operator**:
   - Use `print(ob1 < ob2)` to trigger the overloaded behavior.

---

## 💻 Program
```
class A:
    def __init__(self,a):
        self.a=a
    def __lt__(self,other):
        return self.a<other.a
ob1 = A(2)

ob2 = A(3)
if ob2<ob1:
    print("ob2 is less than ob1")
else:
    print("ob1 is less than ob2")
```
## Output
<img width="337" height="95" alt="image" src="https://github.com/user-attachments/assets/de12641c-f588-41e0-a4e0-d821dd717311" />

## Result
Thus the python program has been executed successfully

@@ -0,0 +1,32 @@
# # 🐍 Python OOP: Polymorphism with Classes

## 🎯 AIM

To create two specific classes — `Beans` and `Mango`. Then, create a **generic function** that can accept any object and determine its **type** (Fruit or Vegetable) and **color**, using polymorphism.

---

## 🧠 ALGORITHM

1. **Create Class `Beans`**:
   - Define `type()` method that prints `"Vegetable"`.
   - Define `color()` method that prints `"Green"`.

2. **Create Class `Mango`**:
   - Define `type()` method that prints `"Fruit"`.
   - Define `color()` method that prints `"Yellow"`.

3. **Define Generic Function `func(obj)`**:
   - Call `obj.type()` and `obj.color()` — this works with both `Beans` and `Mango` objects, showcasing **polymorphism**.

4. **Create Objects**:
   - Instantiate `Beans` and `Mango`.
   - Pass them to `func()` and execute the program.

---

## 💻 Program
```
class Beans:
    def type(self):
        print("Type: Vegetable")

    def color(self):
        print("Color: Green")

class Mango:
    def type(self):
        print("Type: Fruit")

    def color(self):
        print("Color: Yellow")

def func(obj):
    obj.type()
    obj.color()
b = Beans()
m = Mango()
func(b)
func(m)

```
## Output
<img width="320" height="175" alt="image" src="https://github.com/user-attachments/assets/4865b795-bcdc-4d43-9a74-4a2d2fd7a5a0" />

## Result
Thus the python program has been executed successfully
