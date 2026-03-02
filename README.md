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

Algorithm 1: Print Numbers 
Step 1: Start

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
Step 7: Stop

OR 
To print Numbers from 1 to 10 :
- Change the condition to while i<=11
- print(i)
- Increment i (i+=1)

  OR
  To print 'N' Numbers :
  - Input the Number
  - Change the condition to while i<=number
- print(i)
- Increment i (i+=1)
Algorithm 2: Factorial of a Given Number
Step 1: Start

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
Step 9: Display factorial result
   - Command: print("The factorial of the number is : ", fact)
   - Function: print() - Built-in function for console output
   - Source: Built-in Python function (no import required)
Step 10: Handle invalid (non-positive) input
   - Command: else: print("Invalid!Please try again")
   - Function: print() - Built-in function for console output
   - Source: Built-in Python function (no import required)
Step 11: Stop
Algorithm 3: Fibonacci Series up to N Terms
Step 1: Start
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
Step 10: Stop
Algorithm 4: Reverse a Number
Step 1: Start
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
Step 9: Display reversed number
   - Command: print("The reverse of the number is :", rev)
   - Function: print() - Built-in function for console output
   - Source: Built-in Python function (no import required)
Step 10: Stop
Algorithm 5: Check if a Number is Palindrome
Step 1: Start
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
Step 9: Compare reversed number with original
   - Command: if(rev == temp):
   - Function: == - Equality comparison operator
   - Source: Built-in Python operator (no import required)
Step 10: Display result
   - Command: print("The number is a palindrome") / print("The number is not a palindrome")
   - Function: print() - Built-in function for console output
   - Source: Built-in Python function (no import required)
Step 11: Stop
Algorithm 6: Linear Search in a List
Step 1: Start
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
Step 10: Handle element not found using else clause
   - Command: else: print("Element not found")
   - Function: else - while-else keyword; print() - Built-in output function
   - Source: Built-in Python keyword and function (no import required)
Step 11: Stop
Algorithm 7: Print Numbers 1 to 10
Step 1: Start
Step 2: Initialize counter variable
   - Command: i = 1
   - Function: Variable assignment
   - Source: Built-in Python operation (no import required)
Step 3: Check loop condition
   - Command: while i <= 10:
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
Step 7: Stop
Algorithm 8: Print Numbers 1 to N (User Input)
Step 1: Start
Step 2: Accept number of terms from user
   - Command: n = int(input("Enter the number of terms : "))
   - Function: input() - Built-in function for user input; int() - converts string to integer
   - Source: Built-in Python functions (no import required)
Step 3: Initialize counter variable
   - Command: i = 1
   - Function: Variable assignment
   - Source: Built-in Python operation (no import required)
Step 4: Check loop condition
   - Command: while i <= n:
   - Function: <= - Less than or equal to comparison operator
   - Source: Built-in Python operator (no import required)
Step 5: Print current value of i
   - Command: print(i)
   - Function: print() - Built-in function for console output
   - Source: Built-in Python function (no import required)
Step 6: Increment counter
   - Command: i = i + 1
   - Function: + - Addition operator
   - Source: Built-in Python operator (no import required)
Step 8: Stop
Algorithm 9: Fibonacci Series up to a Limit Value
Step 1: Start
Step 2: Accept limit value from user
   - Command: limit = int(input("Enter the limit of the series : "))
   - Function: input() - Built-in function for user input; int() - integer conversion
   - Source: Built-in Python functions (no import required)
Step 3: Initialize first two Fibonacci variables
   - Command: a = 0 ; b = 1
   - Function: Variable assignment
   - Source: Built-in Python operation (no import required)
Step 4: Check loop condition
   - Command: while a <= limit:
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
Step 9: Stop
Algorithm 10: Check if a String is Palindrome (Two-Pointer Method)
Step 1: Start
Step 2: Define the string
   - Command: s = "madam"
   - Function: Variable assignment
   - Source: Built-in Python operation (no import required)
Step 3: Initialize two pointers and palindrome flag
   - Command: i, j = 0, len(s) - 1 ; is_palindrome = True
   - Function: len() - Returns length of string
   - Source: Built-in Python function (no import required)
Step 4: Check loop condition
   - Command: while i < j:
   - Function: < - Less than comparison operator
   - Source: Built-in Python operator (no import required)
Step 5: Compare characters at both pointer positions
   - Command: if s[i] != s[j]:
   - Function: != - Inequality operator; [] - String indexing
   - Source: Built-in Python operators (no import required)
