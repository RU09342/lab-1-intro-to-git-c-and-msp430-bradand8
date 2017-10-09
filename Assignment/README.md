## MSP430 Math Library

This Library can be used on any MSP430 processor. 

## Dependencies 

The only dependency for this library is that the specific processor header file is included in the main file. The MSP430.h file, for example, includes all Texas Instruments MSP430 based processors.

## How to Use

With the math.h and math.c files included in a project, all that is needed to use the math function is to call the function and specify two integer numbers and an operator (Accepted Operators are + , - , * , / , % ) as shown below:

``` math(int 1, int2, operator); ```

## Description of Code

The following code is a representation of a simple calculator in C programming language, defined as the int math function (math.h). The 
int math function takes two integer numbers whose values can be set in the int main function. ( 9 and 3 were chosen arbitrarly for 
this example) In the int math statement, a switch statement is used to compute different operations based on the selected operator.
In this example the addition operator, '+' , was selected resulting in the numbers 9 and 3 to be added together. The choices for 
operators are as follows; '+' for addition, '-' for subtraction, '\*' for multiplication, '/' for division, and '%' for modulus. 
After an operation is carried out, the end value is stored in the variable "result" which is returned to the main function
and then printed to the screen in this code example.




## Code Example

```c
/* 
   math.h

   Created on: 9/18/2017
   
   Last edited: 9/20/2017
   
   Author: Bradley Anderson

*/




#include <stdio.h>

int math(int num1, int num2, char operator);

int main()
{
	printf("%f", math(9,3,'+'));  // ( 9 , 3, and + were chosen for this example)

	return 0;
}

int math(int num1, int num2, char operator, {

	/*performs various operations based on the chosen operator. Accepted Operators (+,
	- ,* , / , %) */

	float result = 0;
	switch(operator)
	{
		case '+' : 
			result = num1 + num2; /*adds two numbers and stores value in "result" */
			printf("%f", result);
			break;
		
		case '-' :
			result = num1 - num2; /* subtracts two numbers and stores value in "result" */
			printf("%f", result);
			break;

		case '*' :
			result = num1 * num2; /* multiplies two numbers and stores value in "result" */
			printf("%f", result);
			break;
			
		case '/' :
			result = num1 / num2; /*divides number one by number two and stores value in "result" */
			printf("%f", result);
			break;

		case '%' :
			result = num1 % num2; /*divides num1 by num2 and stores the value of the remainder in "result" */
			printf("%f", result);
			break;
	}
		return result;
	}
```

  ###### Created by Bradley Anderson

