# Object Oriented notes and definitions

## This class takes 3 given arguements and makes the the attributes of the object
### This definition takes an input of a single letter to determine the which output to give
```python
class teacher:

  def __init__(self, gender, name, subject)
      self.gender = gender
        if self.gender == "m":
          self.gender == "Mr"
        else:
          self.gender == "Ms"
          
```
## These attributes hold a string input from the user or a given print statement to be used in later code
```python
      self.name = name
      self.subject = subject
```
## This defined function prints out a striong of the given attributes
```python
  def__str__(self):
    return f"the teachers name is {self.gender} {self.name} and their favourite subject is {self.subject}"
```
## This function will automatically print it as a string as a control so as to not produce an error
```python
  def__repr__(self):
    return self.__str__()
```
## This fucntion defines an action the object "teacher" has and an outcome along with the action
```python
  def __grade__(self, grade):
    pas
    self.grade = random(65, 101):
      return f"{self.gender} {self.name} has given your test a {self.grade}
      if self.grade >= 80:
        print("you have done very well")
      else:
        print("you have done a medicore job")

```
