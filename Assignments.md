Q1. Which keyword is used to create a function? Create a function to return a list of odd numbers in the
range of 1 to 25.
Ans- def get_odd_numbers():
    return [num for num in range(1, 26) if num % 2 != 0]

# Calling the function
odd_numbers = get_odd_numbers()
print(odd_numbers)
Out Put- 
[1, 3, 5, 7, 9, 11, 13, 15, 17, 19, 21, 23, 25]
This function uses list comprehension to filter odd numbers from 1 to 25.
‘OR’
l=[1,2,3,4,5,66,7,8,9,10,11,12,13,14,15,16,17,18,19,20,21,22,23,24,25]
list(filter(lambda x:x%2!=0,l))
Out Put-
[1, 3, 5, 7, 9, 11, 13, 15, 17, 19, 21, 23, 25]
------------------------------------------------------------------------------------------------------------------------------------------
Q2. Why *args and **kwargs is used in some functions? Create a function each for *args and **kwargs
to demonstrate their use.
Ans- 
*args and `**kwargs are used in functions to handle a variable number of arguments.  

- *args allows a function to accept any number of **positional arguments** as a tuple.  
- **kwargs allows a function to accept any number of **keyword arguments** as a dictionary.  

# Example Function Using `*args
This function takes multiple numbers as arguments and returns their sum.  

def sum_numbers(*args):
    return sum(args)

# Calling the function
print(sum_numbers(1, 2, 3, 4, 5))  
# Output: 15
print(sum_numbers(10, 20))         
# Output: 30


## Example Function Using **kwargs
This function accepts multiple keyword arguments and prints them in key-value pairs.  


def print_info(**kwargs):
    for key, value in kwargs.items():
        print(f"{key}: {value}")

# Calling the function
print_info(name="Ajay", age=30, city="Varanasi")

Output:
name: Ajay
age: 30
city: Varanasi


# Summary:
- Use `*args when you need to pass **multiple positional arguments**.
- Use `**kwargs when you need to pass **multiple keyword arguments**.


Q3. What is an iterator in python? Name the method used to initialise the iterator object and the method?
Ans – 
An iterator in Python is an object that allows traversal through a sequence (such as a list, tuple, or string) one element at a time. It follows the Iterator Protocol, which consists of two methods:

__iter__() → Initializes the iterator object.

__next__() → Returns the next item from the sequence.

Example of an Iterator
class MyIterator:
    def __init__(self):
        self.num = 1  # Initialize starting value
    
    def __iter__(self):
        return self  # Returns the iterator object itself
    
    def __next__(self):
        if self.num > 5:
            raise StopIteration  # Stops when the condition is met
        value = self.num
        self.num += 1
        return value

# Creating an iterator object
iterator_obj = MyIterator()

# Using the iterator
for num in iterator_obj:
    print(num)
Out Put -
1
2
3
4
5

used for iteration. Use these methods to print the first five elements of the given list [2, 4, 6, 8, 10, 12, 14,
16, 18, 20].

Q4. What is a generator function in python? Why yield keyword is used? Give an example of a generator
function.
Ans- 
A generator function is a special type of function that returns an iterator but does not store all values in memory. Instead of return, it uses the yield keyword to generate values lazily, meaning it produces values one at a time as needed.
yield pauses the function execution and remembers its state.

When the function is called again, it resumes from where it left off instead of starting over.

It is memory-efficient since it does not store all values at once, making it ideal for large datasets.
Example of a Generator Function
This generator function produces odd numbers from 1 to 10 one at a time:

def odd_numbers():
    for num in range(1, 11, 2):
        yield num  # Yielding each odd number

# Using the generator function
gen = odd_numbers()

# Fetching values one by one
for value in gen:
    print(value)
Out Put-
1
3
5
7
9

