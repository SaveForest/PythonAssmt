
""" Task 1
- Define a class named Car with attributes: make, model, year
- Initialize these attributes in the __init__ method
- Add a method named describe_car() that prints information about the car as "Year Make Model"    
"""
# Task 2
# Create an instance of the Car class with the following attributes and call describe_car method:
# - Make: Toyota, Model: Corolla, Year: 2020 

class Car:
	def __init__(self, make, model, year):
		self.make = make
		self.model = model
		self.year = year
	def describe_car(self):
		print("Q7 ", self.make,self.model,self.year)
newCar = Car("Toyota", "Corolla", 2020)
newCar.describe_car()

""" Task 1
- Create a function that finds the first negative number in a list (lst).
- Return the first negative number if found, otherwise return "No negatives".
- Use a while loop to implement this."""
# Task 2
# Invoke the function "find_first_negative" using the following scenario:
# - [3, 5, -1, 7, -2, 8]
# - [2, 10, 7, 0]
#def find_first_negative(lst):

def find_first_negative(zlist):
	a = len(zlist)
	i = 0
	while i < a:
		if zlist[i] >= 0:
			i += 1
		else: 
			print("Q6 1st neg:", zlist[i])
			break
find_first_negative([3, 5, -1, 7, -2, 8])
find_first_negative([2, 10, 7, 0])

""" Task 1
- Create a function to check if the number (num) is divisible by another number (divisor).
- Both num and divisor must be numeric.
- Return True if num is divisible by divisor, False otherwise."""
# Task 2
# Invoke the function "check_divisibility" using the following scenarios:
# - 10, 2
# - 7, 3

def check_divisibility(num, divisor):
	numeric = (int, float)
	if type(num) not in numeric and type(divisor) not in numeric:
		print(f"Q5. ValueError!")
	else:
		print(f"Q5 ", bool(num % divisor))
	return(num, divisor)
check_divisibility(-10, 2)
check_divisibility(-7, 3)

"""    Task 1
- Create a function that reverses a given string (s).
- s must be a string.
- Return the reversed string. """
# Task 2
# Invoke the function "string_reverse" using the following scenarios:
# - "Hello World"
# - "Python"

def string_reverse(s):
	print("Q4 Reverse Str ", s[::-1])
	return s
string_reverse("Hello World")
string_reverse("Python")

"""    Task 1
    - Create a function that updates a dictionary (dct) with a new key-value pair.
    - If the key already exists in dct, print the original value, then update its value.
    - Return the updated dictionary."""
# Task 2
# Invoke the function "update_dictionary" using the following scenarios:
# - {}, "name", "Alice"
# - {"age": 25}, "age", 26

def update_dictionary(dct, key, value):
	if dct != {}:
		print(f"Q3 Original value: ", dct.get(key))
	dct[key] = value
	print(f"Q3 Update new value: ", dct.values())
	return dct

update_dictionary({}, "name", "Alice")
update_dictionary({"age": 25}, "age", 26)

"""    Task 1
- Create a function that searches for all occurrences of a value (find_val) in a given list (lst) and replaces them with another value (replace_val).
    - lst must be a list.
    - Return the modified list."""
# Task 2
# Invoke the function "find_and_replace" using the following scenarios:
# - [1, 2, 3, 4, 2, 2], 2, 5
# - ["apple", "banana", "apple"], "apple", "orange"

# 1st is illegal variable name
def find_and_replace(flist, find_val, replace_val):
	for ea in range(len(flist)):
		if flist[ea] == find_val:
			flist[ea] = replace_val
			ea +1
	print("Q2", flist)
	return flist

find_and_replace(["apple", "banana", "apple"], "apple", "orange")
find_and_replace([1, 2, 3, 4, 2, 2], 2, 5)

"""Task 1
- Create a function that would swap the value of x and y using only x and y as variables.
- x and y must be numeric.
- Return -1 if x and y is not numeric, and
- print the swapped values if both x and y are numeric.
Task 2
Invoke the function "swap" using the following scenarios:
- "Apple", 10
- 9, 17
"""
def swapXY(x, y):
	x, y = y, x
	if isinstance(x, int) == True and isinstance(y, int) == True:
		print(f"Q1 x: ", x, " y: ", y)
	elif isinstance(x, int) == False or isinstance(y, int) == False:
		return(-1)

swapXY(9, 7)
swapXY("Apple", 10)
