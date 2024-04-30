Counting the sum of numbers in a string
 
Here we will use alphanumeric strings to find the sum of all numbers in that string basically well Count the sum of numbers in a string.Numbers can be added, but strings follow the rule of concatenation a string of alphabets will be concatenated before or after one another but in case of integers, numbers are added to each other to form a new number. Strings can be of many types:-
 
AlphaNumeric
Numeric
Character
 
Python Program to Count the Sum of Numbers in a String
Here we need to count the sum of the number present in the string in the string we can have alphabets as well as some digits so we need to find the sum of the digits. Lets take one example to understand.

Input string :- “4PREP2INSTAA6”
Output :- 12
As in the given string “4PREP2INSTAA6” the number of character that is a number is 4+2+6=12 hence the output is 12.

First we can iterate through the string and check if the character is in range of ‘0’ to ‘9’ if that is the case we will add it to the sum and then print the result.

Using inbuild function we can do the same that is iterate throughout the string and check if the character is a digit or not using isdigit() function.

Algorithm
Step 1:- Start.
Step 2:-  Take user input as alphanumeric string.
Step 3:- Initialize an integer variable with zero value.
Step 4:- Check for numbers available in string.
Step 5:- If numbers are found add number to integer variable by typecasting it to int.
Step 6:- Print sum of the numbers available in string.
Step 7:- End.
Count the sum of numbers in a string
Run
#take user input
String = "Daya123Ben456"
#initialize integer variable
sum1 = 0
for i in String:
    #check if values lies between range of numbers or not
    #according to ascii tale
    if ord(i) >= 48 and ord(i) <= 57:
        #convert it to integer and add
        sum1 = sum1 + int(i)
print('Sum is :' + str(sum1))
Output
Sum is :21
Method 2 (Regex)
Run
# Function to calculate sum of all
# numbers present in a string
# containing alphanumeric characters

import re
def find_sum(str1):
    # Regular Expression that matches
    # digits in between a string
    return sum(map(int, re.findall('\d+', str1)))

# Driver code
# input alphanumeric string
str1 = "12Prep20insta68"

# Function call
print("Sum of all the digits",find_sum(str1))
Output
Sum of all the digits 100
