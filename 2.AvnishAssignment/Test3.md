\*\*\*Instructions: Attempt all questions. Write proper Python syntax, use meaningful variable names, and provide complete code for programming questions.



\*\*Section A – Very Short Answer Questions



Q1. Which function is used to open a file in Python?

Ans: open()



Q2. Write the syntax for opening a file in read mode.

Ans: "r" 



Q3. What is a lambda function?

Ans: A lambda function is a small and nameless function that is written in a single line.



Q4. Write one example of a lambda function that adds two numbers.

Ans: add = lambda a, b: a + b

&#x20;    print(add(5, 3))



Q5. What is List Comprehension?

Ans: List comprehension in python is short and simple way to create a new list using a single line of code. 



Q6. Which Python module is commonly used to work with JSON data?

Ans: JSON module is commonly used to work with JSON data.



Q7. What does JSON stand for?

Ans: JSON:-JavaScript Object Notation



Q8. What is an API?

Ans: An API ('Application Programming Interface') is a set of rules that allows different software to communicate and share data with each other.



Q9. What is a decorator in Python?

Ans: A decorator in Python is a function that is used to modify or extend the behavior of another function without changing its code.



Q10. What is a generator function?

Ans: A generator function is a function that produces values one at a time instead of returning all values at once.



\*\*Section B – Short Answer / Coding Questions



Q11. Write Python code to create a file named data.txt and write the following text into it: 

Python is easy to learn. 

Python is powerful.

Ans: file = open("data.txt", "w")

&#x20;    file.write("Python is easy to learn.")

&#x20;    file.write("Python is powerful.")

&#x20;    file.close()



Q12. Write Python code to read the complete contents of data.txt.

Ans: file = open("data.txt", "r")

&#x20;    content = file.read()

&#x20;    print(content)

&#x20;    file.close()



Q13. Write a lambda function to find the square of a number.

Ans: square = lambda x: x \* x

&#x20;    print(square(5))



Q14. Using lambda, find the maximum of two numbers.

Ans: maximum = lambda a, b: max(a, b)

&#x20;    print(maximum(10, 20))



Q15. Create a list containing squares of numbers from 1 to 10 using List Comprehension.           

Ans: squares = \[x \* x for x in range(1, 11)]

&#x20;    print(squares)



Q16. Create a list containing only even numbers from 1 to 20 using List Comprehension.

Ans: even\_numbers = \[x for x in range(1, 21) if x % 2 == 0]

&#x20;    print(even\_numbers)



Q17. Write Python code to convert the following dictionary into a JSON string: 

student = {'name': 'Rahul', 'age': 22, 'course': 'Python'}

Ans: import json



&#x20;    student = {'name': 'Rahul', 'age': 22, 'course': 'Python'}

&#x20;    json\_string = json.dumps(student)

&#x20;    print(json\_string)



Q18. Write Python code to convert the following JSON string into a Python dictionary: 

data = '{"name": "Rahul", "age": 22}'

Ans: import json



&#x20;    data = '{"name": "Rahul", "age": 22}'

&#x20;    student = json.loads(data)

&#x20;    print(student)



Q19. Write the basic syntax of a Python decorator and explain the role of @.

Ans: Basic syntax of a Python decorator:-  

&#x20;    The @ symbol is used to apply a decorator to a function.



Q20. Write a generator function that generates numbers from 1 to 5 using yield.

Ans: num = \[1,2,3,4,5,6]

&#x20;    for i in range(1, 6):

&#x20;     for num in numbers():

&#x20;      print(num)



\*\*Section C – Long Answer / Programming Questions



Q21. File Reading and Writing – 5 Marks

&#x20;Write a Python program that: 

1\. Creates a file named student.txt. 

2\. Writes the names of 5 students into the file. 

3\. Reads the file. 

4\. Displays all student names on the screen. Use appropriate file modes and with open().

Ans: with open("student.txt", "w") as file:

&#x20;     file.write("Rahul\\n")

&#x20;     file.write("Amit\\n")

&#x20;     file.write("Priya\\n")

&#x20;     file.write("Sneha\\n")

&#x20;     file.write("Rohan\\n")

&#x20;    with open("student.txt", "r") as file:

&#x20;     students = file.read()

&#x20;     print("Student Names:")

&#x20;     print(students)



Q22. Lambda + List Comprehension – 5 Marks Write a Python program that: 

1\. Creates the list: numbers = \[1,2,3,4,5,6,7,8,9,10] 

2\. Uses List Comprehension to create a list of even numbers. 

3\. Uses a lambda function to calculate the square of every even number. 

4\. Displays the final result. 

Expected output: \[4, 16, 36, 64, 100]

Ans: numbers = \[1, 2, 3, 4, 5, 6, 7, 8, 9, 10]

&#x20;    even\_numbers = \[num for num in numbers if num % 2 == 0]

&#x20;    square = lambda x: x \* x

&#x20;    result = \[square(num) for num in even\_numbers]

&#x20;    print(result)



Q23. JSON + API – 5 Marks 

Answer the following: 

(a) What is JSON and why is it commonly used with APIs? 

(b) Write Python code using the requests library to send a GET request to an API. 

import requests 

url = "https://api.example.com/data" 

response = requests.get(url) 

print(response.status\_code) 

print(response.json()) 

Explain the purpose of requests.get(), response.status\_code, and response.json().

Ans(a):JSON (JavaScript Object Notation) is a lightweight data format used to store and exchange data.It is easy foe us to understand,read and write.It is commanly used because:-

✔️It is simple and lightweight.

✔️It can represent structured data using key-value pairs.

✔️It is supported by many programming languages.

Ans(b): import requests



&#x20;       url = "https://api.example.com/data"

&#x20;       response = requests.get(url)

&#x20;       print(response.status\_code)

&#x20;       print(response.json())



Q24. Decorator + Generator – 5 Marks

&#x20;

Part A – Decorator: Create a decorator named login\_required that prints "Login Required" before executing a function. 

@login\_required 

def dashboard(): 

&#x20;   print("Welcome to Dashboard")



Ans: def login\_required(func):

&#x20;      def wrapper():

&#x20;        print("Login Required")

&#x20;        func()

&#x20;   return wrapper

@login\_required

def dashboard():

&#x20;   print("Welcome to Dashboard")

dashboard()



Part B – Generator: Create a generator function named count\_numbers() that generates numbers from 1 to 5 using yield. Display the generated values using a for loop.s

Ans: def count\_numbers():

&#x20;   for i in range(1, 6):

&#x20;       yield i

&#x20;   for number in count\_numbers():

&#x20;       print(number)

