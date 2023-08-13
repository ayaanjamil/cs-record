<h1>Class 12 Record Programs</h1>
1. Write a menu driven program to compute,
a. Factorial of a given integer
b. Fibonacci series up to the given number n
c. Check whether the given integer is palindrome or not
```py
while True:
    print("1. Factorial of a number")
    print("2. Fibonacci series")
    print("3. Check palindrome")
    print("4. Exit")
    choice = int(input("Enter your choice: "))
    
    if choice == 1:
        num = int(input("Enter a number: "))
        factorial = 1
        for i in range(1, num + 1):
            factorial *= i
        print("Factorial:", factorial)
    elif choice == 2:
        n = int(input("Enter the number of terms: "))
        fib_series = [0, 1]
        while len(fib_series) < n:
            fib_series.append(fib_series[-1] + fib_series[-2])
        print("Fibonacci Series:", fib_series)
    elif choice == 3:
        num = int(input("Enter a number: "))
        num_str = str(num)
        if num_str == num_str[::-1]:
            print("Palindrome")
        else:
            print("Not Palindrome")
    elif choice == 4:
        break
    else:
        print("Invalid choice")

```
<br>

2. Write a program to accept the list of marks for  subjects from the user for n students and do the following,
a. Print highest mark scored
b. Print the number of students scored less than 40
c. Compute the average marks
d. Compute the percentage of marks scored
```py
n = int(input("Enter the number of students: "))
marks_list = []
for i in range(n):
    marks = float(input("Enter the marks: "))
    marks_list.append(marks)

highest_mark = max(marks_list)
print("Highest Mark:", highest_mark)

below_40 = sum(1 for mark in marks_list if mark < 40)
print("Students scored below 40:", below_40)

average_marks = sum(marks_list) / n
print("Average Marks:", average_marks)

percentage = (below_40 / n) * 100
print("Percentage of students scored below 40:", percentage)
```
<br>

3. Write a python program to input ‘n’ customers and their details like items bought, cost and phone number etc. Store them in a dictionary and display all the details in a tabular form.
```py
n = int(input("Enter the number of customers: "))
customers = []
for i in range(n):
    details = {}
    details['name'] = input("Enter customer name: ")
    details['items_bought'] = input("Enter items bought: ")
    details['cost'] = float(input("Enter cost: "))
    details['phone_number'] = input("Enter phone number: ")
    customers.append(details)

print("Customer Details:")
print("Name\tItems Bought\tCost\tPhone Number")
for customer in customers:
    print(f"{customer['name']}\t{customer['items_bought']}\t{customer['cost']}\t{customer['phone_number']}")
```
<br>

4. Write a program using function that takes amount – in – dollars and dollar – to – rupee conversion price, it then returns the amount converted to rupees. Create a function in both void and non-void forms.
```python
def convert_to_rupees(amount, conversion_rate):
    return amount * conversion_rate

def convert_to_rupees_void(amount, conversion_rate):
    converted_amount = amount * conversion_rate
    print("Amount in Rupees:", converted_amount)

amount_in_dollars = float(input("Enter amount in dollars: "))
conversion_rate = float(input("Enter conversion rate: "))
converted_amount = convert_to_rupees(amount_in_dollars, conversion_rate)
print("Amount in Rupees:", converted_amount)

convert_to_rupees_void(amount_in_dollars, conversion_rate)
```
<br>

5. Write a program using function to calculate volume of a box with appropriate default values for its parameters. Your function should have the following input parameters,
a. Length of box
b. Width of box
c. Height of box
```python
def calculate_volume(length=1, width=1, height=1):
    return length * width * height

length = float(input("Enter length of the box: "))
width = float(input("Enter width of the box: "))
height = float(input("Enter height of the box: "))
volume = calculate_volume(length, width, height)
print("Volume of the box:", volume)
```
<br>

6. Write a program with a definition of a method COUNTNOW(PLACES) to find and display those places names in which there are more than 5 characters after storing the names of places in a dictionary.
```python
def count_places_with_more_than_5_chars(places_dict):
    result = []
    for place in places_dict.values():
        if len(place) > 5:
            result.append(place)
    return result

places = {
    1: "Chennai",
    2: "Los Angeles",
    3: "New York",
    4: "Delhi",
    5: "Hyderabad"
}

places_with_more_than_5_chars = count_places_with_more_than_5_chars(places)
print("Places with more than 5 characters:", places_with_more_than_5_chars)

```
<br>

