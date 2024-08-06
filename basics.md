# ***Introduction to Python - CMPUT 174***

## what is tokenization?
#### toeknization is assembling a series of instructions that makes a sentence, but instead of english, its python.
### example
#### -> My brown fox jumped
- my = pronoun
- brown = adjective
- fox = noun
- jumped = verb

#### these words in thise sequence  create a word that makes sense. lik english, python also needs a set of words that need to make sense, you cant just arrange a random row of instructions that dont make sense and expect python to know what it means.
```py 
message = "this is a simple statement"
print(message)
```
## Variables

#### -> variables need to be written in a certain manner.
1) cannot startk with a number
2) can start with an underscore, or a lowercase letter
3) cannot start with a capital letter
4) should follow CamelCase or underscores

```py
camelCase = "camelCase rule"
under_score = "under_score rule"
```

#### -> variables should also be meaningful, so they dont get confusing and are easy to read.
```py 
number = 50
newNumber = number + 1
newNumber = number /2
print(newNumber) 
```
## Inputs 

#### -> Inputs are used to allow the user to alter variables
```py
var1 = input("This is Where You Can Enter Your Input: ")
```
##### -> you can also change your input and translate it into a differnt type (str,int,float)
```py
var1 = str(input("This is Where You Can Enter Your Input: ")) # this takes your input and converts it into a string
var2 = int(input("This is Where You Can Enter Your Input: ")) # this takes your input and converts it into an intiger
var3 = float(input("This is Where You Can Enter Your Input: ")) # this takes yout input and converts it into a float
```
```py
name = input("Please Enter Your Name: ")
print("Hello "+ name + "!" )
```
## Structure of A Python 

### - Keywords -
- words that are reserved in the language
- in, is, False, True, print
### - Identifiers -
- not part of the langauge
- things you can define
- varriables
### - Literals -
- represents a value
- "Hello" -> is a string literal. (anything inside a "" or a '' is a string)
- 10 -> is a intiger literal. (any number that is a whole number)
- 10.5 -> is a float literal. (any number that is a decimal point, or a float number.)

### - Operators -
- instructions for what to do
- +, //, %, !=, ==0
- they are mathematical operators 
### - Keywords -
- False, None, True, And, As, Class
- can act as a delimeter
- can act as a value
- can act as operators
- !KEYWORDS ARE CASE SENSITIVE!
```py
print("Addition:", 10 + 50)
print("Subtraction:", 10 - 50)
print("Multiply:", 10 * 10)
print("Int div:", 5 // 2) # produces an int
print("Float div:", 5 / 2) # produces a float
print("Remainder:", 5 % 2) # modulo to provide remainder
print("These are Booleans:", True, False) # Boolean values
print("These are strings:", "true", "false") # strings
result = 10 * 2 - 5 // 2  # Watch the precedence
print(result)
print(10 ** 2 * 5)
print(10 * 2 ** 5) # exponent has highest precedence
print((100 - 5) * (10 + 90)) # brackets have highest precedence above operators
```
## Indendation and Dedentation
- shows the ide thet the next line of code is connected to that
- creates an indent token
- very important, shows the code whats next and wheter or not to execute it
```py
rainy = True

if rainy == True:
    print("You May Need An Umbrella")
else:
    print("You Dont Need An Umbrella")

termperature = -5

if termperature <= 0:
    print("Water Will Freeze")
else:
    print("Water Will Not Freeze")
```
## Compound Statements

- compound statements are a combination of other statements
- they are used to make an action

```py
temperature = 25
humid = True
if temperature > 25:
    print("its hot outside")
    if humid:
        ("its also humid")
        
print("outside of if")

```

## Conditions expressions
- reply in True or False
- can use not function to reverse true or false statements
```py
x = 5
y = 6

x > y # this will answer to false, since x is smaller than y
x == y # this will answer to false aswell, since x is not equal to y
x < y # this will answer to true, since x indeed is smalelr than y

# not uniary operator, can be applied to boolean values
not True
not False
```
## For Loops
- sets a range or lists every single item in a list or str or int
```py
myFavourite = ["Oranges", "Kiwis", "Grapefruit", "Mango"] # since this is a list, you can add or take away items in the list, and the code will still work. unlike a tuple

faveString = "My Favourites are "
for item in myFavourite[:-1]:
    faveString = faveString + item +", "
faveString = faveString + "and " + myFavourite[-1]

print(faveString)

# another solution using for loops and range

myFavourite = ["Oranges", "Kiwis", "Grapefruit", "Mango"]

faveString = "My Favourites are "

#instead of looping over items, we loop over indices of my list
# "len" to find the lenght of  string
for i in range(len(myFavourite)):
    # i will be from 0 upto len(myFavourite)-1
    # which is the same thing as the indices
    if i < len(myFavourite)-1:
        #if im not on the last line
        faveString = faveString + myFavourite[i] + ", "
    else:
        faveString = faveString + "and " + myFavourite[i]
print(faveString)
```
## While Statements
- while statements evaluates the expressions, if expressions are true it will proceed with the code, but if its false then the loop will stop
```py
code = False
while code:
    print("hello") # will not print hello
```
#### since the code = False, the code will not follow through and thhe output will not work
```py
word = ''
while len(word) < 8:
    word = input("Enter word: ") # will keep asking for in input, until the parameter is reached (until we enter an input that has the lenght greater than 8
```
#### this loop will keep asking for a input that is greater than 8 (len(word)<8) until its satisfied
```py
code = False
while code:
    print("hello") # will not print hello
```
```py
word = ''
while len(word) < 8:
    word = input("Enter word: ") # will keep asking for in input, until the parameter is reached (until we enter an input that has the lenght greater than 8
print(word)
```
## FILE I/O

