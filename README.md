# week3-file-handling and error-handling

*Q1. How to open, read, and write to .txt files in Python?*

```python

    with open("sample.txt", "w") as file: (writing from a file)
    
    file.write("Hello, this is my first file!\n")

    with open("sample.txt", "r") as file: (reading from a file)
    
    content = file.read()
    
    print(content)

```

-- OUTPUT: Hello, this is my first file! 

*Q2. How to open and read a .csv file in Python?*

```python

import csv

with open("students.csv", "w", newline="") as file:
    writer = csv.writer(file)
    writer.writerow(["Name", "Score"])
    writer.writerow(["Alice", 85])
    writer.writerow(["Bob", 90])
import csv

with open("students.csv", "r") as file:
    reader = csv.reader(file)
    for row in reader:
        print(row)

```
 --OUTPUT: ['Name', 'Score']
           ['Alice', '85']
            ['Bob', '90']

*Q3. What is error handling in Python?*

Error handling means managing errors smoothly without crashing the program.

We use try, except, and finally.

```python

try:
    number = int(input("Enter a number: "))
    print("You entered:", number)
except ValueError:
    print("Oops! That was not a valid number.")
finally:
    print("Program ended.")

```
--OUTPUT:Enter a number: abc

Oops! That was not a valid number.

Program ended.

*Q4. How to read and write a text file in Python?*

We can use the open() function to read and write text files.

```python

with open("notes.txt", "w") as file:
    file.write("Hello, this is my first file.\n")
    file.write("Python makes it easy!")

with open("notes.txt", "r") as file:
    content = file.read()
    print(content)

```

--OUTPUT: Hello, this is my first file.

Python makes it easy!






 
 
  
