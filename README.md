Experiment No. 7

Name: Pranav Menon

PRN No.: 25070123085

Batch: ENTC - B1

Aim:

To study while loop in Python and understand iterative structures, loop control statements, and their practical applications.

THEORY

1) Introduction to while Loop

A while loop in Python is a control flow statement that repeatedly executes a block of code as long as a specified condition remains True. It is used when the number of iterations is not known beforehand and depends on a condition evaluated at runtime.

Key Characteristics:
• Condition-Based – Executes as long as the condition evaluates to True
• Pre-Test Loop – Condition is checked before the loop body executes
• Dynamic Iteration – Number of repetitions depends on runtime values
• Infinite Loop Risk – Must ensure the condition eventually becomes False
• Supports break/continue – Loop flow can be altered using control statements

Syntax:
while condition:
    statement(s)

Example:
i = 1
while i <= 5:
    print(i)
    i += 1
Output: 1 2 3 4 5

2) The break Statement

Terminates the loop immediately regardless of the condition. Execution continues with the statement after the loop.

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

3) The continue Statement

Skips the remaining statements in the current iteration and jumps back to the condition check. Used to selectively skip iterations without exiting the loop.

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

4) The while-else Statement

Python allows an optional else clause with the while loop. The else block executes when the loop condition becomes False. It is skipped if the loop exits via a break statement.

Syntax:
while condition:
    statement(s)
else:
    statement(s)

Example:
i = 0
while i < len(nums):
    if nums[i] == key:
        print("Found")
        break
    i += 1
else:
    print("Not found")

5) Modulo and Floor Division Operators

Two arithmetic operators used frequently in while loop programs:
- % (Modulo) – Returns the remainder of a division. Used to extract the last digit of a number (n % 10) and to check even/odd (n % 2).
- // (Floor Division) – Divides and discards the remainder. Used to remove the last digit of a number (n //= 10) and to count digits.

Example:
123 % 10   → 3   (last digit)
123 // 10  → 12  (removes last digit)

6) String Slicing for Reversal

Python strings support slicing using the syntax str[start:stop:step]. Using a step of -1 reverses the string without a loop.

Example:
s = "madam"
rev = s[::-1]   # rev = "madam"

7) Palindrome Concept

A palindrome is a sequence (number or string) that reads the same forwards and backwards.
- Number palindrome: Reverse the digits and compare with the original.
- String palindrome: Compare the string with its reverse using slicing or the two-pointer technique.

Example: 121, "madam", "racecar" are palindromes.

8) Linear Search

Linear search traverses a list one element at a time, comparing each element to the target key. The while-else construct in Python is ideal for this — the else block executes only if the loop finishes without hitting a break, signalling the element was not found.

Example: Searching for 20 in [10, 20, 30, 40, 50] → Found at Index 1

ALGORITHMS

Algorithm 1: Print Numbers 1 to 5

Step 1: Start
   - Begin printing numbers from 1 to 5

Step 2: Initialize counter variable
   - Command: i = 1
   - Function: Variable assignment
   - Source: Built-in Python operation (no import required)

Step 3: Check loop condition
   - Command: while i <= 5:
   - Function: <= - Less than or equal to comparison operator
   - Source: Built-in Python operator (no import required)

Step 4: Print current value of i
   - Command: print(i)
   - Function: print() - Built-in function for console output
   - Source: Built-in Python function (no import required)

Step 5: Increment counter
   - Command: i += 1
   - Function: += - Augmented addition assignment operator
   - Source: Built-in Python operator (no import required)

Step 6: Return to Step 3 and repeat until condition is False

Step 7: Stop
   - End the algorithm

Algorithm 2: Factorial of a Given Number

Step 1: Start
   - Begin factorial computation

Step 2: Accept integer input from user
   - Command: n = int(input("Enter the number : "))
   - Function: input() - Built-in function for user input; int() - converts string to integer
   - Source: Built-in Python functions (no import required)

Step 3: Initialize factorial and counter variables
   - Command: fact = 1 ; i = 1
   - Function: Variable assignment
   - Source: Built-in Python operation (no import required)

Step 4: Validate that input is positive
   - Command: if(n > 0):
   - Function: > - Greater than comparison operator
   - Source: Built-in Python operator (no import required)

Step 5: Check loop condition
   - Command: while i <= n:
   - Function: <= - Less than or equal to comparison operator
   - Source: Built-in Python operator (no import required)

Step 6: Multiply fact by current counter value
   - Command: fact = fact * i
   - Function: * - Multiplication operator
   - Source: Built-in Python operator (no import required)

Step 7: Increment counter
   - Command: i += 1
   - Function: += - Augmented addition assignment operator
   - Source: Built-in Python operator (no import required)

Step 8: Return to Step 5 and repeat until i > n

Step 9: Display factorial result
   - Command: print("The factorial of the number is : ", fact)
   - Function: print() - Built-in function for console output
   - Source: Built-in Python function (no import required)

Step 10: Handle invalid (non-positive) input
   - Command: else: print("Invalid!Please try again")
   - Function: print() - Built-in function for console output
   - Source: Built-in Python function (no import required)

Step 11: Stop
   - End the algorithm

Algorithm 3: Fibonacci Series up to N Terms

Step 1: Start
   - Begin Fibonacci series generation

Step 2: Accept number of terms from user
   - Command: n = int(input("Enter the number of terms : "))
   - Function: input() - Built-in function for user input; int() - integer conversion
   - Source: Built-in Python functions (no import required)

Step 3: Initialize variables
   - Command: i = 1 ; a = 0 ; b = 1
   - Function: Variable assignment
   - Source: Built-in Python operation (no import required)

