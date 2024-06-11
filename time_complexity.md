# Algorithm Analysis
### Time and Space Complexity
- Saaim Japanwala
- CMPT 175

# What is Big O?
- run time.
- the amount of time it takes for our algorithm to execute as the input size of our algorithm grows.
- (usually) when the input grows, execution time will also grow. (could be linear, logarithmic, etc...).
- only care about the n value, not any other operation.
- Time Complexity (how much time it takes to execute)
- Space Complexity (how much space it takes to execute)

#  O(1) - constant growth complexity
- 1 is the only constant that is relevant
- no matter what the input value is, the number will always be the same, these are the most effecient algorithms
<p align="center">
<img src="img\xr21dwit.bmp" width="350" length="350"/>
</p>

```py
#Regardless of the size of the array, accessing a specific element takes the same amount of time because arrays provide direct access to elements based on their indices.

array = [1, 2, 3, 4, 5]
firstElement = array[0]
lastElement = array[-1]

print(f"First Element {firstElement}, Last Element {lastElement}")
```

# O(*n*) - linear growth complexity
- Linear complexity refers to the rate at which the time or space requirements of an algorithm increase linearly with the size of the input data 
- as input size grows (n), time will grow proportinally
- "2 inputs, will grow 2 times as fast" 
- For example, an algorithm with linear time complexity might have a running time proportional to the number of elements in an array or the length of a list. Similarly, an algorithm with linear space complexity might use additional memory proportional to the size of the input. ( affecting both time and space complexity)
<p align="center">
<img src="img\a8xfi9re.bmp" width="350" length="350"/>
</p>

```py
# an example of linear complexity would be, looping over an array
# lets say if it takes 1ms to loop over one item in an array, then if you have 5 items, it would take 5ms to loop over that array, therefor growing in time linear/proportionate to the input size

array = [1,2,3,4,5]
for n in array:
    print(n)
```
<p align="center" >
This is a visual example of the code block above. ↓
</p>

<p align="center">
<img src ="img\linearexample.png" width="350" length="350"/>
</p>

# O(*n*²) - quadratic growth complexity
- the time taken by an alogrithm that grows quadratically (n * n)
- the time it takes for an algorithm is squared. so if it takes an algorith 3ms, it will take 9ms for it to execute.
<p align="center">
<img src="img\o2.png" width="350" length="350">
</p>

```py
# a great example for a quadratic time complexity is iterating over an array (n * n) times.
# so if you were to loop over an array with a size of 5, but you wanted to loop over it again, it would be (5 * 5) therefor resulting in a quadratic time complexity of 25.

array = [1, 2, 3, 4, 5]
counter = 0 # to show iteration time
for i in array:
    for j in array:
        counter += 1
        print(i,j)
print(f"Iterated, {counter} Time(s)")

#>>> the output would be 25 which is 5^2
```
# O(*n* * *m*)
-  refers to the time complexity of an algorithm or operation where the performance depends on two variables: 'n' and 'm'.
- n refers to the size of the first input
- m refers to the size of the second input



<p align="center">
there is not graph for this one 😟
</p>

# O(*n*³) - cubic growth complexity  
- is the time complexity where the input is cubed O(n * n * n)
- when the input grows proportionally to cubed of the input
- if an array has 5 elements with 1ms each, we can iterate them 3 times with nested for loops, esentially giving us the output of (5 * 5 * 5) = 125ms to execute the algorithm
<p align="center">
<img src="img\pwpkxj4e.bmp" width="350" lenght="350"/>
</p>

```py
# a cubic time complexity is very similiar to a quadratic time complexity.
# we can use the same form of iteration test method

array = [1, 2, 3, 4, 5]
counter = 0

for i in array: # 5 iterations
    for j in array: # 25 iterations
        for k in array: # 125 iterations
            counter += 1
            print(i,j)
print(f"Iterated, {counter} Time(s)")

#>>> the output would be 125 which is 5^3
```
# O(*log*n) / O(N *log*n) - logarithmic growth complexity
- growth rate logarithmically
- mainly used in "divide and conquer" based algo's
- quicksort, binarytrees, etc..
-  has a runtime that increases very slowly as the input size grows. This makes it highly efficient, especially for large datasets.
<p align="center">
<img src="img\2w3ppwcf.bmp" width="350" length="350" />
</p>

```py
def binary_search(arr, target):
    left = 0
    right = len(arr) - 1
    
    while left <= right:
        mid = (left + right) // 2
        if arr[mid] == target:
            return mid
        elif arr[mid] < target:
            left = mid + 1
        else:
            right = mid - 1
    
    return -1  # If the target is not found
```

# O(2ⁿ) - exponential growth complexity
- growth rate exponentially proportionate to the input.
- for example, for 10 inputs it would take 1024 ms
- since it time complexity grows really fast, its not feasable to use for larger numbers
<p align="center">
<img src="img\gkiacxtf.bmp" width="350" height="350"/>
</p>

```py
# the fibonacci sequence is an excellent example of how exponential time complexity works]

def fibonacci(n):
    if n <= 1:
        return n
    else:
        return fibonacci(n-1) + fibonacci(n-2)

# when the variable n is replaced with input, it finds the nth term in the fibonacci sequence. this takes exponential time complexity. if we look for the 100th term,it will take 2^100 ms to find that term or 1.27E30
```

# Conclusion
<p align="center">
<img src="img\fwh1wts7.bmp" width="600" height="350"/l>
</p>

In summary, time complexity is a fundamental aspect of algorithm design and analysis that provides a theoretical framework for evaluating and comparing the efficiency of algorithms. It guides the development of efficient, scalable solutions and helps ensure that computational resources are used effectively. Understanding and applying time complexity principles is essential for both theoretical and practical aspects of computer science.
