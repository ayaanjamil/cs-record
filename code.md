22. Create a dictionary with Roll No, Name and Marks of n students in a class and display the names of students who have scored marks above 75.

```python
myDict = {}
n = int(input("Enter number of students - "))

for i in range(n):
    name = input("Enter name - ")
    roll = int(input(f"Enter {name}'s roll no. - "))
    marks = int(input(f"Enter {name}'s marks - "))
    myDict[name] = [roll, marks]
    print()

print("The students who got above 75 marks are:")
for i in myDict:
    if myDict[i][1] > 75:
        print(i)
```

Output

```
Enter number of students - 3
Enter name - Raju
Enter Raju's roll no. - 22
Enter Raju's marks - 78

Enter name - Kaju
Enter Kaju's roll no. - 18
Enter Kaju's marks - 69

Enter name - Baju
Enter Baju's roll no. - 6
Enter Baju's marks - 85

The students who got above 75 marks are:
Raju
Baju
```





23. Write a python program to input 'n' Names and Phone Number to store it in a dictionary and print the phone number of a particular name.

```python
myDict = {}
n = int(input("Enter number of people - "))

for i in range(n):
    name = input("Enter name - ")
    phone = int(input(f"Enter {name}'s phone no. - "))
    myDict[name] = phone
    print()

who = input("Whose number do you want to see? - ")
print(myDict[who])
```

Output

```
Enter number of people - 2
Enter name - Drake
Enter Drake's phone no. - 9876543210

Enter name - J Cole
Enter J Cole's phone no. - 1234567890

Whose number do you want to see? - J Cole
1234567890
```

24. Write a python program to input names of 'n' employees and salary details like Basic pay, HRA, DA, CA. Calculate total salary of each employee and display the same using dictionary.
    
    ```python
    myDict = {}
    n = int(input("Enter number of employees - "))
    
    for i in range(n):
        name = input("Enter name - ")
        bp = int(input(f"Enter {name}'s basic pay - "))
        hra = int(input(f"Enter {name}'s HRA - "))
        da = int(input(f"Enter {name}'s DA - "))
        ca = int(input(f"Enter {name}'s CA - "))
        myDict[name] = [bp, hra, da, ca]
        print()
    
    print("Total salaries are:")
    
    for i in myDict:
        print(i, ' - ', sum(myDict[i]))
    ```

Output

```
Enter number of employees - 2
Enter name - Raju
Enter Raju's basic pay - 10000
Enter Raju's HRA - 2000
Enter Raju's DA - 1000
Enter Raju's CA - 800

Enter name - Kaju
Enter Kaju's basic pay - 12000
Enter Kaju's HRA - 2300
Enter Kaju's DA - 1200
Enter Kaju's CA - 1000

Total salaries are:
Raju  -  13800
Kaju  -  16500
```

25. Write a python program to input names of 'n' Countries and their Capital and Currency, store it in a dictionary and display in tabular form. Also search and display Currency for a particular Country.
    
    ```python
    myDict = {}
    n = int(input("Enter number of countries - "))
    
    for i in range(n):
        name = input("Enter name - ")
        capital = input("Enter capital - ")
        currency = input("Enter currency - ")
        myDict[name] = [capital, currency]
        print()
    
    print("    NAME    CAPITAL    CURRENCY")
    for i in myDict:
        print(f"{i}    {myDict[i][0]}    {myDict[i][1]}")
    
    print()
    
    search = input("Which currency do you want to search? - ")
    for i in myDict:
        if myDict[i][1] == search:
            print(i)
    ```

Output

```

```


