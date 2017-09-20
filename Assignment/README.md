The following code is a representation of a simple calculator in C programming launguage, defined as the int math function. The 
int math function takes two integer numbers whose values can be set in the int main function. ( 9 and 3 were chosen arbitrarly for 
this example) In the int math statement, a switch statement is used to compute different operations based on the selected operator.
In this example the addition operator, '+' , was selected resulting in the numbers 9 and 3 to be added together. The choices for 
operators are as follows; '+' for addition, '-' for subtraction, '*' for multiplication, '/' for division, and '%' for modulus. 
After an operation is carried out, the end value is stored in the variable "result" which is returned to the main function
and then printed to the screen.

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

