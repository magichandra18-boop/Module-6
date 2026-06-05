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
from abc import ABC, abstractmethod
import math
class Shape(ABC):
    @abstractmethod
    def calculate_area(self):
        pass
class Rectangle(Shape):
    def __init__(self, length=5, breadth=4):
        self.length = length
        self.breadth = breadth
    def calculate_area(self):
        return self.length * self.breadth
class Circle(Shape):
    def __init__(self, radius=3):
        self.radius = radius

    def calculate_area(self):
        return math.pi * self.radius * self.radius
rect = Rectangle()
circ = Circle()S
print("Area of Rectangle:", rect.calculate_area())
print("Area of Circle:", round(circ.calculate_area(), 2))

## Output
<img width="1012" height="457" alt="image" src="https://github.com/user-attachments/assets/de920be0-bae8-4ca7-88b0-d120051878e6" />


## Result
The area of the rectangle and circle was correctly calculated and displayed.