### opening a file works in these 3 steps
1) reading files(r)
2) write(w)
3) append(a)

#### python opens files, asking the operating system if they are allowed to open or close the file.

#### 2 pieces of data is required.
- filename - (file path)
- filemode
```py
# opening a file
file = open("filename.txt")
# to read every line in file, we use a for loop
for line in file:
    print(line) # prints every line in the file
# read files individial
content = file.readline() # reads the first line, written again will read the second line... and so on
file.close() # is needed after gathering data
```
```py
# alice wc
file = open("alice.txt", "r", encoding="utf-8") # 
contents = file.read()
print(contents)
```
## Print Parameters
- different ways print can be used
```py
# print params

print(1,2,3) 
# >>> 1 2 3

print("a", "b", "c") 
# >>> a bc 

print("1 2 3\na b c") 
# prints
# >>> 1 2 3
# >>> a b c 

print('x','y', 'z', end= "*")
print('a', 'b', 'c')
# >>> x y z*a b c

x = "Hello"
y = "Friend"

print(x,y)
# >>> HelloFriend
# why does this not print "HelloFriend" ? Print is adding a a space inbetween arguements

print(x,y, sep="-")
# >>> Hello-Friend
print(1, 2, 3, 'a', 'b', 'c', sep="-")
# >>> 1-2-3-a-b-c
```
## User Defined Functions

-  like f(x) = 2x^2+3 - thats a functions, you can say x = 5 which would give you f(x) = 53. when x=5 thats called an arguements, f(5) is a function call. the answer, 53, would be called a return value (valuse produced by a function operation). no matter how many times i apply 5 into f, will produce 53, but in python, when i apply 5, it may vary depending on the return value

