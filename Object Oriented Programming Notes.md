# Slideshow 1 Notes:
---
  #### Objects:
  ---
  - There are [two](https://www.freecodecamp.org/news/object-oriented-programming-in-python/#:~:text=Python%2C%20like%20every%20other%20object,define%20a%20particular%20object%20type.) types of objects
  - **Objects in general computer science** refer to any type of data that exists in the computers memory which has a value and can be called or referenced by an identifier
  - **Objects in OOP (object oriented programming)** is an instance in a class where an object can be a variable, function, or data structure (or a combination of them)
  #### The OOP Paradigm:
  ---
  - [*Object Oriented Programming*](https://www.educative.io/blog/object-oriented-programming) creates reusable programmed software systems
  - Creates **objects** to use in said programmed software
  - Uses definitions to interpret code
  
  Procedure-oriented:              OOP:
  - Be logical                     - Name attribute
  - Complete tasks                 - Home address
  - Complete tasks that humans     - Attributes related to humans
    would be able to
  
  - Classes are a collection of all objects which can be accessed from it
  - Classes have attributes
  - Attributes are an objects tools
  - Fields are any variables belonging to an object or class
  - Methods are functions which objects are able to call upon
  
  #### OOP in Python 3:
  ---
  - Class is a python 3 built in keyword which allows the creation of classes
  
  [*Example:*](https://docs.google.com/presentation/d/1wJ1SqLBaVSahdJUO41QRkyyLDmXpMWCROxV5TzdWsvU/edit#slide=id.g2a79f171fd_0_28)
  ```python
  class Person:
    pass #Empty
  #end of Person Class
  
  student1 = Person() #student1 now belongs to Person Object
  ```
  
  - Methods for classes are declared like a function
  - Initialization method is used as soon as an object of a class is called upon
  - Self parameter declares that the method is applied and used for itself
  - Double underscore overwrites built in python features
          

# Slideshow 2 Notes:
---
  #### Encapsulation: 
  ---
  - **Encapsulation** is sued to restrict the access to certain classes and objects attributes/methods
  - This is useful for data protection and restricting what methods can be called upon
  - This is done in python by using double underscores as a prefix

[*Example*](https://docs.google.com/presentation/d/1BSBVPl27YKaFtiNa_6EPyUd5gnM5o60fKHdrmtp2jGk/edit#slide=id.g2a84dd718b_0_9)

```python
class Student:
  def __init__(self, nameF, nameL, num):
    self.firstName = nameF
    self.lastname = nameL
    self.__studentNumber = num
    
  def __getStudentNumber(self):
    return self.__studentNumber
    
#if someone were to try and call on the student number it would result in an error because it is now encapsulated
```
  #### Overloading and Overriding:
  ---
  - [**Overloading**](https://www.pluralsight.com/guides/overload-methods-invoking-overload-methods-csharp) is when two methods with the same name exist in one class but possess different parameters
  - [**Overriding**](https://www.techopedia.com/definition/24010/overriding) is when two methods with the same name exist **and** have the same parameters
  - **You can't overload in Python 3**
  
  #### Polymorphism:
  ---
  - **Polymorphism** is a method which can be utilized across multiple classes and objects assuming the correct parametrs are met
  
  #### Base Overrides:
  --- 
  - Two *different* classes utilize the **same** attribute and/or method 
  - A child would override that universal method and utilize it differently
  - Those are the two fundamental concepts related to overriding and polymorphism dual utility in Python
  - This concept can be used to override built-in methods in Python 3
  
  #### [__repr__() base function](https://www.digitalocean.com/community/tutorials/python-str-repr-functions):
  ---
  - This function allows us to **control** what is returned by the repr() string
  
# Slideshow 3 Notes:
---
  #### Inheritance:
  ---
  - When an object/class gets its features from a parent class
      1. *Single Inheritance:* A child class inherting the features of a single superclass or a parent class
      2. *Multiple Inheritance:* A child class inherting the features of mulitple parent classes
      3. *Multilevel Inheritance:* A child class inherting from another child 
  - A child class does not need a new __init__() method unless there is a new attribute 
  - A child class does not need to reinstate the parents methods unless the child class overrides them
  - super() is a method which allows for child classes to refer to their parent class
  - Multiple inheritances have different types
    1. *Multi-Generational:* Grandparent class --> Parent class --> Child class
    2. *Multi-Parent:* Parent A + Parent B --> Child class
    3. Mixture of 1 and 2

  [*Example:*](https://docs.google.com/presentation/d/1Y_By4kpgBXSZrrpH0JwcwBKgZf3GcTAweFDXrnMZx-U/edit#slide=id.g55ff66ea53_0_14)
  
  **Parent Class**                
  ```python
  class Person:
    def __init__(self, name):
      self.__name = name
      
    def getName(self):
      return self.__name
```
**Inherited Class**
```python
class Student(Person):
  def __init__(self, name, num):
    Person.__init__(self, name)
    self.__sNum = num
    
  def getStudentName(self):
    return("%s: %s" % (self.__sNum, self.getName()))
```  

  

# Slideshow 4 Notes:
---
  #### Iterable Objects:
  ---
  - Objects which can be iterated through similarly to a sequence 
  - **__iter__()** allows objects to be iterable
  - **__next__()** grabs the next value while iterating
  
 
