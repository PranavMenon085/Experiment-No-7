Experiment No. 7

Name: Pranav Menon

PRN No.: 25070123085

Batch: ENTC - B1

Aim: To study while loop in Python and understand iterative structures, loop control statements, and their practical applications.

THEORY:

1) Introduction to while Loop

The while loop in Python is a control flow statement that allows repeated execution of a block of code as long as a specified condition remains True. It is used when the number of iterations is not known beforehand and depends on a dynamic condition evaluated at runtime. The loop checks the condition before each iteration and exits when the condition becomes False.

Key Characteristics:
• Condition-Based – Executes as long as the condition evaluates to True
• Pre-Test Loop – Condition is checked before the loop body executes
• Dynamic Iteration – Number of repetitions depends on runtime values
• Infinite Loop Risk – Must ensure the condition eventually becomes False
• Supports break/continue – Loop flow can be altered using control statements

2) Syntax of while Loop

The while loop uses a simple structure where the condition is evaluated and if True, the indented block executes. The process repeats until the condition becomes False.

Syntax:
while condition:
    statement(s)

Example:
i = 1
while i <= 5:
    print(i)
    i += 1
Output: 1 2 3 4 5

3) The break Statement

The break statement is used to terminate a loop immediately, regardless of the loop condition. When break is encountered inside a while loop, the loop exits and program execution continues with the next statement after the loop. It is commonly used to exit a loop when a specific condition is met.

Syntax:
while condition:
    if some_condition:
        break
    statement(s)

Example:
i = 0
while i < 10:
    i += 1
    if i == 5:
        break
    print(i)
Output: 1 2 3 4

4) The continue Statement

The continue statement skips the remaining statements in the current iteration and jumps back to the loop condition check. It is used to skip specific iterations without terminating the entire loop, allowing selective execution of the loop body.

Syntax:
while condition:
    if some_condition:
        continue
    statement(s)

Example:
i = 0
while i < 10:
    i += 1
    if i % 2 == 0:
        continue
    print(i)
Output: 1 3 5 7 9

5) The while-else Statement

Python allows an optional else clause with the while loop. The else block executes when the loop condition becomes False (i.e., when the loop ends normally). If the loop is terminated by a break statement, the else block is skipped.

Syntax:
while condition:
    statement(s)
else:
    statement(s)

Example:
nums = [10, 20, 30]
key = 50
i = 0
while i < len(nums):
    if nums[i] == key:
        print("Found")
        break
    i += 1
else:
    print("Not found")
Output: Not found

6) Nested while Loops

A while loop can be placed inside another while loop. The inner loop executes completely for each iteration of the outer loop. Nested loops are useful for working with multi-dimensional data structures and generating patterns.

Syntax:
while outer_condition:
    while inner_condition:
        statement(s)

Example:
i = 1
while i <= 3:
    j = 1
    while j <= 3:
        print(i * j, end=" ")
        j += 1
    print()
    i += 1

7) To print numbers from 1 to 5 using while loop

This program prints numbers from 1 to 5 sequentially using a while loop with a hardcoded upper limit. The counter variable i starts at 1 and is incremented after each print until the condition i<=5 becomes False.

Logic: Initialize i=1, while i<=5 print i and increment i by 1

Syntax:
i = 1
while i <= 5:
    print(i)
    i += 1

Output: 1 2 3 4 5

8) To print numbers from 1 to 10 using while loop

This program prints numbers from 1 to 10 sequentially using a while loop with a hardcoded upper limit. It extends the previous program by changing the loop condition to i<=10, demonstrating how the same while loop structure scales to different ranges.

Logic: Initialize i=1, while i<=10 print i and increment i by 1

Syntax:
i = 1
while i <= 10:
    print(i)
    i += 1

Output: 1 2 3 4 5 6 7 8 9 10

9) To print numbers up to a given limit using while loop

This program prints numbers sequentially from 1 up to a user-specified limit using a while loop. The counter variable is incremented in each iteration until the condition becomes False.

Logic: Initialize i=1, while i<=n print i and increment i by 1

Syntax:
n = int(input("Enter the number of terms : "))
i = 1
while i <= n:
    print(i)
    i = i + 1

10) To calculate the factorial of a given number

This program computes the factorial of a positive integer using a while loop. It multiplies successive integers from 1 to n. Input validation is performed to handle negative numbers.