-  are a way for us to store code and use them later
```py
# relative to the md box
# -- these are all pure functions --
# -- no "sideeffects" = things that change the state of your program (changing a variables value, printing to the screen, or taking user input)

#f(x) = 2x^2 + 3
def f(x):
    2*x*x + 3
    value = x*x
    value = value*2
    value = value+3
    return value

#g(x) = x^2+3y
def g(x,y):
    return x*x+3*y

# t(p) = |p|*5-10
def t(p):
    return absolute(p)*5 - 10

print(t(10))


def absolute(x):
    if x >= 0:
        return x
    else:
        return -x

print(f(2))
print(f(4))
print(g(3,2))

print(absolute(5))
print(absolute(-5))
```
```py 
def pause():
    print("***************************")
    print("* press enter to continue *")
    print("***************************")    
    input()
name = input()
print(f"hello {name}")
pause()
print("have a nice day")
```
## Multi Dimensional Lists
```py
## Regular Lists
myList = ["Hello","Hi","How Are You?"]
## same thing as 
```
#### Matrices are lists of numbers
```py
matrix = [[1,2,3]
          [1,2,3],
          [1,2,3]]
```
```py
#rowsum
matrix1 = [[1,2,3],
           [7,7,7],
           [0,0,3]]

def rowsum(matrix,rowNum):
    total = 0
    for row in matrix:
        print(row)
```
```py
#column sum
matrix1 = [[1,2,3],
           [7,7,7],
           [0,0,3]]


def columnSum(matrix, columnNum):
    total = 0
    for row in matrix:
        total = total + row[columnNum]
    return total

print(columnSum(matrix1,0))
# >>> 8
print(columnSum(matrix1,1))
# >>> 9
print(columnSum(matrix1,2))
# >>> 13
```
```py
def createMatrix(numRows,numColumns):
    '''
    creates a matrix where the value at each row increases by 1 startting at 1, and the first item in each row is larger than the items at then end of th previous rows
    e.g
    createMatrix(3,3) -> [[1,2,3],
                          [4,5,6],
                          [7,8,9]]
    createMatrix(2,5) -> [[1,2,3,4,5],
                          [6,7,8,9,10]]
    '''
    matrix = []
    nextNum = 1
    for rowNum in range(numRows):
        row = []
        for columnNim in range(numColumns):
            row.append(nextNum)
            nextNumber += 1
        matrix.append(row)
    return matrix

print(createMatrix(2,3))
# >>> [[1,2,3],
#     [4,5,6]]
```
```py
matrix1 = [[1,2,3],
           [7,7,7],
           [0,0,3]]


def printMatrix(matrix):
    for row in matrix:
        rowString = "|"
        for val in row:
            rowString = rowString + str(val)
            rowString = rowString + ", "
        rowString = rowString + str(row[-1]) + " |"
        print(rowString)

printMatrix(matrix1)


def printRow(row):
    '''
    prints row 
    | 1, 2, 3 |
    '''
    outString = "| "
    for val in row[0;len(row)-1]:
        outString = outString + str(val) + ", "
    outString = outString
    ## incomplete



def printMatrix2(matrix):
    for row in matrix:
        print(row)
```
### Transpose of a Matrix
```py
matrix1 = [[1,2,3],
           [7,7,7],
           [0,0,3]]

def transposeMatrix(matrix):
    '''
    returns a transpose of a matrix
    '''
    numRows = len(matrix)
    numColumns = len(matrix[0])
    newMatrix = []
    for colNum in range(numColumns):
        col = getColumn(???):
```
## Dictionaries
```py
# Parallel lists, given some index i
# the person whos name is at the names[i] also has thier
# phone number at phoneNumbers [i]
names = ["Rob", "Mahmoud", "Yang-Tian", "Sadaf", "Ashley"]
phoneNumbers = ["555-3211", "555-7632", "555-9837", "555-1010", "555-2232"]

phoneBook = [["Rob", "555-3214"],
            ["Mahmoud", "555-3390"]]
def lookUpPhoneBook(name,pBook):
    ind = None
    for i in range(len(pBook)):
        if pBook[i][0] == name:
            ind = i
```
```py
def makePhoneBook(name,number):
    """
    makes a phonebook
    """
    phoneBook = {}
    # add to phonebook
    phoneBook[name] = number
    return phoneBook
def callNumber(adict,name):
    """
    calls phone number
    """
    number = adict.get(name,"Not in PhoneBook")
    return number
def main():
    C = True
    while C:
        choice = int(input("Please Choose An Option\n1) Add To PhoneBook\n2) Get Phone Number\n\n0) exit\n:"))
        if choice == 1:
            name = input("Please Enter A Name: ")
            number = input("Please Enter a Number: ")
            book = makePhoneBook(name,number)
            print(f"Added {name} into PhoneBook")
        elif choice == 2:
            name = input("Please Enter a Name To Get Thier Phonenumber: ")
            pnumber = callNumber(book,name)
            print(f"Phone Number for {name} is {pnumber}")
        elif choice == 0: break
        else:
            print("Incorrect Choice\n")
main()
```

## Json and API's

### What is JSON?
- a data format
- non proprietary, its not exclusive to a language
- very verstile, can work with a plethora of languages (JS, Python, PHP)
- Standardized
```py
import json

# this is what a json file looks like
{
    "speaker" : {
        "firstName" : "Larson",
        "lastName" : "Richard",
        "topics": ["JSON", "REST", "SOA"]
    }
}

#json can be parsed as a string.
# so these two are the same thing

pets_json = '{
    "cat": "meow",
    "dog": "woof",
    "bird": "tweet"
}'

pets_json = '{"cat": "meow", "dog": "woof", "bird": "tweet"}'

# to parse it we would use something like this. but remember to !! IMPORT JSON!!
pets = json.loads(pets_json)

dogs_json = '''[{"breed": "Labrador", "name": "Rover", "age": 3},
                {"breed": "Poodle", "name": "Fido", "age": 2},
                {"breed": "Collie", "name": "Lassie", "age": 1}]'''
dogs = json.load(dogs_json)
```
``` py
import json
# This is a Python dictionary
my_dict = {
    "carrot": "orange",
    "tomato": "red",
    "lettuce": "green"
}
# We can convert it into JSON
my_json = json.dumps(my_dict)

# json.dumps() copies a json from a dictionary or another json format
# json.load() loads or brings up a json formatfile

#What do you think is the type of my_json?

print(type(my_json))
```
```py
# word of advice, use pretty pring when working with json.
import pprint
pprint.pprint(my_json)
```

## Classes 
### what is a class?
- another type, a data type
- definition characterizes the properties and the behavior of a group of objects that are of a certain kind – exactly like a blueprint or skeleton!
```py
class <class name>:
```
- For example built-in types in Python, like an int, define how integer objects look like and behave

- It is convenient to be able to define new classes to represent things with similar properties and behaviour, which we can also manipulate

-  Used Primarily with OOP (object oriented programming)
- - based on concepts of objects and classes
- - a major programming paradigm  
- Classes make it easier to,
- - reuse code
- - maintain code
- - extend code over long periods of time
``` py
# for example, when a progrm deals with variables that stay the same for a while, like beartracks.
# it convenient to have a class for students that characterizes important properties and behavior

class <studentname>:
class <classinformation>:
class <studentid>:
class <classid>:
```



        
