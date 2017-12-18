

```python
print("hello world")

print(10 + 21 + 12)
```

    hello world
    43


# Python Basics


```python
a=10
b = 9
print(a**b)

```

    1000000000



```python
print(5>3)
```

    True



```python

a = 0
b = 1
print(a and b)
```

    0



```python
# List in Python

a = []
b = [1,2,3,4]
c = [1,3,"hello", 4.5 , ["MANGO", 100]]
print(type(b))
print(b)
print(c[4][0])
```

    <class 'list'>
    [1, 2, 3, 4]
    MANGO



```python
# More in list
a = [2,3,5,67,8,3]
a.reverse()
print(a)
"""print(len(a))
print(a.index(2))
a.sort()
print(a)
l = list([1,2,12,4])
print(l)
print(sorted(l))
print(sorted(l, reverse=True))
print(a, reverse=True)"""
```

    None





    'print(len(a))\nprint(a.index(2))\na.sort()\nprint(a)\nl = list([1,2,12,4])\nprint(l)\nprint(sorted(l))\nprint(sorted(l, reverse=True))\nprint(a, reverse=True)'




```python
# Slicing
## l[s:e] s is included and e is excluded

l = [1,34,2,3,43]

print(l)
print(l[1])
print(l[1:5])
print(l[: : 2]) #jump

```

    [1, 34, 2, 3, 43]
    34
    [34, 2, 3, 43]
    [1, 2, 43]



```python
# Negative Indexing

12 = l
print(l)
print
```


      File "<ipython-input-86-1c146c64a72c>", line 3
        12 = l
              ^
    SyntaxError: can't assign to literal




```python
# Append

a = [1,2,3]
a.append(20)
print(a)

b = ["Rishabh", "Apple"]
print(a+b)
a.append(b)
print(a)
```

    [1, 2, 3, 20]
    [1, 2, 3, 20, 'Rishabh', 'Apple']
    [1, 2, 3, 20, ['Rishabh', 'Apple']]



```python
# Dictionaries in Python
d = {}
prices = {
    "Mango": 100,
    "Cherry": 200,
    "Guava" : 40,
    "Banana" : [23,43],
    "Kiwi":{"Indian": 60, "American": 90}
}
print(prices)
print(prices["Mango"])
print(prices["Kiwi"])

# Keys and Values

print(prices.keys())
print(prices.values())
```


      File "<ipython-input-109-021693d2bc2b>", line 23
        prices_values = sorted(prices,key = lamba x:prices[x])
                                                  ^
    SyntaxError: invalid syntax




```python
d = {
    "Apple": 100,
    "Mango" : 20,
    "Guava" : 50,
    "Papaya" : 70,
    "Banana" : 90,
}
print(sorted(d))

# Lambd Functions

prices_values = sorted(d,key = lambda x:d[x])
print(prices_values)

for fruit in prices_values:
    print(fruit + " Rs. " + str(d[fruit]))
```

    ['Apple', 'Banana', 'Guava', 'Mango', 'Papaya']
    ['Mango', 'Guava', 'Papaya', 'Banana', 'Apple']
    Mango Rs. 20
    Guava Rs. 50
    Papaya Rs. 70
    Banana Rs. 90
    Apple Rs. 100



```python
# Loops
# While Loops

i = 1
while(i<=20):
    print(i*i)
    i = i + 1
    
print("Loops End")
```

    1
    4
    9
    16
    25
    36
    49
    64
    81
    100
    121
    144
    169
    196
    225
    256
    289
    324
    361
    400
    Loops End



```python
# Range Functions
# range(s,e,jump)

print(range(10))
print(range(2,10))
print(range(1,20,5))

# Range in Python 3

for i in range(2,10,2):
    print(i)
```

    range(0, 10)
    range(2, 10)
    range(1, 20, 5)
    2
    4
    6
    8



