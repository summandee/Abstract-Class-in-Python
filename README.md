# Abstract-Class-in-Python
# Abstract class definition

In Python, an abstract class is a class that is designed to be used as a base class and is not meant to be instantiated directly. It typically contains one or more abstract methods that must be implemented by its subclasses.

Benefits of Abstract Classes in Python:
Encapsulation:
Abstract classes help in encapsulating common behavior that can be shared among multiple subclasses. They define a common interface for all subclasses to follow.
Forcing Implementation:
Abstract classes can define abstract methods that must be implemented by the subclasses. This enforces a contract that ensures that all subclasses provide the required functionality.
Structure and Organization:
Abstract classes help in organizing code by defining a blueprint for how subclasses should be structured. They promote a clear structure and inheritance hierarchy.
Code Reusability:
Abstract classes promote code reusability by allowing common methods to be defined in the abstract class and used by all subclasses. This reduces code duplication.
Polymorphism:
Abstract classes enable polymorphic behavior, where objects of different classes can be treated as objects of the abstract class. This simplifies code and allows for more flexibility.
Future Extensibility:
Abstract classes make it easier to add new subclasses in the future that adhere to the common interface defined by the abstract class. This promotes extensibility and maintainability.

# Example of an Abstract Class in Python:
Here is an example demonstrating the use of the abc module to create an abstract class in Python:

from abc import ABC, abstractmethod

class Shape(ABC):
    @abstractmethod
    def area(self):
        pass

class Circle(Shape):
    def __init__(self, radius):
        self.radius = radius

    def area(self):
        return 3.14 * self.radius * self.radius

class Square(Shape):
    def __init__(self, side_length):
        self.side_length = side_length

    def area(self):
        return self.side_length * self.side_length

# Usage
# circle = Circle(5)
# print(circle.area())
# square = Square(4)
# print(square.area())