Q5. Create a generator function for prime numbers less than 1000. Use the next() method to print the
first 20 prime numbers.
Ans- 
Generator Function for Prime Numbers Less Than 1000
A prime number is a number greater than 1 that has no divisors other than 1 and itself. Below is a generator function that yields prime numbers less than 1000 one by one.
def is_prime(n):
    """Helper function to check if a number is prime."""
    if n < 2:
        return False
    for i in range(2, int(n ** 0.5) + 1):
        if n % i == 0:
            return False
    return True

def prime_generator():
    """Generator function to yield prime numbers less than 1000."""
    num = 2  # Start from the first prime number
    while num < 1000:
        if is_prime(num):
            yield num  # Yield the prime number
        num += 1

# Creating the generator object
primes = prime_generator()

# Using next() to print the first 20 prime numbers
for _ in range(20):
    print(next(primes))
Out Put
2
3
5
7
11
13
17
19
23
29
31
37
41
43
47
53
59
61
67
71

Q6. Write a python program to print the first 10 Fibonacci numbers using a while loop.
Ans- 
range(10)
range(0, 10)
for i in range(10):
    print (i)
0
1
2
3
4
5
6
7
8
9
def test_fib(n):
    a,b=0,1
    for i in range(n):
        yield a
        a,b=b,a+b
for i in test_fib(10):
    print(i)
0
1
1
2
3
5
8
13
21
34
def test_fib1():
    a,b=0,1
    while True:
        yield a
        a,b=b, a+b
fib=test_fib1()
for i in range(10):
    print(next(fib))
0
1
1
2
3
5
8
13
21
34

Q7. Write a List Comprehension to iterate through the given string: ‘pwskills’.
Expected output: ['p', 'w', 's', 'k', 'i', 'l', 'l', 's']
Ans- 
I can use list comprehension to iterate through the string 'pwskills' and store each character in a list.
string = "pwskills"
char_list = [char for char in string]
print(char_list)

Out Put-
['p', 'w', 's', 'k', 'i', 'l', 'l', 's']

Q8. Write a python program to check whether a given number is Palindrome or not using a while loop.
Ans- 
Python Program to Check if a Number is a Palindrome Using a While Loop
A palindrome number is a number that reads the same forward and backward (e.g., 121, 1331, 454).

def is_palindrome(num):
    original_num = num  # Store the original number
    reversed_num = 0  # Initialize reversed number
    
    while num > 0:
        digit = num % 10  # Get the last digit
        reversed_num = reversed_num * 10 + digit  # Append the digit to reversed number
        num //= 10  # Remove the last digit
    
    return original_num == reversed_num  # Check if original and reversed numbers are the same

# Input from user
num = int(input("Enter a number: "))

# Check if palindrome
if is_palindrome(num):
    print(f"{num} is a Palindrome.")
else:
    print(f"{num} is not a Palindrome.")
Example Runs-
Input:
Enter a number: 121
Out Put- 
121 is a Palindrome.
Input:
Enter a number: 123
Out Put-
123 is not a Palindrome.

Q9. Write a code to print odd numbers from 1 to 100 using list comprehension.
Note: Use a list comprehension to create a list from 1 to 100 and use another List comprehension to filter
out odd numbers.
Ans- 
You can achieve this in two steps using nested list comprehensions:

Create a list from 1 to 100.

Use another list comprehension to filter odd numbers.
# Step 1: Create a list of numbers from 1 to 100
numbers = [num for num in range(1, 101)]

# Step 2: Filter out odd numbers from the list
odd_numbers = [num for num in numbers if num % 2 != 0]

# Print the odd numbers
print(odd_numbers)
Out Put- 
[1, 3, 5, 7, 9, 11, 13, 15, 17, 19, 21, 23, 25, 27, 29, 31, 33, 35, 37, 39, 
 41, 43, 45, 47, 49, 51, 53, 55, 57, 59, 61, 63, 65, 67, 69, 71, 73, 75, 77, 79, 
 81, 83, 85, 87, 89, 91, 93, 95, 97, 99]