Logic: If n>0, initialize fact=1, multiply fact by each i from 1 to n; else display invalid message

Syntax:
n = int(input("Enter the number : "))
fact = 1
i = 1
if(n > 0):
    while i <= n:
        fact = fact * i
        i += 1
    print("The factorial of the number is : ", fact)
else:
    print("Invalid!Please try again")

11) To display Fibonacci Series up to n terms

This program generates the Fibonacci series for a given number of terms. It uses two variables to track the previous two numbers, updating them in each iteration to produce the next term.

Logic: Initialize a=0, b=1; in each iteration print a, compute next term c=a+b, shift a=b, b=c

Syntax:
n = int(input("Enter the number of terms : "))
i = 1
a = 0
b = 1
while i <= n:
    print(a, end=" ")
    c = a + b
    a = b
    b = c
    i += 1

12) To display Fibonacci Series up to a given limit

This program prints all Fibonacci numbers up to a specified limit value. Instead of counting terms, it continues as long as the current Fibonacci number does not exceed the limit.

Logic: Initialize a=0, b=1; while a<=limit print a and compute next term

Syntax:
limit = int(input("Enter the limit of the series : "))
a = 0
b = 1
while a <= limit:
    print(a, end=" ")
    c = a + b
    a = b
    b = c

13) To reverse a number using while loop

This program reverses the digits of a given integer using repeated modulo and integer division operations. The last digit is extracted using modulo 10, appended to the reversed number, and the original number is reduced by floor division.

Logic: Extract last digit using n%10, build reversed number as rev*10+d, remove last digit using n//10

Syntax:
n = int(input("Enter the number : "))
rev = 0
while n > 0:
    d = n % 10
    rev = (rev * 10) + d
    n //= 10
print("The reverse of the number is :", rev)

14) To check if a number is palindrome or not

This program checks whether a number reads the same forwards and backwards. It reverses the digits using the same logic as number reversal, then compares the reversed number with the original.

Logic: Store original in temp, reverse n, if rev==temp then palindrome else not palindrome

Syntax:
n = int(input("Enter the number : "))
temp = n
rev = 0
while n > 0:
    d = n % 10
    rev = (rev * 10) + d
    n //= 10
if(rev == temp):
    print("The number is a palindrome")
else:
    print("The number is not a palindrome")

15) To check if a string is palindrome or not

This program checks whether a string is a palindrome using two approaches: the two-pointer technique with a while loop, and Python's slicing operator. A palindrome reads the same forwards and backwards.

Logic (Method 1): Use i and j pointers from both ends; compare characters while i<j; if any mismatch set is_palindrome=False and break
Logic (Method 2): Reverse string using slicing str[::-1] and compare with original

Syntax (Method 1):
s = "madam"
i, j = 0, len(s) - 1
is_palindrome = True
while i < j:
    if s[i] != s[j]:
        is_palindrome = False
        break
    i += 1
    j -= 1

Syntax (Method 2):
str = input("Enter a string: ")
rev = str[: : -1]
if str == rev:
    print("Palindrome")
else:
    print("Not a Palindrome")

16) To calculate the number of digits in a number

This program counts the total number of digits in a given integer by repeatedly dividing it by 10 and incrementing a counter until the number becomes 0.

Logic: Initialize count=0; while num>0, increment count and floor divide num by 10

Syntax:
num = int(input("Enter the number : "))
count = 0
while num > 0:
    count += 1
    num = num // 10
print("Number of digits are : ", count)

17) To search for an element from a list

This program performs a linear search on a list to find a user-specified element. It traverses the list using a while loop and prints the index if found. The while-else construct handles the case when the element is absent.

Logic: Traverse list with index i; if nums[i]==key print index and break; if loop completes without break, else prints "not found"

Syntax:
nums = [10, 20, 30, 40, 50]
key = int(input("Enter the element to be searched : "))
i = 0
while i < len(nums):
    if nums[i] == key:
        print("Element found at Index ", i)
        break
    i = i + 1
else:
    print("Element not found")

18) To print odd numbers using while loop

This program prints all odd numbers up to a given limit using two different approaches: starting from 1 and incrementing by 2, and using the continue statement to skip even numbers.

Logic (Method 1): Start i=1; while i<=num and i%2!=0, print i and increment by 2
Logic (Method 2): Start i=0; increment i; if i%2==0 continue; else print i

