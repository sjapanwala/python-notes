# <center> Final Exam Preperations
## <center> Disclaimer: **Dont Use This To Solely Study**,this is meant to be used for revision purposes!
### <center> Saaim Japanwala | CMPUT 175
### Topics to Prepare
- [x] Classes, Objects, Methods
- [x] Built in Data Structure (Lists, Tuple, Dictionary)
- [x] Time Complexity / Algorithm Analysis
- [x] Abstract Data Structures (Stacks, Queues)
- [x] Error Handeling and Exception
- [x] Recursion
- [x] Sorting
- [x] Searching
- [x] Trees

## Classes, Objects, Methods
### Classes
A class is a blueprint for creating objects. Classes encapsulate data for the object.

### Objects
An object is an instance of a class. It can have attributes (data) and methods (functions).

### Methods
Methods are functions defined inside a class that describe the behaviors of an object.

### Example
```python
class Animal:
    def __init__(self, name):
        self.name = name  # Attribute

    def speak(self):
        pass  # Placeholder for a method

class Dog(Animal):
    def speak(self):
        return f"{self.name} says Woof!"

# Creating an object of the Dog class
dog = Dog("Buddy")
print(dog.speak())  # Output: Buddy says Woof!
```
#### In this example, Animal is a class, Dog is a subclass of Animal, and dog is an instance (object) of the Dog class.

## Built In Data Types
- built in data types include lists, tuples, dictionaries
### List
- An ordered, mutable collection of items.
```py
fruits = ["apple", "banana", "cherry"]
# Accessing an element
print(fruits[1])  # Output: banana
# Modifying an element
fruits[1] = "blueberry"
```
### Tuple
- An ordered, immutable collection of items. Once created, the items cannot be changed.
```py
coordinates = (10, 20)
# Accessing an element
print(coordinates[0])  # Output: 10
```
### Dictionary
- An unordered collection of key-value pairs. Each key must be unique.
```py
student = {"name": "Alice", "age": 24}
# Accessing a value
print(student["name"])  # Output: Alice
# Adding a new key-value pair
student["grade"] = "A"
```
### Set
- An unordered collection of unique items. Duplicate elements are not allowed.
```py
unique_numbers = {1, 2, 3, 4, 5}
# Adding an element
unique_numbers.add(6)
# Removing an element
unique_numbers.remove(3)
```

## Time Complexity and Algorithm Analysis
### Big O Notation
- Big O notation describes the upper limit of the time complexity as the input size grows. It's used to classify algorithms based on their running times or space requirements in the worst-case scenario.

### Common Complexities

#### <center>Fastest
- O(1) time
    * Accessing Array Index (int a = ARR[5];)
    * Inserting a node in Linked List
    * Pushing and Poping on Stack
    * Insertion and Removal from Queue
    * Finding out the parent or left/right child of a node in a tree stored in Array
    * Jumping to Next/Previous element in Doubly Linked List
- O(n) time
    * In a nutshell, all Brute Force Algorithms, or Noob ones which require linearity, are based on O(n) time complexity
    * Traversing an array
    * Traversing a linked list
    * Linear Search
    * Deletion of a specific element in a Linked List (Not sorted)
    * Comparing two strings
    * Checking for Palindrome
    * Counting/Bucket Sort and here too you can find a million more such examples....
- O(log n) time
    * Binary Search
    * Finding largest/smallest number in a binary search tree
    * Certain Divide and Conquer Algorithms based on Linear functionality
    * Calculating Fibonacci Numbers - Best Method The basic premise here is NOT using the complete data, and reducing the problem size with every iteration
- O(n log n) time
    * The factor of 'log n' is introduced by bringing into consideration Divide and Conquer. Some of these algorithms are the best optimized ones and used frequently.
    * Merge Sort
    * Heap Sort
    * Certain Divide and Conquer Algorithms based on optimizing O(n^2) algorithms
- O(n^2) time
    * These ones are supposed to be the less efficient algorithms if their O(nlogn) counterparts are present. The general application may be Brute Force here.
    * Bubble Sort
    * Insertion Sort
    * Selection Sort
    * Traversing a simple 2D array
#### <center>Slowest

## Abstract Data Types (ADT)
- **a way to structure data and data types which stores and emits data effeciently or according to the speed/storage a program or algorithm needs.**
- provides a framework for data
- speed up and make operations more effecient

### Bags and Sets
- a bag or a set is one of the simplest data stuctures
- **are not ordered or sorted by any means**
- items can be added, removed, or accessed
- **duplicates are only allowed in bags (lists and tuples)**
- sets have different operations 
    * union - everything in the set of a and b
    * intersection - only the shared items in the set of a an b
    * difference - the differences in the set of a and b
    * subset - a set inside of the set of a and b
### Stack
- A stack is a data structure that follows the Last In, First Out (LIFO) principle. The last item added is the first one to be removed.
    * Operations
       * push: Add an item to the top.
       * pop: Remove the top item.
       * peek: View the top item without removing it.
       * is_empty: Check if the stack is empty.
### Queue
- A queue is a data structure that follows the First In, First Out (FIFO) principle. The first item added is the first one to be removed.
    * Operations
        * enqueue: Add an item to the end.
        * dequeue: Remove the front item.
        * front: View the front item without removing it.
        * is_empty: Check if the queue is empty.

## Error Handeling and Exceptions
### Try-Except Block
-  Use try-except blocks to handle exceptions and prevent the program from crashing.
```py
try:
    result = 10 / 0
except ZeroDivisionError:
    print("Cannot divide by zero")
```
### Finally Block
- The finally block executes code regardless of whether an exception occurred or not. It's useful for cleanup actions.
```py
try:
    file = open('test.txt', 'r')
except FileNotFoundError:
    print("File not found")
finally:
    file.close()
```
## Recursion
### Definition
- Recursion is a method of solving problems where a function calls itself as a subroutine. This allows the function to be repeated several times as it can call itself during its execution.

### Base Case
- A base case is a condition that stops the recursion. Without it, the function would call itself indefinitely.

#### Example: Factorial
The factorial of a number is the product of all positive integers up to that number.
```py
def factorial(n):
    if n == 1:  # Base case
        return 1
    else:
        return n * factorial(n-1)  # Recursive call

print(factorial(5))  # Output: 120
```

## Sorting Algorithms
- is a set of instructions to sort data
### Bubble Sort
- Bubble sort repeatedly steps through the list, compares adjacent elements, and swaps them if they are in the wrong order. The process repeats until the list is sorted.
### Merge Sort
- Merge sort is a divide and conquer algorithm. It divides the input array into two halves, calls itself for the two halves, and then merges the two sorted halves.

## Searching Algorithms
### Binary Search
- Binary search works on sorted arrays. It divides the array into halves to find the target value.

- Steps:
    * Compare the target with the middle element.
    * If the target matches the middle element, return the index.
    * If the target is smaller, repeat the search on the left half.
    * If the target is larger, repeat the search on the right half.

## Trees and Binary Trees