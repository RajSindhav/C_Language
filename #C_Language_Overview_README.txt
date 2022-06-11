**# C_Language_Overview**
-----------------------------------------------------------------------------------------------------------------------------------------------------------------------
**Basic Syntax :**

#include <stdio.h>
_int main() {
  printf("Hello World!");
  return 0;
}_

1. #include <stdio.h> is a header file library that lets us work with input and output functions, such as printf() (used in line 4). Header files add functionality to C-programs.
2. Another thing that always appear in a C program, is main(). This is called a function. Any code inside its curly brackets {} will be executed.
3. printf() is a function used to output/print text to the screen. In our example it will output "Hello World".

**Note that:** Every C statement ends with a semicolon ; 
               The body of int main() could also been written as: int main(){printf("Hello World!");return 0;}
               
 4. return 0 ends the main() function.
 5. Do not forget to add the closing curly bracket } to actually end the main function

-----------------------------------------------------------------------------------------------------------------------------------------------------------------------

**C Output**

1. The printf() function is used to output values/print text
   #include <stdio.h>
   int main() {
     printf("Hello World!");
     return 0;
    }

2. You can add as many printf() functions as you want. However, note that it does not insert a new line at the end of the output
   #include <stdio.h>
   int main() {
     printf("Hello World!");
     printf("I am learning C.");
     return 0;
   }

3. To insert a new line, you can use the \n character.
   #include <stdio.h>
   int main() {
     printf("Hello World!\n");
     printf("I am learning C.");
     return 0;
   }

4. You can also output multiple lines with a single printf() function. However, be aware that this will make the code harder to read
   #include <stdio.h>
   int main() {
     printf("Hello World!\nI am learning C.\nAnd it is awesome!");
     return 0;
   }

5. Two \n characters after each other will create a blank line
   #include <stdio.h>
   int main() {
     printf("Hello World!\n\n");
     printf("I am learning C.");
     return 0;
   }

The newline character (\n) is called an escape sequence, and it forces the cursor to change its position to the beginning of the next line on the screen. This results in a new line

Examples of other valid escape sequences are:

\t - Creates a horizontal tab
#include <stdio.h>
int main() {
  printf("Hello World!\t");
  printf("I am learning C.");
  return 0;
}

\\ - Inserts a backslash character (\)
#include <stdio.h>
int main() {
  printf("Hello World!\\");
  printf("I am learning C.");
  return 0;
}

\" - Inserts a double quote character
#include <stdio.h>
int main() {
  printf("They call him \"Johnny\".");
  return 0;
}
-----------------------------------------------------------------------------------------------------------------------------------------------------------------------

**Comments in C**

Comments can be used to explain code, and to make it more readable. It can also be used to prevent execution when testing alternative code.
Comments can be singled-lined or multi-lined.