Syntax (Method 1):
num = int(input("Enter the number : "))
i = 1
while i <= num and i % 2 != 0:
    print(i)
    i += 2

Syntax (Method 2):
i = 0
while i < 10:
    i += 1
    if i % 2 == 0:
        continue
    print(i)

ALGORITHMS:

Algorithm 1: Print Numbers from 1 to 5 (Hardcoded Limit)

Step 1: Start

Begin the process of printing numbers sequentially from 1 to 5

Step 2: Initialize counter variable

Command: i = 1
Function: Variable assignment
Source: Built-in Python operation (no import required)

Step 3: Check loop condition

Command: while i <= 5:
Function: <= - Less than or equal to comparison operator
Source: Built-in Python operator (no import required)

Step 4: Print current value of i

Command: print(i)
Function: print() - Built-in function for console output
Source: Built-in Python function (no import required)

Step 5: Increment counter

Command: i += 1
Function: += - Augmented addition assignment operator
Source: Built-in Python operator (no import required)

Step 6: Return to Step 3 and repeat until condition is False

Step 7: Stop

End the algorithm

Algorithm 2: Print Numbers from 1 to 10 (Hardcoded Limit)

Step 1: Start

Begin the process of printing numbers sequentially from 1 to 10

Step 2: Initialize counter variable

Command: i = 1
Function: Variable assignment
Source: Built-in Python operation (no import required)

Step 3: Check loop condition

Command: while i <= 10:
Function: <= - Less than or equal to comparison operator
Source: Built-in Python operator (no import required)

Step 4: Print current value of i

Command: print(i)
Function: print() - Built-in output function
Source: Built-in Python function (no import required)

Step 5: Increment counter

Command: i += 1
Function: += - Augmented addition assignment operator
Source: Built-in Python operator (no import required)

Step 6: Return to Step 3 and repeat until condition is False

Step 7: Stop

End the algorithm

Algorithm 3: Print Numbers up to User-Input Value

Step 1: Start

Begin the process of printing numbers up to a user-specified limit

Step 2: Accept input from user

Command: n = int(input("Enter the number of terms : "))
Function: input() - Built-in function for accepting user input as string
Function: int() - Built-in function to convert string to integer
Source: Built-in Python functions (no import required)

Step 3: Initialize counter variable

Command: i = 1
Function: Variable assignment
Source: Built-in Python operation (no import required)

Step 4: Check loop condition

Command: while i <= n:
Function: <= - Less than or equal to comparison operator
Source: Built-in Python operator (no import required)

Step 5: Print current value of i

Command: print(i)
Function: print() - Built-in output function
Source: Built-in Python function (no import required)

Step 6: Increment counter

Command: i = i + 1
Function: + - Addition operator
Source: Built-in Python operator (no import required)

Step 7: Return to Step 4 and repeat until condition is False

Step 8: Stop

End the algorithm

Algorithm 4: Factorial of a Given Number

Step 1: Start

Begin factorial computation process

Step 2: Accept integer input from user

Command: n = int(input("Enter the number : "))
Function: input() - Built-in function for accepting user input
Function: int() - Built-in function to convert string to integer
Source: Built-in Python functions (no import required)

Step 3: Initialize factorial and counter variables

Command: fact = 1
Command: i = 1
Function: Variable assignment
Source: Built-in Python operation (no import required)

Step 4: Validate that input is positive

Command: if(n > 0):
Function: > - Greater than comparison operator
Source: Built-in Python operator (no import required)

Step 5: Check loop condition

Command: while i <= n:
Function: <= - Less than or equal to comparison operator
Source: Built-in Python operator (no import required)

Step 6: Multiply fact by current counter value

Command: fact = fact * i
Function: * - Multiplication operator
Source: Built-in Python operator (no import required)

Step 7: Increment counter

Command: i += 1
Function: += - Augmented addition assignment operator
Source: Built-in Python operator (no import required)

Step 8: Return to Step 5 and repeat until i > n

Step 9: Display factorial result

Command: print("The factorial of the number is : ", fact)
Function: print() - Built-in function for console output
Source: Built-in Python function (no import required)

Step 10: Handle invalid (non-positive) input

Command: else:
Command: print("Invalid!Please try again")
Function: else - Default case keyword
Function: print() - Built-in output function
Source: Built-in Python features (no import required)

Step 11: Stop

End the algorithm

