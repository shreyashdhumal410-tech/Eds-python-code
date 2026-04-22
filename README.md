

---

## 1. List - Basic Operations

**Code:**
```python
a = [10, 20, 15]
print(a[0])  # access first item
a.append(11)  # add item
a.remove(20)  # remove item
print(a)
```

**Output:**
```
10
[10, 15, 11]
```

---

## 2. Creating a List - Using Square Brackets

**Code:**
```python
# List of integers
a = [1, 2, 3, 4, 5]
# List of strings
b = ['apple', 'banana', 'cherry']
# Mixed data types
c = [1, 'hello', 3.14, True]
print(a)
print(b)
print(c)
```

**Output:**
```
[1, 2, 3, 4, 5]
['apple', 'banana', 'cherry']
[1, 'hello', 3.14, True]
```

---

## 3. Creating a List - Using list() Constructor

**Code:**
```python
# From a tuple
a = list((1, 2, 3, 'apple', 4.5))
print(a)
```

**Output:**
```
[1, 2, 3, 'apple', 4.5]
```

---

## 4. Creating a List - With Repeated Elements

**Code:**
```python
# Create a list [2, 2, 2, 2, 2]
a = [2] * 5
# Create a list [0, 0, 0, 0, 0, 0, 0]
b = [0] * 7
print(a)
print(b)
```

**Output:**
```
[2, 2, 2, 2, 2]
[0, 0, 0, 0, 0, 0, 0]
```

---

## 5. Accessing List Elements

**Code:**
```python
a = [10, 20, 30, 40, 50]
# Access first element
print(a[0])
# Access last element
print(a[-1])
```

**Output:**
```
10
50
```

---

## 6. Adding Elements into List

**Code:**
```python
# Initialize an empty list
a = []
# Adding 10 to end of list
a.append(10)
print("After append(10):", a)
# Inserting 5 at index 0
a.insert(0, 5)
print("After insert(0, 5):", a)
# Adding multiple elements [15, 20, 25] at the end
a.extend([15, 20, 25])
print("After extend([15, 20, 25]):", a)
```

**Output:**
```
After append(10): [10]
After insert(0, 5): [5, 10]
After extend([15, 20, 25]): [5, 10, 15, 20, 25]
```

---

## 7. Updating Elements in List

**Code:**
```python
a = [10, 20, 30, 40, 50]
# Change the second element
a[1] = 25
print(a)
```

**Output:**
```
[10, 25, 30, 40, 50]
```

---

## 8. Removing Elements from List

**Code:**
```python
a = [10, 20, 30, 40, 50]
# Removes the first occurrence of 30
a.remove(30)
print("After remove(30):", a)
# Removes the element at index 1 (20)
popped_val = a.pop(1)
print("Popped element:", popped_val)
print("After pop(1):", a)
# Deletes the first element (10)
del a[0]
print("After del a[0]:", a)
```

**Output:**
```
After remove(30): [10, 20, 40, 50]
Popped element: 20
After pop(1): [10, 40, 50]
After del a[0]: [40, 50]
```

---

## 9. Tuple - Basic Example

**Code:**
```python
# Note: In case of list, we use square
# brackets []. Here we use round brackets ()
t = (10, 20, 30)
print(t)
print(type(t))
```

**Output:**
```
(10, 20, 30)
<class 'tuple'>
```

---

## 10. Tuple - Immutability Demo

**Code:**
```python
t = (1, 2, 3, 4, 5)
# tuples are indexed
print(t[1])
print(t[4])
# tuples contain duplicate elements
t = (1, 2, 3, 4, 2, 3)
print(t)
# updating an element (this will cause an error)
t[1] = 100
print(t)
```

**Output:**
```
2
5
(1, 2, 3, 4, 2, 3)
Traceback (most recent call last):
  File "Solution.py", line 12, in <module>
    t[1] = 100
TypeError: 'tuple' object does not support item assignment
```

---

## 11. List of Tuples - Manual Creation

**Code:**
```python
# Creating a list of tuples manually
a = [(1, 'apple'), (2, 'banana'), (3, 'cherry')]
print(a)
```

**Output:**
```
[(1, 'apple'), (2, 'banana'), (3, 'cherry')]
```

---

## 12. List of Tuples - Using a Loop

**Code:**
```python
a = [1, 2, 3]
b = ['apple', 'orange', 'cherry']
# Initialize an empty list
res = []
# Using a loop to create tuples and add them to the list
for i in range(len(a)):
    res.append((a[i], b[i]))
print(res)
```

**Output:**
```
[(1, 'apple'), (2, 'orange'), (3, 'cherry')]
```

---

## 13. List of Tuples - Using List Comprehension (Example 1)

**Code:**
```python
# Creating a list of tuples using list comprehension
a = [(x, x ** 2) for x in range(5)]
print(a)
```

**Output:**
```
[(0, 0), (1, 1), (2, 4), (3, 9), (4, 16)]
```

---

## 14. List of Tuples - Using List Comprehension (Example 2)

**Code:**
```python
a = [[1, 'apple'], [2, 'orange'], [3, 'cherry']]
# List comprehension to create a list of tuples
a = [tuple(x) for x in a]
print(a)
```

**Output:**
```
[(1, 'apple'), (2, 'orange'), (3, 'cherry')]
```

---

## 15. List of Tuples - Using zip()

**Code:**
```python
# Two lists with ids and name
a = [1, 2, 3]
b = ['apple', 'orange', 'cherry']
# Zip the lists and convert back into a list
a = list(zip(a, b))
print(a)
```