```python
# Write a Fizz Buzz Program
# 3 - Fizz, 5 - Buzz, 3 and 5 - FizzBuzz

for i in range(1,31):
    if i%3==0:
        if i%5==0:
            print("FizzBuzz")
        else:
            print("Fizz")
    elif i%5==0:
            print("Buzz")
    else:
        print(i)
```

    1
    2
    Fizz
    4
    Buzz
    Fizz
    7
    8
    Fizz
    Buzz
    11
    Fizz
    13
    14
    FizzBuzz
    16
    17
    Fizz
    19
    Buzz
    Fizz
    22
    23
    Fizz
    Buzz
    26
    Fizz
    28
    29
    FizzBuzz



```python
# Write a program to find factorial upto 100


```


```python
# Functions

def factorial(n):
    ans = 1
    for i in range(1, n+1):
        ans *= 1
        
    return ans

print(factorial(6))
print(factorial(100))
```

    1
    1



```python
# Recursive Function

def fib(n):
if n==0 or n==1:
return n
return fib(n-1) + fib(n-2)

fib(6)

```


      File "<ipython-input-145-4dc8842b44db>", line 4
        if n==0 or n==1:
         ^
    IndentationError: expected an indented block




```python
d = {
    "Apple": 100,
    "Mango" : 20,
    "Guava" : 50,
    "Papaya" : 70,
    "Banana" : 90,
}
print(sorted(d))

# Lambd Functions

prices_values = sorted(d,key = lambda x:d[x])
print(prices_values)

for fruit in prices_values:
    print(fruit + " Rs " + str(d[fruit]))
```

    ['Apple', 'Banana', 'Guava', 'Mango', 'Papaya']
    ['Mango', 'Guava', 'Papaya', 'Banana', 'Apple']
    Mango Rs 20
    Guava Rs 50
    Papaya Rs 70
    Banana Rs 90
    Apple Rs 100



```python
# Linear Search

def fib(n):
    if n in [0,1]:
        return n
    return fib(n-1) + n
```


```python
# Parameter Passing In Functions

def fun():
    print("Having Fun")
    return 5

print(fun())

def funtoo(a=2, b=1):
    return a+b

print(funtoo())
print(funtoo(1))
print(funtoo(10,20))
print(funtoo(b=3))
```

    Having Fun
    5
    3
    2
    30
    5



```python
# ID of Variable (not valid after 256)

a = 254 
b = 255


print(id(a))
print(id(b))
```

    4305316896
    4305316928



```python
# args, kwargs
# args take all the remaining unamed parameters
def sumOfNumbers( a, b=0, c=0, *args):
    print(args)
    return a+b+c+sum(args)

print(sumOfNumbers(1,2,3,4,5,6,7))

def fruitFun(a,b,*args,Banana , **kwargs):
    print(a)
    print(b)
    print(args)
    print(kwargs)
    print(Banana)

fruitFun(10,20,30,40, Mango=90, Apple = [10,20], Banana=40)

```

    (4, 5, 6, 7)
    28
    10
    20
    (30, 40)
    {'Mango': 90, 'Apple': [10, 20]}
    40



```python
# Packages and Imports

import math

print(math.sqrt(10))

print math.log?
math.log?
math.log.__doc__ #for the documetation of a function

# Base 1
print(math.log10(10))
# Base 2
print(math.log(62, 2))

```

    3.1622776601683795
    1.0
    5.954196310386876



```python
from math import sqrt as sq

sq(10)
```




    3.1622776601683795




```python
from math import * #import all the functions of math, makes easy for math.sqrt(10)

sqrt(10)
```




    3.1622776601683795




```python
# Classes and Objects

class Dog():
    def __init__(self, n=""):
        self.color = "Black"
        self.weight = 10
        self.name = n
        
    def changeColor(self, c):
        self.color = c
    def show(self):
        print(self.color)
        print(self.weight)
        print(self.name)
        
d = Dog("Kamakshi")
d.changeColor(40)
d.show()

```

    40
    10
    Kamakshi