Algorithm 5: Fibonacci Series up to N Terms

Step 1: Start

Begin Fibonacci series generation

Step 2: Accept number of terms from user

Command: n = int(input("Enter the number of terms : "))
Function: input() - Built-in function for user input
Function: int() - Built-in function for integer conversion
Source: Built-in Python functions (no import required)

Step 3: Initialize variables

Command: i = 1
Command: a = 0
Command: b = 1
Function: Variable assignment
Source: Built-in Python operation (no import required)

Step 4: Check loop condition

Command: while i <= n:
Function: <= - Less than or equal to comparison operator
Source: Built-in Python operator (no import required)

Step 5: Print current Fibonacci number

Command: print(a, end=" ")
Function: print() - Built-in output function
Function: end=" " - Named parameter to suppress newline
Source: Built-in Python function (no import required)

Step 6: Compute next Fibonacci number

Command: c = a + b
Function: + - Addition operator
Source: Built-in Python operator (no import required)

Step 7: Shift variables for next iteration

Command: a = b
Command: b = c
Function: Variable assignment
Source: Built-in Python operation (no import required)

Step 8: Increment term counter

Command: i += 1
Function: += - Augmented addition assignment operator
Source: Built-in Python operator (no import required)

Step 9: Return to Step 4 and repeat until i > n

Step 10: Stop

End the algorithm

Algorithm 6: Fibonacci Series up to a Given Limit

Step 1: Start

Begin limit-based Fibonacci series generation

Step 2: Accept limit value from user

Command: limit = int(input("Enter the limit of the series : "))
Function: input() - Built-in function for user input
Function: int() - Built-in function for integer conversion
Source: Built-in Python functions (no import required)

Step 3: Initialize variables

Command: a = 0
Command: b = 1
Function: Variable assignment
Source: Built-in Python operation (no import required)

Step 4: Check loop condition

Command: while a <= limit:
Function: <= - Less than or equal to comparison operator
Source: Built-in Python operator (no import required)

Step 5: Print current Fibonacci number

Command: print(a, end=" ")
Function: print() - Built-in output function
Source: Built-in Python function (no import required)

Step 6: Compute next Fibonacci number

Command: c = a + b
Function: + - Addition operator
Source: Built-in Python operator (no import required)

Step 7: Shift variables

Command: a = b
Command: b = c
Function: Variable assignment
Source: Built-in Python operation (no import required)

Step 8: Return to Step 4 and repeat until a > limit

Step 9: Stop

End the algorithm

Algorithm 7: Reverse a Number

Step 1: Start

Begin number reversal process

Step 2: Accept integer input from user

Command: n = int(input("Enter the number : "))
Function: input() - Built-in function for user input
Function: int() - Built-in function for integer conversion
Source: Built-in Python functions (no import required)

Step 3: Initialize reversed number variable

Command: rev = 0
Function: Variable assignment
Source: Built-in Python operation (no import required)

Step 4: Check loop condition

Command: while n > 0:
Function: > - Greater than comparison operator
Source: Built-in Python operator (no import required)

Step 5: Extract last digit using modulo

Command: d = n % 10
Function: % - Modulo operator (returns remainder of division)
Source: Built-in Python operator (no import required)

Step 6: Append digit to reversed number

Command: rev = (rev * 10) + d
Function: * - Multiplication operator
Function: + - Addition operator
Source: Built-in Python operators (no import required)

Step 7: Remove last digit from original number

Command: n //= 10
Function: //= - Augmented floor division assignment operator
Source: Built-in Python operator (no import required)

Step 8: Return to Step 4 and repeat until n becomes 0

Step 9: Display reversed number

Command: print("The reverse of the number is :", rev)
Function: print() - Built-in output function
Source: Built-in Python function (no import required)

Step 10: Stop

End the algorithm

Algorithm 8: Check if a Number is Palindrome

Step 1: Start

Begin palindrome check process

Step 2: Accept integer input from user

Command: n = int(input("Enter the number : "))
Function: input() - Built-in function for user input
Function: int() - Built-in function for integer conversion
Source: Built-in Python functions (no import required)

Step 3: Store original number in temporary variable

Command: temp = n
Function: Variable assignment
Source: Built-in Python operation (no import required)

Step 4: Initialize reversed number variable

Command: rev = 0
Function: Variable assignment
Source: Built-in Python operation (no import required)

