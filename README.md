# ObjectOriented

## Into notes

* Can assign a variable that doesn't exist in the class definition

Optional and Default values to initialized variables:
```
class Employee:
    # defining the properties and assigning None to them
    def __init__(self, ID=None, salary=0, department=None):
        self.ID = ID
        self.salary = salary
        self.department = department
```

Class varaibles are the same for all instances of the class. Instance variables are uniqiue to each object.
```
class Player:
    teamName = 'Liverpool'  # class variables

    def __init__(self, name):
        self.name = name  # creating instance variables
```
