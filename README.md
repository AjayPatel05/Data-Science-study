Q1. Create one variable containing following type of data:
(i) string
(ii) list
(iii) float
(iv) tuple
Ans- 
Creating a variable containing different data types
Mixed variable = ("Hello", [1, 2, 3], 3.14, (5, 6))
In the above variable:
•	"Hello" is a string.
•	[1, 2, 3] is a list.
•	3.14 is a float.
•	(5, 6) is a tuple.
Q2. Given are some following variables containing data:
(i) var1 = ‘ ‘
(ii) var2 = ‘[ DS , ML , Python]’
(iii) var3 = [ ‘DS’ , ’ML’ , ‘Python’ ]
(iv) var4 = 1.
Ans- 
var1 = ' '  
# var1 is a string
var2 = '[ DS , ML , Python]'  
# var2 is a string (because of the quotes)
var3 = ['DS', 'ML', 'Python']  
# var3 is a list
var4 = 1.  
# var4 is a float (note the period)
Q3. Explain the use of the following operators using an example:
(i) /
(ii) %
(iii) //
(iv) **
Ans- 
Division (/): result = 10 / 3  
Region- result is 3.3333 (float division)
Modulus (%): remainder = 10 % 3  
Region- remainder is 1 (10 divided by 3 leaves a remainder of 1)
Floor Division (//): quotient = 10 // 3  
Region- quotient is 3 (integer division)
Exponentiation (**): power = 2 ** 3  
Region- power is 8 (2 raised to the power of 3)
Q4. Create a list of length 10 of your choice containing multiple types of data. Using for loop print the
element and its data type.
Ans-
l= [1, "Hello", 3.14, True, [1, 2], (3, 4), {5, 6}, {"key": "value"}, None, complex(2, 3)]
for i in l:
    print(type(i))
<class 'int'>
<class 'str'>
<class 'float'>
<class 'bool'>
<class 'list'>
<class 'tuple'>
<class 'set'>
<class 'dict'>
<class 'NoneType'>
<class 'complex'>

Q5. Using a while loop, verify if the number A is purely divisible by number B and if so then how many times it can be divisible.
Ans- 
A = 100
B = 5
count = 0

while A % B == 0:
    A //= B
    count += 1

print(f"Number is divisible {count} times.")

Number is divisible 2 times.

Q6. Create a list containing 25 int type data. Using for loop and if-else condition print if the element is divisible by 3 or not.
Ans-
numbers = list(range(1, 26))
for num in numbers:
    if num % 3 == 0:
        print(f"{num} is divisible by 3")
    else:
        print(f"{num} is not divisible by 3")

Q7. What do you understand about mutable and immutable data types? Give examples for both showing this property.
Ans-
Mutable Data Types: These are data types whose values can be changed after they are created. Example: lists.
my_list = [1, 2, 3]
my_list[0] = 100  
# Changing the first element

Immutable Data Types: These are data types whose values cannot be changed after they are created. Example: tuples.
my_tuple = (1, 2, 3)
# my_tuple[0] = 100  
# This will raise an error

Which of the following data types in Python is mutable? int float tuple list
ChatGPT said:
ChatGPT
Among the data types listed, list is mutable.
•	int (integer) is immutable.
•	float is immutable.
•	tuple is immutable.
•	list is mutable, meaning its elements can be changed after it is created.
4o
You said:
Which of the following data types in Python is immutable? set dict list str
ChatGPT said:
ChatGPT
Among the data types listed, str (string) is immutable.
•	set is mutable.
•	dict (dictionary) is mutable.
•	list is mutable.
•	str (string) is immutable, meaning once a string is created, it cannot be changed.
4o
You said:
Which of the following operations can be performed on immutable objects? Appending new elements Removing elements Modifying elements None of the above
ChatGPT said:
ChatGPT
The correct answer is None of the above.
Immutable objects in Python cannot be changed after they are created, so you cannot perform operations like appending new elements, removing elements, or modifying elements on them. If you need to change an immutable object, you would have to create a new object with the desired modifications.
4o
You said:
What happens when you assign a new value to an existing variable of an immutable data type? The existing object is modified with the new value. A new object is created with the new value and assigned to the variable. An error occurs as you cannot assign a new value to an existing variable of an immutable data type. None of the above.
ChatGPT said:
ChatGPT
The correct answer is:
A new object is created with the new value and assigned to the variable.
When you assign a new value to an existing variable of an immutable data type (like a string, integer, or tuple), Python creates a new object with the new value and assigns it to the variable. The original object remains unchanged, and the variable now points to the new object.
4o
You said:
Consider the following code: my_list = [1, 2, 3] new_list = my_list new_list.append(4) print(my_list) What will be the output of the above code? [1, 2, 3] [1, 2, 3, 4] [1, 2, 3, 3, 4] Error
ChatGPT said:
ChatGPT
The correct answer is:
[1, 2, 3, 4]
Here's why:
•	my_list = [1, 2, 3] creates a list [1, 2, 3] and assigns it to my_list.
•	new_list = my_list does not create a new list; it simply makes new_list another reference to the same list object in memory as my_list.
•	new_list.append(4) modifies the list in place, adding 4 to the existing list.
•	Since both my_list and new_list refer to the same list, the change is reflected in both variables.
Thus, print(my_list) will output [1, 2, 3, 4]