Single-line Comments:
Single-line comments start with two forward slashes (//).
Any text between // and the end of the line is ignored by the compiler (will not be executed).

Example 
printf("Hello World!"); // This is a comment

C Multi-line Comments:
Multi-line comments start with /* and ends with */.
Any text between /* and */ will be ignored by the compiler

Example
/* The code below will print the words Hello World!
to the screen, and it is amazing */
printf("Hello World!");
-----------------------------------------------------------------------------------------------------------------------------------------------------------------------

**C Variables**

Variables are containers for storing data values.
In C, there are different types of variables (defined with different keywords), for example:

int - stores integers (whole numbers), without decimals, such as 123 or -123
float - stores floating point numbers, with decimals, such as 19.99 or -19.99
char - stores single characters, such as 'a' or 'B'. Char values are surrounded by single quotes

Declaring (Creating) Variables
To create a variable, specify the type and assign it a value
Syntax:- type variableName = value;
Where type is one of C types (such as int), and variableName is the name of the variable (such as x or myName). The equal sign is used to assign a value to the variable.

So, to create a variable that should store a number, look at the following example:
int myNum = 15;

You can also declare a variable without assigning the value, and assign the value later:
int myNum;
myNum = 15;
-----------------------------------------------------------------------------------------------------------------------------------------------------------------------

**Format Specifiers**

Format specifiers are used together with the printf() function to tell the compiler what type of data the variable is storing. It is basically a placeholder for the variable value.
A format specifier starts with a percentage sign %, followed by a character.

For example, to output the value of an int variable, you must use the format specifier %d or %i surrounded by double quotes, inside the printf() function:
int myNum = 15;
printf("%d", myNum);  // Outputs 15

To print other types, use %c for char and %f for float
// Create variables
int myNum = 5;             // Integer (whole number)
float myFloatNum = 5.99;   // Floating point number
char myLetter = 'D';       // Character
// Print variables
printf("%d\n", myNum);
printf("%f\n", myFloatNum);
printf("%c\n", myLetter);

To combine both text and a variable, separate them with a comma inside the printf() function:
int myNum = 5;
printf("My favorite number is: %d", myNum);

To print different types in a single printf() function, you can use the following:
int myNum = 5;
char myLetter = 'D';
printf("My number is %d and my letter is %c", myNum, myLetter);
-----------------------------------------------------------------------------------------------------------------------------------------------------------------------

**Add Variables Together**

To add a variable to another variable, you can use the + operator:
int x = 5;
int y = 6;
int sum = x + y;
printf("%d", sum);
-----------------------------------------------------------------------------------------------------------------------------------------------------------------------

**Declare Multiple Variables**

To declare more than one variable of the same type, use a comma-separated list:
int x = 5, y = 6, z = 50;
printf("%d", x + y + z);

You can also assign the same value to multiple variables of the same type:
int x, y, z;
x = y = z = 50;
printf("%d", x + y + z);
-----------------------------------------------------------------------------------------------------------------------------------------------------------------------

**C Variable Names**

All C variables must be identified with unique names.
These unique names are called identifiers.
Identifiers can be short names (like x and y) or more descriptive names (age, sum, totalVolume).

Note: It is recommended to use descriptive names in order to create understandable and maintainable code:
// Good
int minutesPerHour = 60;

// OK, but not so easy to understand what m actually is
int m = 60;

The general rules for naming variables are:
Names can contain letters, digits and underscores
Names must begin with a letter or an underscore (_)
Names are case sensitive (myVar and myvar are different variables)
Names cannot contain whitespaces or special characters like !, #, %, etc.
Reserved words (such as int) cannot be used as names
-----------------------------------------------------------------------------------------------------------------------------------------------------------------------

**C Data Types**

Data Types
As explained in the Variables chapter, a variable in C must be a specified data type, and you must use a format specifier inside the printf() function to display it:
// Create variables
int myNum = 5;             // Integer (whole number)
float myFloatNum = 5.99;   // Floating point number
char myLetter = 'D';       // Character
// Print variables
printf("%d\n", myNum);
printf("%f\n", myFloatNum);
printf("%c\n", myLetter);
-----------------------------------------------------------------------------------------------------------------------------------------------------------------------

**Basic Data Types**

The data type specifies the size and type of information the variable will store.
In this tutorial, we will focus on the most basic ones:

Data      Type Size	     Description
int	      2 or 4 bytes	 Stores whole numbers, without decimals
float	    4 bytes	       Stores fractional numbers, containing one or more decimals. Sufficient for storing 7 decimal digits
double	  8 bytes	       Stores fractional numbers, containing one or more decimals. Sufficient for storing 15 decimal digits
char	    1 byte	       Stores a single character/letter/number, or ASCII values
-----------------------------------------------------------------------------------------------------------------------------------------------------------------------

**Basic Format Specifiers**

There are different format specifiers for each data type. Here are some of them:
Format Specifier	 Data Type
%d or %i	         int	
%f	               float	
%lf	               double	
%c	               char	
%s	               Used for strings
-----------------------------------------------------------------------------------------------------------------------------------------------------------------------

**C Constants**

Constants

When you don't want others (or yourself) to override existing variable values, use the const keyword (this will declare the variable as "constant", which means unchangeable and read-only):
const int myNum = 15;  // myNum will always be 15
myNum = 10;  // error: assignment of read-only variable 'myNum'

You should always declare the variable as constant when you have values that are unlikely to change:
const int minutesPerHour = 60;
const float PI = 3.14
-----------------------------------------------------------------------------------------------------------------------------------------------------------------------

**C Operators**

Operators are used to perform operations on variables and values.

In the example below, we use the + operator to add together two values:
int myNum = 100 + 50;

Although the + operator is often used to add together two values, like in the example above, it can also be used to add together a variable and a value, or a variable and another variable:
int sum1 = 100 + 50;        // 150 (100 + 50)
int sum2 = sum1 + 250;      // 400 (150 + 250)
int sum3 = sum2 + sum2;     // 800 (400 + 400)

C divides the operators into the following groups:
Arithmetic operators
Assignment operators
Comparison operators
Logical operators
Bitwise operators

Arithmetic Operators
Arithmetic operators are used to perform common mathematical operations.
Operator	Name	           Description	                             Example	
+	        Addition	       Adds together two values	                 x + y	
-	        Subtraction	     Subtracts one value from another	         x - y	
*	        Multiplication	 Multiplies two values	                   x * y	
/	        Division	       Divides one value by another	             x / y	
%	        Modulus	         Returns the division remainder	           x % y	
++	      Increment	       Increases the value of a variable by 1	   ++x	
--	      Decrement	       Decreases the value of a variable by 1	   --x

Assignment Operators
Assignment operators are used to assign values to variables.

In the example below, we use the assignment operator (=) to assign the value 10 to a variable called x:
int x = 10;

The addition assignment operator (+=) adds a value to a variable:
int x = 10;
x += 5;

A list of all assignment operators:
Operator	Example	   Same As	
=	        x = 5	     x = 5	
+=	      x += 3	   x = x + 3	
-=	      x -= 3	   x = x - 3	
*=	      x *= 3	   x = x * 3	
/=	      x /= 3	   x = x / 3	
%=	      x %= 3	   x = x % 3	
&=	      x &= 3	   x = x & 3	
|=	      x |= 3	   x = x | 3	
^=	      x ^= 3	   x = x ^ 3	
>>=	      x >>= 3	   x = x >> 3	
<<=	      x <<= 3	   x = x << 3

Comparison Operators
Comparison operators are used to compare two values.
Note: The return value of a comparison is either true (1) or false (0).

In the following example, we use the greater than operator (>) to find out if 5 is greater than 3:
int x = 5;
int y = 3;
printf("%d", x > y); // returns 1 (true) because 5 is greater than 3

A list of all comparison operators:
Operator	Name	                        Example	
==	      Equal to	                    x == y	
!=	      Not equal	                    x != y	
>	        Greater than	                x > y	
<	        Less than                   	x < y	
>=	      Greater than or equal to	    x >= y	
<=	      Less than or equal to	        x <= y


Logical Operators
Logical operators are used to determine the logic between variables or values:
Operator	 Name	         Description	                                              Example
&& 	       Logical and	 Returns true if both statements are true	                  x < 5 &&  x < 10	
|| 	       Logical or	   Returns true if one of the statements is true	            x < 5 || x < 4	
!	         Logical not	 Reverse the result, returns false if the result is true  	!(x < 5 && x < 10)


Sizeof Operator
The memory size (in bytes) of a data type or a variable can be found with the sizeof operator:
int myInt;
float myFloat;
double myDouble;
char myChar;
printf("%lu\n", sizeof(myInt));
printf("%lu\n", sizeof(myFloat));
printf("%lu\n", sizeof(myDouble));
printf("%lu\n", sizeof(myChar));
Note that we use the %lu format specifer to print the result, instead of %d. It is because the compiler expects the sizeof operator to return a long unsigned int (%lu), instead of int (%d). On some computers it might work with %d, but it is safer to use %lu.
-----------------------------------------------------------------------------------------------------------------------------------------------------------------------

**C If ... Else**

Conditions and If Statements

You learned from the operators comparison chapter, that C supports the usual logical conditions from mathematics:
Less than: a < b
Less than or equal to: a <= b
Greater than: a > b
Greater than or equal to: a >= b
Equal to a == b
Not Equal to: a != b
You can use these conditions to perform different actions for different decisions.

C has the following conditional statements:
Use if to specify a block of code to be executed, if a specified condition is true
Use else to specify a block of code to be executed, if the same condition is false
Use else if to specify a new condition to test, if the first condition is false
Use switch to specify many alternative blocks of code to be executed


The if Statement
Use the if statement to specify a block of C code to be executed if a condition is true.
Syntax:- 
if (condition) {
  // block of code to be executed if the condition is true
}
Note that if is in lowercase letters. Uppercase letters (If or IF) will generate an error.

In the example below, we test two values to find out if 20 is greater than 18. If the condition is true, print some text:
if (20 > 18) {
  printf("20 is greater than 18");
}

We can also test variables:
int x = 20;
int y = 18;
if (x > y) {
  printf("x is greater than y");
}


The else Statement
Use the else statement to specify a block of code to be executed if the condition is false
Syntax:
if (condition) {
  // block of code to be executed if the condition is true
} else {
  // block of code to be executed if the condition is false
}

Example
int time = 20;
if (time < 18) {
  printf("Good day.");
} else {
  printf("Good evening.");
}
// Outputs "Good evening."


The else if Statement
Use the else if statement to specify a new condition if the first condition is false.
Syntax:
if (condition1) {
  // block of code to be executed if condition1 is true
} else if (condition2) {
  // block of code to be executed if the condition1 is false and condition2 is true
} else {
  // block of code to be executed if the condition1 is false and condition2 is false
}

Example:
int time = 22;
if (time < 10) {
  printf("Good morning.");
} else if (time < 20) {
  printf("Good day.");
} else {
  printf("Good evening.");
}
// Outputs "Good evening."

Another Example
This example shows how you can use if..else if to find out if a number is positive or negative:
Example:
int myNum = 10; // Is this a positive or negative number?
if (myNum > 0)
  printf("The value is a positive number.");
else if (myNum < 0)
  printf("The value is a negative number.");
else
  printf("The value is 0.");
  
Short Hand If...Else (Ternary Operator)
There is also a short-hand if else, which is known as the ternary operator because it consists of three operands. It can be used to replace multiple lines of code with a single line. It is often used to replace simple if else statements:
Syntax:
variable = (condition) ? expressionTrue : expressionFalse;

Instead of writing:
int time = 20;
if (time < 18) {
  printf("Good day.");
} else {
  printf("Good evening.");
}

You can simply write:
Example
int time = 20;
(time < 18) ? printf("Good day.") : printf("Good evening.");
It is completely up to you if you want to use the traditional if...else statement or the ternary operator.
-----------------------------------------------------------------------------------------------------------------------------------------------------------------------