7. Write an application based program (payroll, electricity bill, phone bill etc) to implement LEGB rule and global keyword.
```python
global_var = 10

def local_scope_demo():
    local_var = 20
    print("Local Variable:", local_var)
    print("Global Variable Inside Function:", global_var)

local_scope_demo()
print("Global Variable Outside Function:", global_var)
```
<br>

8. Write a program to implement the guessing game as per the following criteria.
a. To guess an integer number
b. To guess a floating point number
c. To guess a character from a list of character elements
```python
import random

def guess_integer():
    target = random.randint(1, 100)
    while True:
        guess = int(input("Guess an integer between 1 and 100: "))
        if guess == target:
            print("Congratulations! You guessed it right.")
            break
        elif guess < target:
            print("Try a higher number.")
        else:
            print("Try a lower number.")

def guess_float():
    target = round(random.uniform(0, 1), 2)
    while True:
        guess = float(input("Guess a floating-point number between 0 and 1 (upto two decimals): "))
        if round(guess, 2) == target:
            print("Congratulations! Right guess!")
            break
        else:
            print("Try again.")

def guess_character():
    characters = ['a', 'b', 'c', 'd', 'e']
    target = random.choice(characters)
    while True:
        guess = input("Guess a character (a, b, c, d, e): ")
        if guess == target:
            print("Correct!")
            break
        else:
            print("Try again.")

print("1. Guess an integer number")
print("2. Guess a floating-point number")
print("3. Guess a character")
choice = int(input("Enter your choice: "))

if choice == 1:
    guess_integer()
elif choice == 2:
    guess_float()
elif choice == 3:
    guess_character()
else:
    print("Invalid choice")
```
<br>

9. Read a text file line by line and display each word separated by a #.
```python
with open("myfile.txt", "r") as f:
    for line in f.readlines():
        for word in line:
        print(word, end='#')
```
<br>

10. Write a program to find the number of upper case, no of lower case, number of digits, no of vowels, no of consonants, no of special characters and numbers of lines in a text file.
```python
upper_count = lower_count = digit_count = 0
vowel_count = consonant_count = 0
special_char_count = line_count = 0
vowels = 'aeiouAEIOU'
with open("textfile.txt", "r") as file:
    for line in file:
        line_count += 1
        for char in line:
            if char.isupper():
                upper_count += 1
            elif char.islower():
                lower_count += 1
            if char in vowels:
                vowel_count += 1
            elif char.isalpha() and char not in vowels:
                consonant_count += 1
            elif char.isdigit():
                digit_count += 1
            elif char.isspace():
                continue
            else:
	            special_char_count += 1

print("Number of Uppercase characters:", upper_count)
print("Number of Lowercase characters:", lower_count)
print("Number of Digits:", digit_count)
print("Number of Vowels:", vowel_count)
print("Number of Consonants:", consonant_count)
print("Number of Special Characters:", special_char_count)
print("Number of Lines:", line_count)
```
<br>

11. Write a program to remove all the lines that contains the character ‘A’ or ‘a’ in a file and write it to another file.
```python
with open("input.txt", "r") as input_file:
	with open("output.txt", "w") as output_file:
	    for line in input_file.readlines():
	        if 'A' not in line and 'a' not in line:
	            output_file.write(line)
```
<br>

12. Create a file named “test_report.txt”, write a function capitalize_sentence() to create a copy of file “test_report.txt” name it as “file.txt”, which should convert the first letter of the file and the first alphabetic character following a full stop into upper case.
```python
def capitalize_sentence(sentence):
    words = sentence.split()
    capitalized_words = []
    for word in words:
	    if word.isalpha():
		    capitalized_words.append(word.capitalize())
		else:
			capitalized_words.append(word)
    return ' '.join(capitalized_words)

with open("test_report.txt", "r") as input_file:
	with open("file.txt", "w") as output_file:
	    for line in input_file.readlines():
	        capitalized_line = capitalize_sentence(line)
	        output_file.write(capitalized_line)

```
<br>

