# ObjectOriented

## Intro notes

* Can assign a variable that doesn't exist in the class definition

### Optional / Default values initialized
Optional and Default values to initialized variables:
```
class Employee:
    # defining the properties and assigning None to them
    def __init__(self, ID=None, salary=0, department=None):
        self.ID = ID
        self.salary = salary
        self.department = department
```

### Class variables vs Instance variables
Class varaibles are the same for all instances of the class. Instance variables are uniqiue to each object.
```
class Player:
    teamName = 'Liverpool'  # class variables

    def __init__(self, name):
        self.name = name  # creating instance variables
```

### Using Class Variables Smartly

```
class Player:
    teamName = 'Liverpool'      # class variables
    teamMembers = []

    def __init__(self, name):
        self.name = name        # creating instance variables
        self.formerTeams = []
        self.teamMembers.append(self.name)
```

### Method Overloading
In Python, you can't explicitly overload (define another function with the same nume but different arguments. You must use default values of optional arguments.
```
    def __init__(self, ID=None, salary=None, department=None):
        self.ID = ID
        self.salary = salary
        self.department = department

    # method overloading
    def demo(self, a, b, c, d=5, e=None):
        print("a =", a)
        print("b =", b)
        print("c =", c)
        print("d =", d)
        print("e =", e)
```

### Class Methods

Often used to alter class variables. Must use `@classmethod` decorator and `cls` argument.
```
class MyClass:
    classVariable = 'educative'

    @classmethod
    def demo(cls):
        return cls.classVariable
```

### Static Methods

Static methods do not know anything about the state of the class, i.e., they cannot modify class attributes. The purpose of a static method is to use its parameters and produce a useful result.

```
class Player:
    teamName = 'Liverpool'  # class variables

    def __init__(self, name):
        self.name = name  # creating instance variables

    @staticmethod
    def demo():
        print("I am a static method.")
```

Example use:
```
class BodyInfo:

    @staticmethod
    def bmi(weight, height):
        return weight / (height**2)


weight = 75
height = 1.8
print(BodyInfo.bmi(weight, height))
```
### Private Variables
If you must access a private variable:
```
class Employee:
    def __init__(self, ID, salary):
        self.ID = ID
        self.__salary = salary  # salary is a private property


Steve = Employee(3789, 2500)
print(Steve._Employee__salary)  # accessing a private property
```
