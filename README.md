# C-and-Java-Syntax-Notes
Various notes made studying how to program in C++. I heavily used the textbook, STARTING OUT WITH C++ FROM CONTROL STRUCTURES TO OBJECTS by Tony Gaddis when making these notes. I will update this to include more notes in Java 


To increment a value means to increase it by 1 and to decrement a value means to decrease it by 1. They work on variables. 
The operand of these operators must be an lvalue. When they are used  they increment or decrement its operand even when its operand is being assigned to another variable, even when it is used in a function or another object. The more it is used the more operator affects operand. Its operand keeps incrementing or decrementing based on how many times it's read;

cout << x++ // value = 1
cout << x++  // value = 2
cout << x++ // value =3

int x;

int y;
             // Play with this // Value displayed is 32. can change 

X=2;       // diff fixed mode can change it

y= x++;

cout << x << y << endl;

y = ++x;


Postfix mode: the operator is placed after the variable:  EX: num++ .

Prefix mode: operator placed before the variable  EX: ++num


// This program demonstrates the ++ and -- operators.
#include <iostream>
using namespace std;
int main()
{
   int num = 4;   // num starts out with 4.
   
   // Display the value in num.
   cout << "The variable num is " << num << endl;
   cout << "I will now increment num.\n\n";
   
   // Use postfix ++ to increment num.
   num++;
   cout << "Now the variable num is " << num << endl;
   cout << "I will increment num again.\n\n";
// Use prefix ++ to increment num.
   ++num;
   cout << "Now the variable num is " << num << endl;
   cout << "I will now decrement num.\n\n";
   
   // Use postfix -- to decrement num.
   num--;
   cout << "Now the variable num is " << num << endl;
   cout << "I will decrement num again.\n\n";
   
   // Use prefix -- to increment num.
   --num;
   cout << "Now the variable num is " << num << endl;
   return 0;
The fixed mode the operator is used in does matter when your using objects  and functions like cout  and if() on them.
https://www.thenewboston.com/videos.php?cat=16&video=17497

 int num = 4; 
cout << num++ << endl; //  increment doesn't happen yet. Value displayed is 4
	<< num  << endl; // increment does happen. Value displayed is 5
	
	/* if used the ++ operators in prefix mode in prefix mode increment will happen when its operand is first displayed*/
	
	 int num = 4; 
	cout << ++num<< endl; //  Value displayed is 4
		<< num  << endl; // increment already happened. Value displayed is 5
		
		x= 99
		If( x++ < 100)
			cout << "It is true!\n; // Display It is true
		
		
		
	Unlike prefix mode, the postfix mode causes the increment to happen after the value of the variable is used in the expression.

						A loop is part of a program that repeats
						
A loop is a control structure that causes a statement or group of statements to repeat. Loops that never end are called infinite loops.
https://www.thenewboston.com/videos.php?cat=16&video=17494

while(condition) 
{
   statement(s);
}

The condition is a Boolean expression. It evaluates to be to be true or false. The header of the example is the loop header . 
It consists of the key word while followed by a relational expression enclosed in (). If the condition is true, the statement executes until the condition is false.
The statement that is repeated is known as the body of the loop. Like the if statement, w/o the statements following it.  
Don't forget the braces. like if statement don't forget them. 


Each repition of a loop is known as an iteration. Loops sometimes should have prime readings/prompts a top of them and an input validation in them which tells user their invalid entry and what values they should input to make the program work.


The while loop is known as a pretest loop; it tests its expression before each iteration
The loop will never iterate if the test expression is false to start with in a while loop

https://www.thenewboston.com/videos.php?cat=16&video=17495

Find a loop control variable in the above video


	A counter is a variable that is regularly incremented or decremented each time a loop iterates
	
	int num = 0; // num is the counter
	while (num++ < 10)
		cout  << num << "\t\t" <<  ( num * num) << endl;
		
	Is a loop control variable a counter variable?
	
	The do-while loop is a posttest loop, which means its expression is tested after each iteration
			https://www.thenewboston.com/videos.php?cat=16&video=17500
do {
Statement/s;
} while ( condition );





The do-while loop is a posttest loop. It doesn't test its expression until it has completed an iteration. This loop always performs at least 1 iteration, even if the condition is false. The statements are executed first. If the conditional expression in the parameters of the function is true then they'll keep being executed until the conditional expression is false. This is the difference between a do-while loop and a while loop.

int count = 10;

/* counter: a variable that is incremented or decremented each time a loop repeats*/

do
	cout << "Hello World\n";
	while(count++ < 1); // program output Hello World
	
Int v = 0;
do
	cout << v++; // value = 01234
	while (v < 5);
			
			
			The for loop is ideal for performing a known number of iterations
			



for ( init; condition; increment ) /* this is a pretest loop. test expression evaluated before loop iterates*/
{
   statement(s);
}

The 1st line of the for loop is the loop header. The 1st expression is the initialization expression. The 2nd expression is the test expression. Third is the update expression
https://www.thenewboston.com/videos.php?cat=16&video=17498

Ex: 

for (count = 1; count <= 5; count++)
cout << "Hello" << endl; // since it only has 1 statement braces are not needed


You can also define variables in a for loop instead of just initializing them. When a variable is defined in the initialization expression of a for loop, the scope of the variable is limited to that of the loop. Is this true for all functions? Whenever, a variable is defined inside parameters is the scope of the variable limited to that of the f(x)?

You can intitiionalize or define multiple variables in 1 for loop. 

int x, y;
for (x = 1, y = 1; x <= 5; x++)// Notice where the ; are placed
{
cout << x << y; // Don't separate multiple test expressions this way. Use // logical operators to separate them instead of commas           

No need to initialize variable in for-loop if the specific variable is already defined and initialized.

Recommended to modify variables in the update expression in the for loop instead of the body

for (x=1;x<=10; x++)// update expression no longer needed since its already in the function just elsewhere and not its parameters

{

cout << a << endl;

x++; // increment twice for each iteration.

}
 Unless programmer specifically wants x to increment twice, update expression can be omitted 
for reasons stated in comments of above program.

You can even omit the test expression. If that's done the loopp will keep executing. It won't stop

for( ; ; )
	cout << "Hello World\n"; // The string is displayed forever until something interrupts the program, or until program stops running.
	
				A running total is a sum of numbers that accumulates with each iteration of a loop.
				 The variable used to keep the running total is called an accumulator

Set the accumulator to 0

// This program takes daily sales figures over a period of time
// and calculates their total.
#include <iostream>
#include <iomanip>
using namespace std;
int main()
{
   int days;            // Number of days
   double total = 0.0;  // Accumulator, initialized with 0
// Get the number of days.
   cout << "For how many days do you have sales figures? ";
   cin >> days;
   
   // Get the sales for each day and accumulate a total.
   for (int count = 1; count <= days; count++)
   {
      double sales;
      cout << "Enter the sales for day " << count << ": ";
      cin >> sales;
      total += sales;   // Accumulate the running total.
   }
   
   // Display the total sales.
   cout << fixed << showpoint << setprecision(2);
   cout << "The total sales are $" << total << endl;
   return 0;
}


		A sentinel is a special value that marks the end of a list of values
		https://www.thenewboston.com/videos.php?cat=16&video=17496  
		
		
		// This program calculates the total number of points a 
// soccer team has earned over a series of games. The user
// enters a series of point values, then -1 when finished.
#include <iostream>
using namespace std;
		int main()
{
   int game = 1,   // Game counter
       points,     // To hold a number of points
       total = 0;  // Accumulator
		cout << "Enter the number of points your team has earned\n";
   cout << "so far in the season, then enter -1 when finished.\n\n";
   
		   // -1 is the sentinel in this program
		
		   cout << "Enter the points for game " << game << ": ";
   cin >> points;
		while (points != -1)// They used a while loop to help make the sentinel
   {  
      total += points;
      game++;
      cout << "Enter the points for game " << game << ": ";
      cin >> points;
   }
   cout << "\n The total points are " << total << endl;
   return 0;
}
		
		When reading a value from a file with the stream extraction operator, the operator returns a true or false value indicating whether the value was successfully read. This return value can be used to detect when the end of a file has been reached????????????????

int number, total = 0;
for (int count = 0; count < 7; count++) // Programmer find the accumulator
{
cout << "Enter a number: ";
cin >> number;
total += number;
}



		Although most repetitive algorithms can be written with any of the 3 types of loops, each works best in different situation
		
The while loop is a conditional loop. It repeats as long as a particular condition exists. It's also a pretest loop. It's ideal where you don't want the loop to iterate if the condition is false from the beginning. It's good for validating inputs. Sentinel values are good application of the while loop. Look at the only program with a sentinel in these notes. It was done with a while loop.

The do-while loop is like the while loop. It's conditional. It's ideal in situations where you always want the loop to iterate at least once. It's a good choice for repeating a menu.

The for loop is a pretest loop unlike the do-while loop. It's ideal in situations where the exact # of iterations is known


Switch and loop f(x)s can work really well together

				A loop that is inside another loop is called a nested loop
				
The fill f(x) fill sequence with values http://www.cplusplus.com/reference/algorithm/fill/

	
	while(condition)
{
   while(condition)
   {
      statement(s);
   }
   statement(s); // you can put more statements.
}
	
	From <http://www.tutorialspoint.com/cplusplus/cpp_nested_loops.htm> 
	
	• An inner loop goes through all of its iterations for each iteration of an outer loop?
	• Inner loops complete their iterations faster than outer loops?
	• To get the total number of iterations of a nested loop, multiply the number of iterations of all loops
	• http://www.c4learn.com/cplusplus/cpp-nested-loops/
	
	
	The break statement causes a loop to terminate early . It can only be used on switches or loop functions.
	
	Even if a loop is programed initially to execute a certain amount of times, a break can make it executed less than that.
	
	int count = 0;
	while (count++ < 10)
	{
		cout << count << endl;
		if (count == 5)
		break; // b/c if statement the loop will only execute 5 times
	}
	
		The continue statement causes a loop to stop its current iteration & begin the next 1
		
		int testVal = 0;
		while (testVal++ < 10)
		{
			If (testVal == 4)
				continue;
			cout << testValue << "  Hey!";
		}
		
		Why do people use this continue f(x)? Why do people use the break f(x) in loops
						
						Files what is needed?
		
		
		The last statement in a loop a CPU reads when reading a loop are the statements executed when the loop just becomes false. When relational expression of function is false only the function stops executing or not work. Everything else works. The loop f(x)s make loops not the increment/decrement operator. These in/decremental operators do what they are they are called, increment. They don't loop
		
		
		
		   // Basic 10-element integer array.
    int x[10] = { 1, 2, 3, 4, 5, 6, 7, 8, 9, 10 };
		// Range-based for loop to iterate through the array.
    for( int y : x ) { // Access by value using a copy declared as a specific type. 
                       // Not preferred.
        cout << y << " ";
    }
    cout << endl;
		
		From <https://msdn.microsoft.com/en-us/library/jj203382.aspx> 
		
		Output:
		1 2 3 4 5 6 7 8 9 10
		
		
		
		A file’s read position marks the location of the next byte that will be read from 
		the file. When an input file is opened, its read position is initially set to the first 
		byte in the file. 
		
		From <http://media.pearsoncmg.com/aw/ecs_gaddis_sowcpp_cs_8/app_cs/Z13_GADD9395_08_SE_APP13.pdf> 
		
		
		

		
		
		File buffer: a small "holding section" of memory the file bound data is written into. Data is temporarily stored there. Operating systems automatically store data in a file buffer. Closing a file may cause any unsaved data in file buffer to be saved in the file.
    
    

Functions


Look at this Powerpoint @ http://www.slideshare.net/kumar_vic/function-in-c-30522092




You can define functions and input defined variables in the parenthesis of the function. You can then call function from the name you gave them and input the values of those variables in its parenthesis or parameters. Full fledged functions like int main has datatypes and names made by the user to identify them.  Like variables functions can be called w/o being defined again. All they need is their name and their (). The return type gives the final calculation of the function.
https://www.thenewboston.com/videos.php?cat=16&video=17486

https://www.thenewboston.com/videos.php?cat=16&video=17487

			
			A program may be broken up into manageable functions
			
Code reuse refers to writing the code to perform a task once and then reusing it each time you need to perform the task

			A function call is a statement that causes a function to execute. A function definition contains the statements that make up the function
			
When making a function, you have to define it first. You must write its definition, which consists of writing the return type, name, parameter list, and body of the function.

Return type: A function can send a value to the part of the program that executed it. The return type is the data type of the value sent to it. It gives the final calculation of the function.  Not all functions need a return type. Void functions don't need a return type. 

Parameter list: The program can send data into a function. The parameter list is a list of variables that hold the values being passed to the function.

A function is executed when it's called. All functions except function main must be called before it's executed. When a  f(x) is called, the program branches to that function and executes the statements in its body.


https://www.thenewboston.com/videos.php?cat=16&video=17487

// This program has two functions: main and displayMessage
#include <iostream>
using namespace std;
//*****************************************
// Definition of function displayMessage  *
// This function displays a greeting.     *
//*****************************************
void displayMessage()
{
   cout << "Hello from the function displayMessage.\n";
}
//*****************************************
// Function main                          *
//*****************************************
int main()
{
   cout << "Hello from main.\n";
   displayMessage();
   cout << "Back in function main again.\n";
   return 0;
}



Like variables functions can be called w/o being defined again. All they need is their name and their (). The return type gives the final calculation of the function.



A function prototype eliminates the need to place a function definition before all calls to the function
EX: void displayMessage(); // at least datatypes should be inside prototype

You must either place the f(x) definition 1st or place the function prototype first. You can't type both for 1 particular function. If you do the program will not compile.

What about the return type? Where is it in a function prototype? In a void function the keyword void is the return type of the function. The return type is in the function definition that occurs later in the program the prototype is in.

When a function is called, the program may send values into the function.

Values that are sent into a f(x) are called arguments. 

EX: pow(2.0, 4.0);

Variables that are sent into a f(x) are called parameters. The scope of a parameter is limited to the body of the f(x that uses it. The parameter has a local scope

EX: void displayValue(int num)
{
	cout << "The value is " << num << endl;
	

}

Any argument listed inside the parenthesis of a function call is copied into the function's parameter variable
https://www.thenewboston.com/videos.php?cat=16&video=17487

Can variables be defined when functions are called? Can they only be defined when the function is being defined?

When an argument is passed into a parameter, only a copy of the argument's value is passed. Changes to the parameter don't affect the original argument.
Any changes you make to the parameter in the function is made to the copy and does not change the value of the argument in the calling function. 


From <https://elearning.utdallas.edu/bbcswebdav/pid-894609-dt-content-rid-7979608_1/users/dgv130030/CS%201136%20F15/Lesson%209/CS%201136%20Laboratory%20Lesson%209.pdf>


https://elearning.utdallas.edu/bbcswebdav/pid-894609-dt-content-rid-7979608_1/users/dgv130030/CS%201136%20F15/Lesson%209/CS%201136%20Laboratory%20Lesson%209.pdf



When only a copy of an argument is passed to a f(x), it's said to be passed by value.

Functions are ideal for use in menu-driven programs. When the user selects an item from a menu, the program can call the appropriate function.

Menu-driven program: program execution is controlled by a user selecting from a list of actions.

Menu: list of choices on the screen


A modular program is broken up into functions that perform specific tasks.



The return causes a function to end immediately


// This program uses a function to perform division. If division
// by zero is detected, the function returns.
#include <iostream>
using namespace std;
// Function prototype.
void divide(double, double);
int main()
{
   double num1, num2;
cout << "Enter two numbers and I will divide the first\n";
   cout << "number by the second number: ";
   cin >> num1 >> num2;
   divide(num1, num2);
   return 0;
}
//***************************************************************
// Definition of function divide.                               *
// Uses two parameters: arg1 and arg2. The function divides arg1*
// by arg2 and shows the result. If arg2 is zero, however, the  *
// function returns.                                            *
//***************************************************************
void divide(double arg1, double arg2)
{
   if (arg2 == 0.0)
   {
      cout << "Sorry, I cannot divide by zero.\n";
      return;
   }
   cout << "The quotient is " << (arg1 / arg2) << endl;
}

A function may send a value back to the part of the program that called the function

Functions that return a value are appropriately known as value-returning functions.


return expression;

Expression is the value, variable or named constant that holds a value to be returned. The value of the expression is converted to the data type that the function returns, and is sent back to the statement that called the f(x).


A value-returning f(x) returns a value of a specific data type.

How is like and different from the auto datatype?

"The auto keyword directs the compiler to use the initialization expression of a declared variable, or lambda expression parameter, to deduce its type"

From <https://msdn.microsoft.com/en-us/library/dd293667.aspx> 

https://www.thenewboston.com/videos.php?cat=16&video=17504



Functions may return true or false values


// This program uses a function that returns true or false.
#include <iostream>
using namespace std;
// Function prototype
bool isEven(int);
int main()
{
   int val;
// Get a number from the user.
   cout << "Enter an integer and I will tell you ";
   cout << "if it is even or odd: ";
   cin >> val;
   
   // Indicate whether it is even or odd.
   if (isEven(val))
      cout << val << " is even.\n";
   else
      cout << val << " is odd.\n";
   return 0;
}
//*****************************************************************
// Definition of function isEven. This function accepts an        *
// integer argument and tests it to be even or odd. The function  *
// returns true if the argument is even or false if the argument  *
// is odd. The return value is an bool.                           *
//*****************************************************************
bool isEven(int number)
{
   bool status;
if (number % 2 == 0)
      status = true;  // number is even if there is no remainder.
   else
      status = false; // Otherwise, the number is odd.
   return status;
}

A local variable is defined inside a function & isn't accessible outside the function. A global variable is defined outside all functions & is accessible to all functions in its scope.

A function's local variables exist only while the functions is executing. This is known as the lifetime of a local variable. This means that any value stored in a local variable is lost between calls to the f(x) in which the variable is declared.

What is the lifetime of a global variable?

  They are any variables defined outside all the f(X)s in a program. Global numeric variables are initialized to 0. Global characters are initialized to NULL. Global variables have an infinite scope beginning when the variable is 1st defined. They can be accessed by all the f(X)s within its scope like local variables. You should use global constants instead of global variables.

What's the difference between a global character variable and a numeric global variable?


// This program has an uninitialized global variable.
#include <iostream>
using namespace std;
int globalNum;  // Global variable, automatically set to zero
int main()
{
   cout << "globalNum is " << globalNum << endl;
   return 0;
}

What will be displayed when above program is executed?

---
You can't give a parameter variable & a local variable in the same f(x) the same name.

---

To make a local variable have to essentially have the same scope, lifetime, and default initialization as a global variable make the variable static. 
EX: static int statNum;

// This program uses a static local variable.
#include <iostream>
using namespace std;
void showStatic(); // Function prototype
int main()
{
   // Call the showStatic function five times.
   for (int count = 0; count < 5; count++)
      showStatic();
   return 0;
}
//**************************************************************
// Definition of function showStatic.                          *
// statNum is a static local variable. Its value is displayed  *
// and then incremented just before the function returns.      *
//**************************************************************
void showStatic()
{
   static int statNum;
cout << "statNum is " << statNum << endl;
   statNum++;
}

What will the above program display?


Default arguments are passed to parameters automatically if no argument is provided  in the function call.
https://www.thenewboston.com/videos.php?cat=16&video=17504 skip to 2 min of  video

All the default arguments may be overridden. If a f(x) doesn't have a prototype, default arguments may be specified on the f(x) header. Default arguments can't hold parameters. They can hold literals and constants

// This program demonstrates default function arguments.
#include <iostream>
using namespace std;
// Function prototype with default arguments
void displayStars(int = 10, int = 1);
int main()
{
   displayStars();      // Use default values for cols and rows.
   cout << endl;
   displayStars(5);     // Use default value for rows.
   cout << endl;
   displayStars(7, 3);  // Use 7 for cols and 3 for rows.
   return 0;
}
//********************************************************
// Definition of function displayStars.                  *
// The default argument for cols is 10 and for rows is 1.*
// This function displays a square made of asterisks.    *
//********************************************************
void displayStars(int cols, int rows)
{
   // Nested loop. The outer loop controls the rows
   // and the inner loop controls the columns.
   for (int down = 0; down < rows; down++)
   {
      for (int across = 0; across < cols; across++)
         cout << "*";
      cout << endl;
   }
}

When used as parameters, reference variables allow a f(x) to access the parameter's original argument. Changes to the parameter are also made to the argument. 
When you pass by reference the function has access to the variables passed to it. When the function changes an argument that was passed by reference it changes the value of the original variable passed to the function. 

From <https://elearning.utdallas.edu/bbcswebdav/pid-894609-dt-content-rid-7979608_1/users/dgv130030/CS%201136%20F15/Lesson%209/CS%201136%20Laboratory%20Lesson%209.pdf> 

 &&&&&&&&&&


By using a reference variable as a parameter, a function may change a variable that is defined in another function. Reference variables are defined like regular variables, except you place an ampersand (&) in front of the name.
EX:

Void doubleNum( int &refVar )
{
	redVar *= 2;
}

The ampersand must appear in both the prototype & the header of any f(x) that uses a reference variable as a parameter. It doesn't appear in the function call.

// This program uses a reference variable as a function
// parameter.
#include <iostream>
using namespace std;
// Function prototype. The parameter is a reference variable.
void doubleNum(int &);
int main()
{
   int value = 4;
cout << "In main, value is " << value << endl;
   cout << "Now calling doubleNum..." << endl;
   doubleNum(value);
   cout << "Now back in main. value is " << value << endl;
   return 0;
}
//**********************************************************
// Definition of doubleNum.                                *
// The parameter refVar is a reference variable. The value *
// in refVar is doubled.                                   *
//**********************************************************
void doubleNum (int &refVar)
{
   refVar *= 2;
}

When a reference parameter is used, it's said that the argument is passed by reference


Several f(x)s may have the same name, as long as their parameter lists are different

The compiler will determine which version of function to call based upon the number and 
data types of the arguments in the function call.

From <https://elearning.utdallas.edu/bbcswebdav/pid-950869-dt-content-rid-9069273_1/users/lthomp/CS%201336%20Fall%202015/Slides/CS_1336_Chapter_06_PDF.pdf> 



The function signature is the name of the f(x) & the data types of the f(x)'s parameters in the proper order. EX:

https://www.thenewboston.com/videos.php?cat=16&video=17506

The name of parameters in f(x)s can be overridden by the names of them in their f(x) prototypes?


// This program uses overloaded functions.
#include <iostream>
#include <iomanip>
using namespace std;
// Function prototypes
int square(int);
double square(double);
int main()
{
   int userInt;
   double userFloat;
// Get an int and a double.
   cout << fixed << showpoint << setprecision(2);
   cout << "Enter an integer and a floating-point value: ";
   cin >> userInt >> userFloat;
   
   // Display their squares.
   cout << "Here are their squares: ";
   cout << square(userInt) << " and " << square(userFloat);
   return 0;
}
//**************************************************************
// Definition of overloaded function square.                   *
// This function uses an int parameter, number. It returns the *
// square of number as an int.                                 *
//**************************************************************
int square(int number)
{
   return number * number;
}
//***************************************************************
// Definition of overloaded function square.                    *
// This function uses a double parameter, number. It returns    *
// the square of number as a double.                            *
//***************************************************************
double square(double number)
{
   return number * number;
}


The exit () function causes a program to terminate, regardless of which function or control mechanism is executing.

A C++ program stops executing when the return statement in f(x) main is encountered. This is not true for other f(x)s. Only when the exit () is used can a program end w/o int main ending.

// This program shows how the exit function causes a program
// to stop executing.
#include <iostream>
#include <cstdlib>   // For exit
using namespace std;
void function();  // Function prototype
int main()
{
   function();
   return 0;
}
//***********************************************************
// This function simply demonstrates that exit can be used  *
// to terminate a program from a function other than main.  *
//***********************************************************
void function()
{
   cout << "This program terminates with the exit function.\n";
   cout << "Bye!\n";
   exit(0);
   cout << "This message will never be displayed\n";
   cout << "because the program has already terminated.\n";
}

EXIT_SUCCESS can be placed inside the parenthesis of exit() instead of 0. The exit () will work the same with either of those arguments in it.

EXIT_FAILURE is defined as the termination code that commonly represents an unsuccessful exit under the current operating system. This is used as an argument of exit()

A stub is a dummy f(x) that is called instead of the actual f(x) it represents. It usually displays a test message acknowledging that it was called.

A stub allows you to determine whether your program is calling a f(x) when you expect it to, & to confirm that valid values are being sent to the f(x). If the stub reprents a f(x) that returns a value, than the stub should return a test value.

A driver is a program that tests a f(x) by simply calling it. If the f(x) accepts arguments, the driver passes test data.

// This program is a driver for testing the showFees function.
#include <iostream>
using namespace std;
// Prototype
void showFees(double, int);
int main()
{
   // Constants for membership rates
   const double ADULT = 40.0;
   const double SENIOR = 30.0;
   const double CHILD = 20.0;
// Perform a test for adult membership.
   cout << "Testing an adult membership...\n"
        << "Calling the showFees function with arguments "
        << ADULT << " and 10.\n";
   showFees(ADULT, 10);
   
   // Perform a test for senior citizen membership.
   cout << "\nTesting a senior citizen membership...\n"
        << "Calling the showFees function with arguments "
        << SENIOR << " and 10.\n";
   showFees(SENIOR, 10);
   
   // Perform a test for child membership.
   cout << "\nTesting a child membership...\n"
        << "\nCalling the showFees function with arguments "
        << CHILD << " and 10.\n";
   showFees(CHILD, 10);
   return 0;
}
//*****************************************************************
// Definition of function showFees. The memberRate parameter      *
// the monthly membership rate and the months parameter holds the *
// number of months. The function displays the total charges.     *
//*****************************************************************
void showFees(double memberRate, int months)
{
    cout << "The total charges are $"
         << (memberRate * months) << endl;
}


		Arrays
    An array allows you to store and work with multiple values of the same datatype


An array works like a variable that can store a group of values, all of the same type. The values are stored together in consecutive memory locations.

int number[25]



The number inside the brackets of an array is the array's size declarator. It indicates the # of elements or values an array can hold. The size declarator inside the brackets must be a literal or named constant that has a value that is greater than 0 and is an integer.

The size of an array can be found by multiplying the datatype of the array by the size declarator.

 https://www.thenewboston.com/videos.php?cat=16&video=17508

Each of these elements in an array are assigned a # known as a subscript. 

A subscript is used as an index to pinpoint a specific element within an array. The 1st element is assigned the subscript 0, the 2nd element is assigned 1, and so forth. The last element of an array is assigned a subscript that is 1 less than the value of the size declarator. Subscripts can be stored in variables

// This program asks for the number of hours worked
// by six employees. It stores the values in an array.
#include <iostream>
using namespace std;
int main()
{
   const int NUM_EMPLOYEES = 6;
   int hours[NUM_EMPLOYEES];
   
   // Get the hours worked by each employee.
   cout << "Enter the hours worked by "
        << NUM_EMPLOYEES << " employees: ";
   cin >> hours[0];
   cin >> hours[1];
   cin >> hours[2];
   cin >> hours[3];
   cin >> hours[4];
   cin >> hours[5];
   
   // Display the values in the array.
   cout << "The hours you entered are:";
   cout << " " << hours[0];
   cout << " " << hours[1];
   cout << " " << hours[2];
   cout << " " << hours[3];
   cout << " " << hours[4];
   cout << " " << hours[5] << endl;
   return 0;
}

Inputting data into array must be done 1 element at a time. You must use multiple cin statements to read data into each array element, or use a loop -- which is less time consuming -- to step through the array, reading data into its elements.

https://www.thenewboston.com/videos.php?cat=16&video=17509


C++ gives you the freedom to store data past an array's boundaries.  You don't want to store data past an array's boundaries! C++ doesn't have array bounds checking.

Array may be initialized when they are defined

int days[12] = {14, 25, 31, 30, 31, 30, 31, 31, 31, 40, 54, 99}

The series of values inside the braces and separated with commas is called an initialization list. It's possible to define an array w/o a size declarator, as long as you provide an initialization list.

int days[12] = {14, 25, 31}

C++ doesn't require a value for every element . If an array is partially initialized, the uninitialized elements will be set to 0. It's even true for local arrays. If a local array is completely uninitialized, its elements will contain "garbage." like all other local variables. What happens if a global variable or global array is not initialized?

If an array is defined globally, all of its elements are initialized to 0 by default. Local arrays, however, have no default initialization value.

C++ DOES NOT PROVIDE A WAY TO SKIP ELEMENTS IN THE INITIALIZATION LIST

double rating[] = { 1.0, 1.5, 3.0, 3.5, 4.5 } 

// why array numbers have decimals?


Anytime the name of an array is used w/o brackets and a subscript, it is seen as the array's beginning memory address. An array's name is seen as the array's beginning memory address. You must use a loop to display the contents of each of the array's elements.

How can you assign values to arrays? Hint look  at the big program above.

https://www.thenewboston.com/videos.php?cat=16&video=17509

Here's the 1 exception to this rule of Displaying content of an array

char name[] = "Ruth";
cout << name << endl;

This cout statement displays the string "Ruth" instead of the array's address. The << operator is designed to behave differently when it receives the address of a char array. This works b/c char array contains a null terminated C-string as well.

You can't use  == operator with the names of 2 arrays to determine whether the arrays are =. When you use the == operator with array names, the operator compares the beginning memory addresses of the arrays, not the contents of the arrays. Anytime the name of an array is used w/o brackets and a subscript, it is seen as the array's beginning memory address.

By using the same subscript, you can build relationships between data stored in several arrays.

You can multiply with arrays that have the same subscripts and assign them to variables?
Can arrays get assigned values that is more than the amount specified by it's size declarator. If yes, would it and what logical error it may cause?

F(x)s that accept an array as an argument, and processes that array also accept the argument specifying the array's size.

To pass an array as an argument to a f(x), pass the name of the array

https://www.thenewboston.com/videos.php?cat=16&video=17511

Array parameters work very much like reference variables. They give the f(x) direct access to the original array.

https://www.thenewboston.com/videos.php?cat=16&video=17510

A two-dimensional array is like several identical arrays put together. It's useful for storing multiple sets of data

Unlike the 1D arrays we worked with earlier which only can hold 1 set of data, 2D arrays can hold multiple sets of data.



Double scores[3][4];

The 1st size declarator specifies the # of rows, & the 2nd size declarator specifies the # of columns.

When initializing a 2D array, it helps to enclose each row's initialization list in a set of braces.

int hours[3][2] = { {8, 5}, {7,9}, {6, 3} };

C++ doesn't require a value for every element . If an array is partially initialized, the uninitialized elements will be set to 0. This applies to multi-dimensional arrays as well.

https://www.thenewboston.com/videos.php?cat=16&video=17512

A f(x) that accepts an  array as an argument, and process that array should also accept an argument specifying the array's size. with the array alone the function has no way of determining the number of elements it has?


When a 2D array is passed to a f(x) or in other words when a function that accepts 2D arrays is being prototyped or defined, the parameter type must contain a size declarator for the number of columns. Why is that? Why does the f(x) need a size declarator for a 2D array rather than a 1D array? Do any of these rules apply to other multi-dimensional arrays or 1D arrays..

void showArray(int array[][4], int rows)

When a compiler generates code for accessing the elements of a 2D array, it needs to know how many bytes separate the rows in memory?


A two-dimensional array of characters can be used as an array of strings

// This program displays the number of days in each month.
#include <iostream>
using namespace std;
int main()
{
   const int NUM_MONTHS = 12;  // The number of months
   const int STRING_SIZE = 10; // Maximum size of each string
   
   // Array with the names of the months
   char months[NUM_MONTHS][STRING_SIZE] = 
                 { "January", "February", "March",
                   "April", "May", "June",
                   "July", "August", "September",
                   "October", "November", "December" };
   
   // Array with the number of days in each month
   int days[NUM_MONTHS] = {31, 28, 31, 30,
                           31, 30, 31, 31,
                           30, 31, 30, 31};
// Display the months and their numbers of days.
   for (int count = 0; count < NUM_MONTHS; count++)
   {
      cout << months[count] << " has ";
      cout << days[count] << " days.\n";
   }
   return 0;
}

C++ doesn't limit the # of dimensions that an array may have. It's possible to create arrays with multiple dimensions, to model data that occur in multiple sets.

double seats[3][5][8];

The Standard Template Library (STL) offers a vector data type, which in many ways, is superior to standard arrays.

The data types that're defined in the STL are commonly called containers. They are called containers b/c they store and organize data.

A sequence containers organize data in a sequential fashion, similar to an array.

Associative containers organize data with keys, which allow rapid, random access to elements stored in the container.

A vector is a sequence container. They hold and store elements is the same way as arrays. You can use the array subscript operator [] to read the individual elements in the vector. However, vectors don't need any size declarators. If you add a value to a vector is already full, the vector will automatically increase its size to accommodate the new value --that eliminates the problem of bound checking. Does it? Vectors can report the # of elements they contain.

Yo use vectors you need a vector header file

#include <vector>

Here's how a defined vector:

vector<int> numbers(10);

// This statement above defines numbers as a vector of 10 ints.
// This is just a starting value. Its size will expand if you
// add more than 10 values to it

When you specialize a starting size for a vector, you may also specify an initialization value. The initialization value is copied to each element

vector<int> numbers(10, 2)

// In the above statement, number is defined as a vector of 10 ints
// Each element in numbers is initialized to the value 2

// How do you initialized more values in it?

To assign new specific values to a specific place in an array use []. To assign value 12 in element 4

vector_Name[5] = 12

Is this the same for arrays? Yes it is about the same for arrays

push_back(value)/* It's a vector member f(x) that stores a value in the last element of the vector. If the vector is full or empty, a new element is made.*/

X=at(5) /* at vector member f(x)s returns the value of the element located at 5 in the vector. Is 5 a subscript 

Look at p 450 & 451

// This program stores, in two vectors, the hours worked by 5
// employees, and their hourly pay rates.
#include <iostream>
#include <iomanip>
#include <vector>       // Needed to define vectors
using namespace std;
int main()
{
   const int NUM_EMPLOYEES = 5;           // Number of employees
   vector<int> hours(NUM_EMPLOYEES);      // A vector of integers
   vector<double> payRate(NUM_EMPLOYEES); // A vector of doubles
   int index;                             // Loop counter
// Input the data.
   cout << "Enter the hours worked by " << NUM_EMPLOYEES;
   cout << " employees and their hourly rates.\n";
   for (index = 0; index < NUM_EMPLOYEES; index++)
   {
      cout << "Hours worked by employee #" << (index + 1);
      cout << ": ";
      cin >> hours[index];
      cout << "Hourly pay rate for employee #";
      cout << (index + 1) << ": ";
      cin >> payRate[index]; /* can you input values in vectors just like the array above?  Why did the programmer use arrays instead of vecors to take in values from the user? What's the advantage of having some vectors defined but seemingly never used in this program? Is that a separate array or the vector with the same name just converted? */
   }
// Display each employee's gross pay.
   cout << "\nHere is the gross pay for each employee:\n";
   cout << fixed << showpoint << setprecision(2);
   for (index = 0; index < NUM_EMPLOYEES; index++)
   {
      double grossPay = hours[index] * payRate[index];
      cout << "Employee #" << (index + 1);
      cout << ": $" << grossPay << endl;
   }
   return 0;
}

What's the difference between the above vector program with the array programs?



https://www.youtube.com/watch?v=SGyutdso6_c

