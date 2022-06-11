# C_Language_Overview
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







