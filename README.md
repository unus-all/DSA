# Data Structures and Algorithms

![Static Badge](https://img.shields.io/badge/Made%20By-Younes.A-purple)
![Static Badge](https://img.shields.io/badge/Class-NWT24_Guelma-red)
![Static Badge](https://img.shields.io/badge/Telegram-NWT24-2CA5E0?logo=telegram&logoColor=white&link=https%3A%2F%2Ft.me%2FNWT24)
![GitHub last commit](https://img.shields.io/github/last-commit/unus-all/DSA)


> [!NOTE]
> For those interested in learning more about C, [W3Schools](https://www.w3schools.com/c/index.php) offers an excellent tutorial.


# Start Coding
[Code::Blocks](https://www.codeblocks.org/) is a popular integrated development environment (IDE) that allows users to code in
C.

To ensure a seamless experience, it is essential to install the version of [Code::Blocks that
includes the compiler](https://www.fosshub.com/Code-Blocks.html?dwl=codeblocks-20.03mingw-setup.exe).

# First Program
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

# Variables
A variable is the **name** given to the memory location that **stores** some data.
- In other words, a variable acts as a **label** or **identifier** for a memory location.

## Syntax
> ``variable_type variable_name ;``

or

> ``variable_type variable_name = value ;``

### Variable Types
- ``int`` for integers values, *e.g,* 256 , -1498, ..etc.
- ``float`` for real (floating point) numbers, *e.g,* 3.14, -0.6, ..etc.
- ``char`` for characters, *e.g,* 'A', '!', '1', ..etc.

### Variable Names
- ✔️ Variable names must contain only letters, (A-Z, a-z), digits (0-9), and underscores ().
- ✔️ Each variable must be identified with a unique name.
- ✔️ Variables should starts with a letter or underscore.
- ❌ Don’t include white-spaces or special characters.
- ❌ Don’t name a variable with a reserved keyword like ``int``.
- ⚠️ Names are **case-sensitive**: ``age``, ``Age`` and ``AGE`` are different variables.
- ⚠️ It’s recommended that the names have a meaning (``age`` instead of ``a``).

### Assignment Operator ``=``
The assignment operator (``=``) stores a certain value in an already declared variable.
- *e.g,* ``x = y + z;`` will assign the value of ``y + z`` **(right side)** to ``x`` **(left side)**.

## Format Specifiers
Format specifiers tell the compiler what type of data the variable is storing. 

We need to use them whether we’re printing formatted output with ``printf()`` or accepting input with ``scanf()``.

- For integers (``int``) we use ``%d``.
- For real numbers (``float``) we use ``%f``.
- For characters (``char``) we use ``%c``.