13. Take a sample of ten phishing e-mails (or any text file) and find most commonly occurring word(s)
```python
def count_words(words_list):
    word_counts = {}
    for word in words_list:
        word = word.lower()
        if word in word_counts:
            word_counts[word] += 1
        else:
            word_counts[word] = 1
    return word_counts

def get_count(item):
    return item[1]

def most_common_words(word_counts, n=5):
    sorted_words = sorted(word_counts.items(), key=get_count, reverse=True)
    return sorted_words

with  open("phishing_emails.txt", "r") as file:
	words = file.read().split()

word_counts = count_words(words)
most_common = most_common_words(word_counts)

print("Most commonly occurring words:")
for word, count in most_common:
    print(f"{word}: {count} occurrences")
```
<br>

14. Write a menu driven program to perform all the basic operations using dictionary on student binary file such as inserting, updating, searching and deleting a record.
a. Insert records with the following data  (data includes USN, Student_Name, Class, Sec, Marks)
b. Ask for a student name and update their Marks
c. Search for a student record using USN
d. Delete records of students who have scored less than 13
```python
import pickle

students = {}

while True:
    print("1. Insert student record")
    print("2. Update student marks")
    print("3. Search student record")
    print("4. Delete student records with less than 13 marks")
    print("5. Exit")
    choice = int(input("Enter your choice: "))

    if choice == 1:
        usn = input("Enter USN: ")
        student_name = input("Enter Student Name: ")
        class_name = input("Enter Class: ")
        sec = input("Enter Section: ")
        marks = float(input("Enter Marks: "))
        students[usn] = {"Student_Name": student_name, "Class": class_name, "Sec": sec, "Marks": marks}
        with open("student_data.dat", "wb") as file:
            pickle.dump(students, file)
    elif choice == 2:
        usn = input("Enter USN to update marks: ")
        if usn in students:
            new_marks = float(input("Enter new marks: "))
            students[usn]["Marks"] = new_marks
            with open("student_data.dat", "wb") as file:
                pickle.dump(students, file)
        else:
            print("Student not found.")
    elif choice == 3:
        usn = input("Enter USN to search: ")
        if usn in students:
            print("Student Details:", students[usn])
        else:
            print("Student not found.")
    elif choice == 4:
        students = {usn: student for usn, student in students.items() if student["Marks"] >= 13}
        with open("student_data.dat", "wb") as file:
            pickle.dump(students, file)
    elif choice == 5:
        break
    else:
        print("Invalid choice")
```
<br>

15. Write a program to create a Binary file and read byte by byte using seek() and tell().
EG:  Print the pointer position before and after reading all bytes from your file, go to beginning of the file using seek(), Now read 5 bytes from the file and print the pointer position, read the remaining bytes and print the pointer position.
```python
with open("binary_data.dat", "rb") as file:
    print("Initial Pointer Position:", file.tell())
    
    while True:
        byte = file.read(1)
        if not byte:
            break
        
    print("Final Pointer Position:", file.tell())
    
    file.seek(0)
    print("Pointer Position after seeking to the beginning:", file.tell())
    
    five_bytes = file.read(5)
    print("Pointer Position after reading 5 bytes:", file.tell())
```
<br>

16. Write a program to compute the Total salary of the employee and also calculate the size of the binary file named “empfile.dat”. The file consists of the following fields: employee number, employee name, basic salary, allowance. (HINT: Total salary = basic+allowance)
```python
employees = [
    [1, "Ayaan", 5000, 1000],
    [2, "Jamil", 6000, 1200],
    [3, "Thalapathy Vijay", 4500, 800]
]

with open("empfile.dat", "wb") as file:
    for emp in employees:
        emp_line = ",".join(map(str, emp)) + "\n"
        file.write(emp_line)

file_size = 0
with open("empfile.dat", "rb") as file:
    for line in file:
        file_size += len(line)

print("Total File Size:", file_size, "bytes")
```
<br>

17. Write a program to read User_Id and Password for a CSV file, count the number of records and search for a particular record based on User_Id.
```python
import csv

user_id = input("Enter User ID: ")
password = input("Enter Password: ")

with open("user_accounts.csv", "r") as file:
    csv_reader = csv.reader(file)
    record_count = 0
    for row in csv_reader:
        if row[0] == user_id:
            print("User ID found.")
            record_count += 1
            break
    print("Number of records:", record_count)
```
<br>

