# Data Structures and Algorithms

![Static Badge](https://img.shields.io/badge/Made%20By-Younes.A-purple)
![Static Badge](https://img.shields.io/badge/Class-NWT24_Guelma-red)
![Static Badge](https://img.shields.io/badge/Telegram-NWT24-2CA5E0?logo=telegram&logoColor=white&link=https%3A%2F%2Ft.me%2FNWT24)
![GitHub last commit](https://img.shields.io/github/last-commit/unus-all/DSA)


> [!NOTE]
> For those interested in learning more about C, [W3Schools](https://www.w3schools.com/c/index.php) offers an excellent tutorial.


# I. Start Coding
[Code::Blocks](https://www.codeblocks.org/) is a popular integrated development environment (IDE) that allows users to code in
C.

To ensure a seamless experience, it is essential to install the version of [Code::Blocks that
includes the compiler](https://www.fosshub.com/Code-Blocks.html?dwl=codeblocks-20.03mingw-setup.exe).

# II. First Program
The initial program will demonstrate how to output or print information to the console using the
``printf()`` function.

The ``main()`` function serves as the **entry point** for any C program.

```c
#include <stdio.h>

int main(){
    printf("Hello, World!\n");
    return 0;
}
```
-  **Output**
```text
Hello, World!
```

> [!CAUTION]
> Each instruction ends with a semi-colon ;

# A. Variables
A variable is the **name** given to the memory location that **stores** some data.
- In other words, a variable acts as a **label** or **identifier** for a memory location.

## 1. Syntax
> ``variable_type variable_name ;``

or

> ``variable_type variable_name = value ;``

### Variable Types
- ``int`` for integers values, *e.g,* 256 , -1498, ..etc.
- ``float`` for real (floating point) numbers, *e.g,* 3.14, -0.6, ..etc.
- ``char`` for characters, *e.g,* 'A', '!', '1', ..etc.

### Variable Names
- ✔️ Variable names must contain only letters, (``A-Z``, ``a-z``), digits (``0-9``), and underscores (``_``).
- ✔️ Each variable must be identified with a unique name.
- ✔️ Variables should starts with a letter or underscore.
- ❌ Don’t include white-spaces or special characters.
- ❌ Don’t name a variable with a reserved keyword like ``int``.
- ⚠️ Names are **case-sensitive**: ``age``, ``Age`` and ``AGE`` are different variables.
- ⚠️ It’s recommended that the names have a meaning (``age`` instead of ``a``).

### Assignment Operator ``=``
The assignment operator (``=``) stores a certain value in an already declared variable.
- *e.g,* ``x = y + z;`` will assign the value of ``y + z`` **(right side)** to ``x`` **(left side)**.

## 2. Format Specifiers
Format specifiers tell the compiler what type of data the variable is storing. 

We need to use them whether we’re printing formatted output with ``printf()`` or accepting input with ``scanf()``.

- For integers (``int``) we use ``%d``.
- For real numbers (``float``) we use ``%f``.
- For characters (``char``) we use ``%c``.

- **Example:**
```c
#include <stdio.h>

int main(){
    int number = 10;
    float pi = 3.14;
    char character = '#';

    printf("Number is %d, the value of PI is %f, the character is %c", number, pi, character);
    return 0;
}
```
-  **Output**
```text
Number is 10, the value of PI is 3.14, the character is #
```

# B. User Input
To get user input we use the ``scanf()`` function.

The ``scanf()`` function takes two arguments:

- The **format specifier** of the variable (*e.g,* ``%d`` for integers).
- The **memory location (address) of the variable**, here we use the address operator ``&`` *e.g,* ``&myVar``.
- **Example:**
```c
#include <stdio.h>

int main(){
    int birth_year;

    // We show the user a message to properly ask what we need from him.
    printf("Enter your birth year: ");
    // In the address of the birth_year variable, we store what the user will type.
    scanf("%d", &birth_year);
    return 0;
}
```
> [!TIP]
> Comments can be used to explain code, and to make it more readable.
>
> - Single-line comments start with two forward slashes (``//``).
> - Multi-line comments start with ``/*`` and ends with ``*/``.

# C. Operators
## 1. Arithmetic Operators
| Name    | Operator    | Description    | Example    |
|---------------- | --------------- | --------------- | --------------- |
| Addition    | ``+``    | Adds together two values    | ``7 + 3`` (result is 10)|
| Subtraction    | ``-``    | Subtracts one value from another    | ``7 - 3`` (result is 4)|
| Multiplication   | ``*``   | Multiplies two values   | ``7 * 3`` (result is 21)|
| Division   | ``/``   | Divides one value by another   | ``7 / 3`` (result is 2)|
| Modulus   | ``%``   | Returns the division remainder   | ``7 % 3`` (result is 1)|

## 2. Comparison Operators
| Name    | Operator    | Description    | Example    |
|---------------- | --------------- | --------------- | --------------- |
| Equal to    | ``==``    | Returns 1 if the values are equal    | ``7 == 3`` (result is 0)|
| Not equal    | ``!=``    | Returns 1 if the values are not equal    | ``7 != 3`` (result is 1)|
| Greater than   | ``>``   | Returns 1 if the first value is greater than the second value   | ``7 > 3`` (result is 1)|
| Less than   | ``<``   |  	Returns 1 if the first value is less than the second value   | ``7 < 3`` (result is 0)|
| Greater than or equal to   | ``>=``   | Returns 1 if the first value is greater than, or equal to, the second value   | ``7 >= 3`` (result is 1)|
| Less than or equal to   | ``<=``   | Returns 1 if the first value is less than, or equal to, the second value   | ``7 <= 3`` (result is 0)|

## 3. Logical Operators
| Name    | Operator    | Description    | Example    |
|---------------- | --------------- | --------------- | --------------- |
| AND    | ``&&``    | Returns 1 if both statements are true    | ``(7 > 3) && 0`` (result is 0)|
| OR    | ``\|\|``    | Returns 1 if one of the statements is true    | ``(7 > 3) \|\| 0`` (result is 1)|
| NOT   | ``!``   | Reverse the result, returns 0 if the result is 1   | ``!(7 > 3)`` (result is 0)|

# D. Conditional Statements
## 1. ``if`` Statement
The ``if`` in C is the most simple decision-making statement. We use the ``if`` statement to specify a block of code to be executed if a condition is **true**.

```c
if (condition){
    // block of code to be executed if the condition is true..
}
```

- **Example**

```c
#include <stdio.h>

int main(){
    int x = 7, y = 3;

    if (x > y){
        printf("%d is greater than %d", x, y);
    }

    return 0;
}
```
-  **Output**
```text
7 is greater than 3
```

## 2. ``if .. else`` Statement
In the ``if..else`` statement,  if the given condition is **true**, then the code inside the ``if`` block is executed, **otherwise** the code inside the ``else`` block is executed.

```c
if (condition){
    // block of code to be executed if the condition is true..
} else {
    // block of code to be executed if the condition is false..
}
```

- **Example**

```c
#include <stdio.h>

int main(){
    int x = 5, y = 10;

    if (x > y){
        printf("%d is greater than %d", x, y);
    } else {
        printf("%d is less than or equal to %d", x, y);
    }

    return 0;
}
```
-  **Output**
```text
5 is less than or equal to 10
```

## 3. ``switch`` Statement
Instead of writing many ``if..else`` statements, you can use the ``switch`` statement. The ``switch`` statement is much easier to **read** and **write**.
```c
switch (expression) {
  case x: 
    // code block 
    break;
  case y:
    // code block
    break;
  default:
    // code block
}
```

- **Example**

```c
#include <stdio.h>

int main(){
    int month = 1;

    switch (month) {
        case 1: {printf("Jan"); break;}
        case 2: {printf("Feb"); break;}
        case 3: {printf("Mar"); break;}
        // ...
        case 12: {printf("Dec"); break;}
        default: printf("Your input should be a valid month number.");
    }

    return 0;
}
```
-  **Output**
```text
Jan
```

>[!NOTE]
> - When C reaches a ``break`` keyword, it breaks out of the ``switch`` block.
> - The ``default`` statement specifies some code to run if there is no case match (and it is ***optional***).


# E. Loops

Loops in programming are used to repeat a block of code until the specified condition is met.

## 1. ``while``
The ``while`` loop executes a block of code while a specified condition is ``true``.

```c
while (condition) {
  // code block to be executed
}
```

- **Example**

```c
#include <stdio.h>

int main(){
    int i = 1;

    // instead of using 5 printf to display numbers from 1 to 5, we can use loops.
    while (i<=5) {
        printf("%d\n", i);
        i++;
    }

    return 0;
}
```
-  **Output**
```text
1
2
3
4
5
```
>[!NOTE]
> - The loop int the previous example translated to: ***"while the i is less or equal to 5 than keep printing the value of i."***

>[!CAUTION]
> - If we don't increment the counter ``i``, the ``while`` loop will never end (***infinite loop***).
>   
> **SO PLEASE MAKE SURE YOU END THE LOOP AT SOME POINT**.

## 2. ``do..while``
The difference between the ``while`` and ``do...while`` loops lies in the manner of testing the condition. In the ``do...while`` loop, the condition is evaluated at the end of the loop, in contrast to the ``while`` loop.

This difference results in the ``do...while`` loop executing at least **once**, while the ``while`` loop may not. 

```c
do{
  // code block to be executed
}while(condition);
```

- **Example**

```c
#include <stdio.h>

int main(){
    char character;

    // keep asking for a character until the user enters the letter 'q'.
    do{
        printf("Enter a character (q to quit): ");
        scanf(" %c", &character);
    }while(character!='q');

    printf("END");

    return 0;
}
```
-  **Output**
```text
Enter a character (q to quit): a 
Enter a character (q to quit): y 
Enter a character (q to quit): q 
END
```

## 3. ``for``

>[!TIP]
> - When you know exactly how many times you want to loop through a block of code, use the ``for`` loop instead of a ``while`` loop.

```c
 for (expression 1; expression 2; expression 3) {
  // code block to be executed
}

// - expression 1: initialize the counter.
// - expression 2: the condition we test in each iteration.
// - expression 3: update the value of the counter.
```

- **Example**

```c
#include <stdio.h>

int main(){
    int i;

    // printing multiples of 4 less than 20
    for(i=4 ; i<20 ; i=i+4){
        printf("%d\n", i);
    }

    return 0;
}
```
-  **Output**
```text
4
8
12
16
```