Step 6: If mismatch found, set flag to False and exit loop
   - Command: is_palindrome = False ; break
   - Function: break - Loop termination keyword
   - Source: Built-in Python keyword (no import required)
Step 7: Move pointers inward toward the centre
   - Command: i += 1 ; j -= 1
   - Function: += , -= - Augmented assignment operators
   - Source: Built-in Python operators (no import required)
Step 9: Display result based on flag
   - Command: if is_palindrome: print("Palindrome") else: print("Not a palindrome")
   - Function: print() - Built-in function for console output
   - Source: Built-in Python function (no import required)
Step 10: Stop
Algorithm 11: Check if a String is Palindrome (Slicing Method)
Step 1: Start
Step 2: Accept string input from user
   - Command: str = input("Enter a string: ")
   - Function: input() - Built-in function for user input
   - Source: Built-in Python function (no import required)
Step 3: Reverse the string using slicing
   - Command: rev = str[::-1]
   - Function: [::-1] - String slicing with step -1 to reverse the string
   - Source: Built-in Python slicing operation (no import required)
Step 4: Compare original string with reversed string
   - Command: if str == rev:
   - Function: == - Equality comparison operator
   - Source: Built-in Python operator (no import required)
Step 5: Display result
   - Command: print("Palindrome") / print("Not a Palindrome")
   - Function: print() - Built-in function for console output
   - Source: Built-in Python function (no import required)
Step 6: Stop
Algorithm 12: Count the Number of Digits in a Number
Step 1: Start
Step 2: Accept integer input from user
   - Command: num = int(input("Enter the number : "))
   - Function: input() - Built-in function for user input; int() - integer conversion
   - Source: Built-in Python functions (no import required)
Step 3: Initialize digit counter to zero
   - Command: count = 0
   - Function: Variable assignment
   - Source: Built-in Python operation (no import required)
Step 4: Check loop condition
   - Command: while num > 0:
   - Function: > - Greater than comparison operator
   - Source: Built-in Python operator (no import required)
Step 5: Increment digit counter
   - Command: count += 1
   - Function: += - Augmented addition assignment operator
   - Source: Built-in Python operator (no import required)
Step 6: Remove last digit from number using floor division
   - Command: num = num // 10
   - Function: // - Floor division operator
   - Source: Built-in Python operator (no import required)
Step 8: Display digit count
   - Command: print("Number of digits are : ", count)
   - Function: print() - Built-in function for console output
   - Source: Built-in Python function (no import required)
Step 9: Stop
Algorithm 13: Print Odd Numbers (Method 1 — Condition in While)
Step 1: Start
Step 2: Accept upper limit from user
   - Command: num = int(input("Enter the number : "))
   - Function: input() - Built-in function for user input; int() - integer conversion
   - Source: Built-in Python functions (no import required)
Step 3: Initialize counter to 1 (first odd number)
   - Command: i = 1
   - Function: Variable assignment
   - Source: Built-in Python operation (no import required)
Step 4: Check compound loop condition
   - Command: while i <= num and i % 2 != 0:
   - Function: <= - Less than or equal; % - Modulo; != - Inequality; and - Logical AND
   - Source: Built-in Python operators (no import required)
Step 5: Print current odd number
   - Command: print(i)
   - Function: print() - Built-in function for console output
   - Source: Built-in Python function (no import required)
Step 6: Increment by 2 to jump to next odd number
   - Command: i += 2
   - Function: += - Augmented addition assignment operator
   - Source: Built-in Python operator (no import required)
Step 8: Stop
Algorithm 14: Print Odd Numbers (Method 2 — Using continue)
Step 1: Start
Step 2: Initialize counter to 0
   - Command: i = 0
   - Function: Variable assignment
   - Source: Built-in Python operation (no import required)
Step 3: Check loop condition
   - Command: while i < 10:
   - Function: < - Less than comparison operator
   - Source: Built-in Python operator (no import required)
Step 4: Increment counter
   - Command: i += 1
   - Function: += - Augmented addition assignment operator
   - Source: Built-in Python operator (no import required)
Step 5: Skip even numbers using continue
   - Command: if i % 2 == 0: continue
   - Function: % - Modulo operator; == - Equality; continue - Skip rest of current iteration
   - Source: Built-in Python operators and keyword (no import required)
Step 6: Print current odd number
   - Command: print(i)
   - Function: print() - Built-in function for console output
   - Source: Built-in Python function (no import required)
Step 8: Stop
Conclusion:

The study of while loop in Python was successfully completed.
