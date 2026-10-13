Week 5 Assignment
Description
Assignment Instructions
Assignment: Password Generator & Your Own Module

Put this week's big idea - using modules - to work in two small programs. First you will use Python's built-in modules to make passwords. Then you will make a module of your own and import it.

This assignment will help you practice:

Bringing in a module with import
Using the random, string and math modules
Writing a function with a default value
Creating your own module and importing it into another file

Files to create (use these exact names):

password_generator.py
helpers.py
main.py

GitHub repository name to use (public, exact): plp-python-week5
Assignment Body
Question 1 - Password Generator

Create the file password_generator.py.

At the top of your file, import two modules:
import random
import string

Copy in this function and fill in the one missing line inside the loop:

def make_password(length=8):
    characters = string.ascii_letters + string.digits
    password = ""
    for i in range(length):
        # Add one random character from characters to password
    return password


Hint: random.choice(characters) picks one character. Use += to add it onto the end of password.

Make one password using the default length, and one with a length of 12. Print each password and its length:
p1 = make_password()
p2 = make_password(12)

print("Password:", p1)
print("Length:", len(p1))
print("Password:", p2)
print("Length:", len(p2))


Run the program twice. Your passwords should be different each time.

Your passwords will be random, so they will not match anyone else's. The lengths must be exactly this:


Password: zAi1lJ0z
Length: 8
Password: d04fiFjnrbEK
Length: 12

Required results:

A working password_generator.py that makes an 8-character and a 12-character password.
A screenshot of two runs showing different passwords each time.
Question 2 - Your Own Module

Create two files in the same folder: helpers.py and main.py.

Part 1 - helpers.py

This file holds your functions. Copy it in and fill in the two missing lines:


import math

def tables_needed(people, seats):
    # Return people divided by seats, rounded UP with math.ceil()

def welcome(name):
    # Return "Welcome to PLP, NAME!" using the name

if __name__ == "__main__":
    print(tables_needed(10, 4))


Hint: math.ceil() always rounds up. 10 people at tables of 4 need 3 tables, not 2.5 and not 2.

Part 2 - main.py

This file uses your module. Copy it in exactly:


import helpers

print(helpers.welcome("Amina"))
print(helpers.tables_needed(47, 6))
print(helpers.tables_needed(20, 5))

Part 3 - Run both files

Run main.py. The output must be exactly this:


Welcome to PLP, Amina!
8
4

Then run helpers.py on its own. It should print just:

3

Notice that the 3 does not appear when you run main.py. That is the if __name__ == "__main__": line doing its job.

⚠️ Do not name any of your files math.py, random.py or string.py. Python will import your file instead of the real module, and your program will break.

Required results:

A working helpers.py with both functions filled in.
A working main.py that imports helpers and prints the three lines above.
A screenshot of main.py running, and a screenshot of helpers.py running on its own.