18. Create a CSV file “groceries” to store information of different items existing in a shop. The information is to be stored w.r.t each item code, name, price, qty. Write a program to accept the data from user and store it permanently in CSV file.
```python
import csv

groceries = []

while True:
    item_code = input("Enter item code: ")
    if not item_code:
        break
    item_name = input("Enter item name: ")
    price = float(input("Enter price: "))
    qty = int(input("Enter quantity: "))
    groceries.append([item_code, item_name, price, qty])

with open("groceries.csv", "w") as file:
    csv_writer = csv.writer(file)
    csv_writer.writerow(["Item Code", "Item Name", "Price", "Quantity"])
    csv_writer.writerows(groceries)
```
<br>

20. Coach Abhishek stores the races and participants in a dictionary. Write a menu based python program, with separate user defined functions to perform the following operations:
a. Push the names of the participants of the dictionary onto a stack, where the distance is more than 100.
b. Pop and display the content of the stack.
```python
participants = []

while True:
    print("1. Push participant")
    print("2. Pop participant")
    print("3. Exit")
    choice = int(input("Enter your choice: "))

    if choice == 1:
        name = input("Enter participant name: ")
        distance = int(input("Enter distance: "))
        if distance > 100:
            participants.append([name, distance])
    elif choice == 2:
        if participants:
            popped_participant = participants.pop()
            print(f"Popped {popped_participant[0]} with distance {popped_participant[1]}")
            print(participants)
        else:
            print("No participants to pop.")
    elif choice == 3:
        break
    else:
        print("Invalid choice")
```
<br>

20. Write a Menu based program to add, delete and display the record of hostel using list as stack Data Structure in Python. Record of Hostel Contains the following fields: Hostel Number, Total Students and Total Rooms.
```python
hostels = []

def push_hostel():
    hostel_number = input("Enter Hostel Number: ")
    total_students = int(input("Enter Total Students: "))
    total_rooms = int(input("Enter Total Rooms: "))
    hostels.append([hostel_number, total_students, total_rooms])
    print("Hostel record pushed.")

def pop_hostel():
    if hostels:
        popped_hostel = hostels.pop()
        print(f"Popped Hostel - Hostel Number: {popped_hostel[0]}, Total Students: {popped_hostel[1]}, Total Rooms: {popped_hostel[2]}")
    else:
        print("No hostels to pop.")

def display_hostels():
    print("Hostel Records:")
    for hostel in hostels:
        print(f"Hostel Number: {hostel[0]}, Total Students: {hostel[1]}, Total Rooms: {hostel[2]}")

while True:
    print("1. Push Hostel Record")
    print("2. Pop Hostel Record")
    print("3. Display Hostel Records")
    print("4. Exit")
    choice = int(input("Enter your choice: "))

    if choice == 1:
        push_hostel()
    elif choice == 2:
        pop_hostel()
    elif choice == 3:
        display_hostels()
    elif choice == 4:
        break
    else:
        print("Invalid choice")
```
<br>

21. Write a Menu based program to push, pop and display the record of phone directory using list as stack Data Structure in Python. Record of phone directory contains the following fields: Pin code of the city and Name of the city.
```python
phone_directory = []

def push_record():
    pin_code = input("Enter Pin Code: ")
    city_name = input("Enter City Name: ")
    phone_directory.append([pin_code, city_name])
    print("Phone directory record pushed.")

def pop_record():
    if phone_directory:
        popped_record = phone_directory.pop()
        print(f"Popped Record - Pin Code: {popped_record[0]}, City Name: {popped_record[1]}")
    else:
        print("No records to pop.")

def display_records():
    print("Phone Directory Records:")
    for record in phone_directory:
        print(f"Pin Code: {record[0]}, City Name: {record[1]}")

while True:
    print("1. Push Phone Directory Record")
    print("2. Pop Phone Directory Record")
    print("3. Display Phone Directory Records")
    print("4. Exit")
    choice = int(input("Enter your choice: "))

    if choice == 1:
        push_record()
    elif choice == 2:
        pop_record()
    elif choice == 3:
        display_records()
    elif choice == 4:
        break
    else:
        print("Invalid choice")
```

(if u r copying code then change some variables)
