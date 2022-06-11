# C_Language_Overview

**Basic Syntax :**

#include <stdio.h>

_int main() {
  printf("Hello World!");
  return 0;
}_


1. #include <stdio.h> is a header file library that lets us work with input and output functions, such as printf() (used in line 4). Header files add functionality to C programs.
2. Another thing that always appear in a C program, is main(). This is called a function. Any code inside its curly brackets {} will be executed.
3. printf() is a function used to output/print text to the screen. In our example it will output "Hello World".

**Note that:** Every C statement ends with a semicolon ; 
               The body of int main() could also been written as: int main(){printf("Hello World!");return 0;}
               
 4. return 0 ends the main() function.
 5. Do not forget to add the closing curly bracket } to actually end the main function


**C Output**

1. The printf() function is used to output values/print text
_#include <stdio.h>
int main() {
  printf("Hello World!");
  return 0;
}_

2. You can add as many printf() functions as you want. However, note that it does not insert a new line at the end of the output
_#include <stdio.h>
int main() {
  printf("Hello World!");
  printf("I am learning C.");
  return 0;
}_

3. To insert a new line, you can use the \n character.
_#include <stdio.h>
int main() {
  printf("Hello World!\n");
  printf("I am learning C.");
  return 0;
}_

4. You can also output multiple lines with a single printf() function. However, be aware that this will make the code harder to read
_#include <stdio.h>
int main() {
  printf("Hello World!\nI am learning C.\nAnd it is awesome!");
  return 0;
}_

5.Two \n characters after each other will create a blank line
_#include <stdio.h>
int main() {
  printf("Hello World!\n\n");
  printf("I am learning C.");
  return 0;
}_

The newline character (\n) is called an escape sequence, and it forces the cursor to change its position to the beginning of the next line on the screen. This results in a new line

Examples of other valid escape sequences are:
\t - Creates a horizontal tab
\\ - Inserts a backslash character (\)
\" - Inserts a double quote character