Step 5: Check loop condition

Command: while n > 0:
Function: > - Greater than comparison operator
Source: Built-in Python operator (no import required)

Step 6: Extract last digit and build reversed number

Command: d = n % 10
Command: rev = (rev * 10) + d
Function: % - Modulo operator
Function: * - Multiplication operator
Function: + - Addition operator
Source: Built-in Python operators (no import required)

Step 7: Remove last digit from number

Command: n //= 10
Function: //= - Augmented floor division assignment operator
Source: Built-in Python operator (no import required)

Step 8: Return to Step 5 and repeat until n becomes 0

Step 9: Compare reversed number with original

Command: if(rev == temp):
Function: == - Equality comparison operator
Source: Built-in Python operator (no import required)

Step 10: Display palindrome message

Command: print("The number is a palindrome")
Function: print() - Built-in output function
Source: Built-in Python function (no import required)

Step 11: Handle non-palindrome case

Command: else:
Command: print("The number is not a palindrome")
Function: else - Default case keyword
Function: print() - Built-in output function
Source: Built-in Python features (no import required)

Step 12: Stop

End the algorithm

Algorithm 9A: Check if a String is Palindrome (Method 1 - Two Pointer)

Step 1: Start

Begin string palindrome check using two-pointer technique

Step 2: Define string variable

Command: s = "madam"
Function: String literal assignment
Source: Built-in Python data type (no import required)

Step 3: Initialize pointer variables

Command: i, j = 0, len(s) - 1
Function: len() - Built-in function to get length of string
Function: - - Subtraction operator
Source: Built-in Python functions and operators (no import required)

Step 4: Initialize palindrome flag

Command: is_palindrome = True
Function: Variable assignment with boolean value
Source: Built-in Python operation (no import required)

Step 5: Check loop condition

Command: while i < j:
Function: < - Less than comparison operator
Source: Built-in Python operator (no import required)

Step 6: Compare characters at both pointers

Command: if s[i] != s[j]:
Function: != - Not equal comparison operator
Function: [] - Indexing operator
Source: Built-in Python operators (no import required)

Step 7: Set flag to False and exit loop if mismatch found

Command: is_palindrome = False
Command: break
Function: break - Loop termination keyword
Source: Built-in Python keyword (no import required)

Step 8: Move pointers inward

Command: i += 1
Command: j -= 1
Function: += - Augmented addition assignment operator
Function: -= - Augmented subtraction assignment operator
Source: Built-in Python operators (no import required)

Step 9: Return to Step 5 and repeat until i >= j

Step 10: Check palindrome flag and display result

Command: if is_palindrome:
Command: print("Palindrome")
Command: else:
Command: print("Not a palindrome")
Function: print() - Built-in output function
Source: Built-in Python function (no import required)

Step 11: Stop

End the algorithm

Algorithm 9B: Check if a String is Palindrome (Method 2 - Slicing)

Step 1: Start

Begin string palindrome check using slicing

Step 2: Accept string input from user

Command: str = input("Enter a string: ")
Function: input() - Built-in function for user input
Source: Built-in Python function (no import required)

Step 3: Reverse string using slicing

Command: rev = str[: : -1]
Function: [] - Slice operator with step -1 to reverse the string
Source: Built-in Python slicing operation (no import required)

Step 4: Compare original string with reversed string

Command: if str == rev:
Function: == - Equality comparison operator
Source: Built-in Python operator (no import required)

Step 5: Display palindrome message

Command: print("Palindrome")
Function: print() - Built-in output function
Source: Built-in Python function (no import required)

Step 6: Handle non-palindrome case

Command: else:
Command: print("Not a Palindrome")
Function: else - Default case keyword
Function: print() - Built-in output function
Source: Built-in Python features (no import required)

Step 7: Stop

End the algorithm

Algorithm 10: Count Number of Digits in a Number

Step 1: Start

Begin digit counting process

Step 2: Accept integer input from user

Command: num = int(input("Enter the number : "))
Function: input() - Built-in function for user input
Function: int() - Built-in function for integer conversion
Source: Built-in Python functions (no import required)

Step 3: Initialize digit count variable

Command: count = 0
Function: Variable assignment
Source: Built-in Python operation (no import required)

Step 4: Check loop condition

Command: while num > 0:
Function: > - Greater than comparison operator
Source: Built-in Python operator (no import required)

