# Data Structures in Pyton

## Lists in Python

```python
List1 = [1, 2, 3, 4]
print(*List1)  # Output: 1 2 3 4
print(*List1, sep=" ")  # Output: 1 2 3 4 (separated by space)

List1.insert(len(List1), 6)  # will insert 6 at the end of the list
List1.append(6)  # will insert 6 at the end of the list
List1.extend([6, 7, 8])  # will add the elements [6, 7, 8] to the list
List1.pop(4) # will remove the index number 4
del List[4] # will remove the index number 4

List2 = ['A', 'B', 'C', 'D']
List3 = [1, 'A', True, 'B']
List3 = [1, 'A', True, [1, 2, 3, 4]]  # Nested list

```

***

## Tuples

```python
Tuple= (1, 2, '3', True, 4.3)
print(Tuple.count()) # will return 5 the elements count
print(Tuple.count('3')) # will return 2 the index number of '3'
print(Tuple.index(2)) # wil return 1 the index number of 2

```

***

## Sets

```python

Set= {1, 2, 3, 4, 5, 5}
print(Set) # will print {1, 2, 3, 4, 5}
Set.add(6) # will add 6 to the set
Set.remove(2) # will remove 2 from the set
Set.discard(2) # will remove 2 from the set

set_a= {0, 1, 2, 3, 4, 4}
set_b= {5, 6, 7, 8, 9}

print(set_a.union(set_b)) # will print {0, 1, 2, 3, 4, 5, 6, 7, 8, 9}
print(set_a | set_b) # will print {0, 1, 2, 3, 4, 5, 6, 7, 8, 9}
print(set_a.intersection(set_b)) # will brint 4 the element common
print(set_a & set_b) # will brint 4 the element common
print(set_a.difference(set_b)) # will print {0, 1, 2, 3, 4}
print(set_a - set_b) # will print {0, 1, 2, 3, 4}
print(set_a.symmetric_difference(set_b))
print(set_a ^ set_b) w

```

## Dictionaries

```python
my_dict= {'name': 'Mohamed Soliman', 'phone_num': '+201228120928'}
print(my_dict['name']) # will print Mohamed Soliman
my_dict['age']= 21 
print(my_dict)

```

## *args & **kwargs

### *args is used to pass a variable number of non-keyword arguments to a function. It collects these arguments into a tuple.

```python
def print_items(*args):
    for index, item in enumerate(args): # enumerate is a built-in Python function that adds a counter to an iterable (like a list, tuple, or string)
        print(f"Item {index + 1}: {item}")

print_items(1, "apple", True, 3.5)
'''Output:
Item 1: 1
Item 2: apple
Item 3: True
Item 4: 3.5
'''

def print_info(**kwargs):
    for key, value in kwargs.items():
        print(f"{key}: {value}")

print_info(name="Mohamed", age=21, city="Alexandria")
'''Output:
name: Mohamed
age: 21
city: Alexandria
'''

def display_data(*args, **kwargs):
    print("Positional arguments (args):")
    for arg in args:
        print(arg)
    
    print("\nKeyword arguments (kwargs):")
    for key, value in kwargs.items():
        print(f"{key}: {value}")

display_data(1, 2, 3, name="Mohamed", age=21, country="Alexandria")

'''Output:
Positional arguments (args):
1
2
3

Keyword arguments (kwargs):
name: Mohamed
age: 21
country: Alexandria
'''

def display_person(**kwargs):
    print(f"Person info:")
    for key, value in kwargs.items():
        print(f"{key}: {value}")

person = {'name': 'Mohamed', 'age': 21, 'city': 'Alexandria'}
display_person(**person)
'''Output:
Person info:
name: Mohamed
age: 21
city: Alexandria
'''

```