Step 4: Check loop condition
   - Command: while i <= n:
   - Function: <= - Less than or equal to comparison operator
   - Source: Built-in Python operator (no import required)

Step 5: Print current Fibonacci number
   - Command: print(a, end=" ")
   - Function: print() - Built-in output function; end=" " suppresses newline
   - Source: Built-in Python function (no import required)

Step 6: Compute next Fibonacci number
   - Command: c = a + b
   - Function: + - Addition operator
   - Source: Built-in Python operator (no import required)

Step 7: Shift variables for next iteration
   - Command: a = b ; b = c
   - Function: Variable assignment
   - Source: Built-in Python operation (no import required)

Step 8: Increment term counter
   - Command: i += 1
   - Function: += - Augmented addition assignment operator
   - Source: Built-in Python operator (no import required)

Step 9: Return to Step 4 and repeat until i > n

Step 10: Stop
   - End the algorithm

Algorithm 4: Reverse a Number

Step 1: Start
   - Begin number reversal process

Step 2: Accept integer input from user
   - Command: n = int(input("Enter the number : "))
   - Function: input() - Built-in function for user input; int() - integer conversion
   - Source: Built-in Python functions (no import required)

Step 3: Initialize reversed number variable
   - Command: rev = 0
   - Function: Variable assignment
   - Source: Built-in Python operation (no import required)

Step 4: Check loop condition
   - Command: while n > 0:
   - Function: > - Greater than comparison operator
   - Source: Built-in Python operator (no import required)

Step 5: Extract last digit using modulo
   - Command: d = n % 10
   - Function: % - Modulo operator (returns remainder of division)
   - Source: Built-in Python operator (no import required)

Step 6: Append digit to reversed number
   - Command: rev = (rev * 10) + d
   - Function: * - Multiplication operator; + - Addition operator
   - Source: Built-in Python operators (no import required)

Step 7: Remove last digit from original number
   - Command: n //= 10
   - Function: //= - Augmented floor division assignment operator
   - Source: Built-in Python operator (no import required)

Step 8: Return to Step 4 and repeat until n becomes 0

Step 9: Display reversed number
   - Command: print("The reverse of the number is :", rev)
   - Function: print() - Built-in function for console output
   - Source: Built-in Python function (no import required)

Step 10: Stop
   - End the algorithm

Algorithm 5: Check if a Number is Palindrome

Step 1: Start
   - Begin palindrome check process

Step 2: Accept integer input from user
   - Command: n = int(input("Enter the number : "))
   - Function: int() - Built-in function for integer conversion
   - Source: Built-in Python functions (no import required)

Step 3: Store original number in temporary variable
   - Command: temp = n
   - Function: Variable assignment
   - Source: Built-in Python operation (no import required)

Step 4: Initialize reversed number variable
   - Command: rev = 0
   - Function: Variable assignment
   - Source: Built-in Python operation (no import required)

Step 5: Check loop condition
   - Command: while n > 0:
   - Function: > - Greater than comparison operator
   - Source: Built-in Python operator (no import required)

Step 6: Extract last digit and build reversed number
   - Command: d = n % 10 ; rev = (rev * 10) + d
   - Function: % - Modulo operator; * - Multiplication; + - Addition
   - Source: Built-in Python operators (no import required)

Step 7: Remove last digit from number
   - Command: n //= 10
   - Function: //= - Augmented floor division assignment operator
   - Source: Built-in Python operator (no import required)

Step 8: Return to Step 5 and repeat until n becomes 0

Step 9: Compare reversed number with original
   - Command: if(rev == temp):
   - Function: == - Equality comparison operator
   - Source: Built-in Python operator (no import required)

Step 10: Display result
   - Command: print("The number is a palindrome") / print("The number is not a palindrome")
   - Function: print() - Built-in function for console output
   - Source: Built-in Python function (no import required)

Step 11: Stop
   - End the algorithm

Algorithm 6: Linear Search in a List

Step 1: Start
   - Begin linear search process

Step 2: Define the list
   - Command: nums = [10, 20, 30, 40, 50]
   - Function: [] - List literal creation
   - Source: Built-in Python data structure (no import required)

Step 3: Accept search key from user
   - Command: key = int(input("Enter the element to be searched : "))
   - Function: input() - Built-in function for user input; int() - integer conversion
   - Source: Built-in Python functions (no import required)

Step 4: Initialize index variable
   - Command: i = 0
   - Function: Variable assignment
   - Source: Built-in Python operation (no import required)

Step 5: Check loop condition
   - Command: while i < len(nums):
   - Function: < - Less than operator; len() - returns list length
   - Source: Built-in Python functions and operators (no import required)

Step 6: Compare current element with search key
   - Command: if nums[i] == key:
   - Function: == - Equality comparison operator; [] - Indexing operator
   - Source: Built-in Python operators (no import required)

Step 7: Display index if element is found and exit loop
   - Command: print("Element found at Index ", i) ; break
   - Function: print() - Built-in output function; break - loop termination keyword
   - Source: Built-in Python function and keyword (no import required)

Step 8: Increment index
   - Command: i = i + 1
   - Function: + - Addition operator
   - Source: Built-in Python operator (no import required)

Step 9: Return to Step 5 and repeat

Step 10: Handle element not found using else clause
   - Command: else: print("Element not found")
   - Function: else - while-else keyword; print() - Built-in output function
   - Source: Built-in Python keyword and function (no import required)

Step 11: Stop
   - End the algorithm

Conclusion:

The study of while loop in Python was successfully completed. 