Step 5: Increment count

Command: count += 1
Function: += - Augmented addition assignment operator
Source: Built-in Python operator (no import required)

Step 6: Remove last digit using floor division

Command: num = num // 10
Function: // - Floor division operator
Source: Built-in Python operator (no import required)

Step 7: Return to Step 4 and repeat until num becomes 0

Step 8: Display total digit count

Command: print("Number of digits are : ", count)
Function: print() - Built-in output function
Source: Built-in Python function (no import required)

Step 9: Stop

End the algorithm

Algorithm 11: Linear Search in a List

Step 1: Start

Begin linear search process

Step 2: Define the list

Command: nums = [10, 20, 30, 40, 50]
Function: [] - List literal creation
Source: Built-in Python data structure (no import required)

Step 3: Accept search key from user

Command: key = int(input("Enter the element to be searched : "))
Function: input() - Built-in function for user input
Function: int() - Built-in function for integer conversion
Source: Built-in Python functions (no import required)

Step 4: Initialize index variable

Command: i = 0
Function: Variable assignment
Source: Built-in Python operation (no import required)

Step 5: Check loop condition

Command: while i < len(nums):
Function: < - Less than comparison operator
Function: len() - Built-in function to get list length
Source: Built-in Python functions and operators (no import required)

Step 6: Compare current element with search key

Command: if nums[i] == key:
Function: == - Equality comparison operator
Function: [] - Indexing operator
Source: Built-in Python operators (no import required)

Step 7: Display index if element is found and exit loop

Command: print("Element found at Index ", i)
Command: break
Function: print() - Built-in output function
Function: break - Loop termination keyword
Source: Built-in Python function and keyword (no import required)

Step 8: Increment index if element not found at current position

Command: i = i + 1
Function: + - Addition operator
Source: Built-in Python operator (no import required)

Step 9: Return to Step 5 and repeat

Step 10: Handle element not found using else clause

Command: else:
Command: print("Element not found")
Function: else - while-else keyword executed when loop exits without break
Function: print() - Built-in output function
Source: Built-in Python keyword and function (no import required)

Step 11: Stop

End the algorithm

Algorithm 12A: Print Odd Numbers (Method 1 - Increment by 2)

Step 1: Start

Begin odd number printing process

Step 2: Accept upper limit from user

Command: num = int(input("Enter the number : "))
Function: input() - Built-in function for user input
Function: int() - Built-in function for integer conversion
Source: Built-in Python functions (no import required)

Step 3: Initialize counter to first odd number

Command: i = 1
Function: Variable assignment
Source: Built-in Python operation (no import required)

Step 4: Check loop condition

Command: while i <= num and i % 2 != 0:
Function: <= - Less than or equal to comparison operator
Function: % - Modulo operator
Function: != - Not equal comparison operator
Function: and - Logical AND operator
Source: Built-in Python operators (no import required)

Step 5: Print current odd number

Command: print(i)
Function: print() - Built-in output function
Source: Built-in Python function (no import required)

Step 6: Increment counter by 2 to get next odd number

Command: i += 2
Function: += - Augmented addition assignment operator
Source: Built-in Python operator (no import required)

Step 7: Return to Step 4 and repeat

Step 8: Stop

End the algorithm

Algorithm 12B: Print Odd Numbers (Method 2 - Using continue)

Step 1: Start

Begin odd number printing using continue statement

Step 2: Initialize counter variable

Command: i = 0
Function: Variable assignment
Source: Built-in Python operation (no import required)

Step 3: Check loop condition

Command: while i < 10:
Function: < - Less than comparison operator
Source: Built-in Python operator (no import required)

Step 4: Increment counter

Command: i += 1
Function: += - Augmented addition assignment operator
Source: Built-in Python operator (no import required)

Step 5: Check if current number is even

Command: if i % 2 == 0:
Function: % - Modulo operator
Function: == - Equality comparison operator
Source: Built-in Python operators (no import required)

Step 6: Skip even numbers using continue

Command: continue
Function: continue - Loop control keyword to skip current iteration
Source: Built-in Python keyword (no import required)

Step 7: Print current odd number

Command: print(i)
Function: print() - Built-in output function
Source: Built-in Python function (no import required)

Step 8: Return to Step 3 and repeat

Step 9: Stop

End the algorithm

CONCLUSION

The study of while loop in Python was completed successfully.