**Output:**
```
[(1, 'apple'), (2, 'orange'), (3, 'cherry')]
```

---

## 16. List of Tuples - Using map()

**Code:**
```python
a = [[1, 'apple'], [2, 'orange'], [3, 'cherry']]
# Using map to convert each list to a tuple
b = list(map(tuple, a))
print(b)
```

**Output:**
```
[(1, 'apple'), (2, 'orange'), (3, 'cherry')]
```

---

## 17. Dictionary - Basic Example

**Code:**
```python
d = {1: 'Geeks', 2: 'For', 3: 'Geeks'}
print(d)
```

**Output:**
```
{1: 'Geeks', 2: 'For', 3: 'Geeks'}
```

---

## 18. Dictionary - Creating a Dictionary

**Code:**
```python
# create dictionary using { }
d1 = {1: 'Geeks', 2: 'For', 3: 'Geeks'}
print(d1)
# create dictionary using dict() constructor
d2 = dict(a="Geeks", b="for", c="Geeks")
print(d2)
```

**Output:**
```
{1: 'Geeks', 2: 'For', 3: 'Geeks'}
{'a': 'Geeks', 'b': 'for', 'c': 'Geeks'}
```

---

## 19. Dictionary - Accessing Items

**Code:**
```python
d = {"name": "Alice", 1: "Python", (1, 2): [1, 2, 4]}
# Access using key
print(d["name"])
# Access using get()
print(d.get("name"))
```

**Output:**
```
Alice
Alice
```

---

## 20. Dictionary - Adding and Updating Items

**Code:**
```python
d = {1: 'Geeks', 2: 'For', 3: 'Geeks'}
# Adding a new key-value pair
d["age"] = 22
# Updating an existing value
d[1] = "Python dict"
print(d)
```

**Output:**
```
{1: 'Python dict', 2: 'For', 3: 'Geeks', 'age': 22}
```

---

## 21. Dictionary - Removing Items

**Code:**
```python
d = {1: 'Geeks', 2: 'For', 3: 'Geeks', 'age': 22}
# Using del to remove an item
del d["age"]
print(d)
# Using pop() to remove an item and return the value
val = d.pop(1)
print(val)
# Using popitem to remove and return the last key-value pair
key, val = d.popitem()
print(f"Key: {key}, Value: {val}")
# Clear all items from the dictionary
d.clear()
print(d)
```

**Output:**
```
{1: 'Geeks', 2: 'For', 3: 'Geeks'}
Geeks
Key: 3, Value: Geeks
{}
```

---

## 22. Dictionary - Loading JSON to Dictionary

**Code:**
```python
# importing the module
import json

# Opening JSON file
with open('data.json') as json_file:
    data = json.load(json_file)

    # Print the type of data variable
    print("Type:", type(data))

    # Print the data of dictionary
    print("\nPeople1:", data['people1'])
    print("\nPeople2:", data['people2'])
```

**Output:**
```
Type: <class 'dict'>

People1: [{'name': 'Nikhil', 'website': 'gfg.com', 'from': 'Delhi'},
          {'name': 'Abhinav', 'website': 'google.com', 'from': 'Mumbai'}]

People2: [{'name': 'Anshul', 'website': 'apple.com', 'from': 'Chennai'}]
```

---

## 23. Set - Creating Sets

**Code:**
```python
# create an empty set
empty_set = set()

# create a set of integer type
student_id = {112, 114, 116, 118, 115}
print('Student ID:', student_id)

# create a set of string type
vowel_letters = {'a', 'e', 'i', 'o', 'u'}
print('Vowel Letters:', vowel_letters)

# create a set of mixed data types
mixed_set = {'Hello', 101, -2, 'Bye'}
print('Set of mixed data types:', mixed_set)
```

**Output:**
```
Student ID: {112, 114, 115, 116, 118}
Vowel Letters: {'a', 'e', 'i', 'o', 'u'}
Set of mixed data types: {'Hello', 'Bye', 101, -2}
```

---

## 24. Set - Add and Remove Elements

**Code:**
```python
# Add Items to a Set
numbers = {21, 34, 54, 12}
print('Initial Set:', numbers)

# using add() method
numbers.add(32)
print('Updated Set:', numbers)

# Remove an Element from a Set
languages = {'Swift', 'Java', 'Python'}
print('Initial Set:', languages)

# remove 'Java' from a set
languages.discard('Java')
print('Set after remove():', languages)
```

**Output:**
```
Initial Set: {34, 12, 21, 54}
Updated Set: {32, 34, 12, 21, 54}
Initial Set: {'Python', 'Java', 'Swift'}
Set after remove(): {'Python', 'Swift'}
```

---

## 25. Set - Common Set Operations

**Code:**
```python
# first set
A = {1, 3, 5}
# second set
B = {1, 3, 4}

# perform union operation using |
print('Union using |:', A | B)

# perform union operation using union()
print('Union using union():', A.union(B))

print('Intersection using intersection():', A.intersection(B))
print('Difference using difference():', A.difference(B))
print('Symmetric Difference using symmetric_difference():', A.symmetric_difference(B))
```

**Output:**
```
Union using |: {1, 3, 4, 5}
Union using union(): {1, 3, 4, 5}
Intersection using intersection(): {1, 3}
Difference using difference(): {5}
Symmetric Difference using symmetric_difference(): {4, 5}
```
