# **Java basics**
![[Pasted image 20260918082454.png|444]]
Java source-code file are created using any text editor or Integrated Development Environment (IDE). The source file ends with the extension ==.java== and have the same exact name as the public class name. The source file for the source-code (in the image) is ==HelloWorld.java==, since the public class name is ==HelloWorld== and must be saved inside **C:\Java\bin** directory
![[Pasted image 20260918082925.png]]
From the command window, the java code HelloWorld.java is compiled by java compiler ==javac==,
and if there aren’t any syntax errors, the compiler generates bytecode file with .class extension, and this file is executed using the java command
*On windows:*
![[Pasted image 20260918084844.png|385]]
`javac HelloWorld.java` - <u>javac</u> compiles the source code, <u>HelloWorld.java</u>
`dir HelloWorld`
*On linux (mint):* 
`sudo apt install openjdk-17-jdk-headless`
![[Pasted image 20260918085940.png|394]]
![[Pasted image 20260918090002.png]]

The *Java* language is a high-level language, while *Java bytecode* is a low-level language which is similar to machine instructions but is architecture neutral and can run on any platform and operating system that has *Java Virtual Machine (JVM)*, which is an interpreter that translate the ==individual instructions== in the bytecode into the target machine language code one at a time ==rather than the whole program==
![[Pasted image 20260918090349.png]]

# **Data Types**
**Variables** are containers for storing data values
*Syntax:*
`type variable = value;`
*Examples:*
`String name = "Leo";` → creates a string variable named ==name== and assigns it the value =="Leo"==
`int myNum = 30;` → creates an integer variable named ==myNum== and assigns it the value ==30==

**Java data types**
- *Primitive data types* - includes <u>byte, short, int, long, float, double, boolean,</u> and <u>char</u>
	- specifies the size and type of variable values, no additional methods

| data type  | size    | description                                                                        | examples                            |
| ---------- | ------- | ---------------------------------------------------------------------------------- | ----------------------------------- |
| *byte*     | 1 byte  | whole nums *-128* to *127*                                                         | `byte myNum = 100;`                 |
| *short*    | 2 bytes | whole nums from *-32,768* <br>to *32,767*                                          | `short myNum = 5000;`               |
| *int*      | 4 bytes | whole nums from<br>*-2,147,483,648* <br>to *2,147,483,647*                         | `int myNum = 100000;`               |
| *long*     | 8 bytes | whole nums from<br>*-9,223,372,036,854,775,808* <br>to *9,223,372,036,854,775,807* | `long myNum = 15000000000L;`        |
| *float*    | 4 bytes | fractional nums, *6* to *7* <br>decimal digits                                     | `float myNum = 5.75f;`              |
| *double*   | 8 bytes | fractional nums, *15* decimal <br>digits                                           | `double myNum = 19.99d`             |
| *boolean*  | 1 bit   | true (1) or false (0)                                                              | `boolean isJavaFun = true`          |
| *char*     | 2 bytes | single character/letter                                                            | `char myInitial = 'M'`              |
| *String* * |         | a sequence of characters                                                           | `String greeting = "Hello World!";` |
`* not primitive`
- *Non-primitive data types* - such as <u>String, Arrays,</u> and <u>Classes</u>
	- *Reference variables* are created using defined constructors of the classes. They are used to access <u>objects</u>
	- These variables are declared to be of a specific type that can't be changed
	- Class objects, and various type of array variables come under reference data type
	- Default value of any reference variable is <u>null</u>
	- A reference variable can be used to refer to any object of the declared type/compatible type: `Animal animal = new Animal("Bird");`

**JAVA LITERAL**
- A literal is a source code representation of a fixed value
- They are represented directly in the code without any computation
- Literals can be assigned to any primitive type variable
- For example: `byte a = 68; char a='A`
*Prefix 0* is used to indicate octal and prefix *0x* indicates hexidecimal
```
// 100 in base 10
int decimal = 100;

// 100 in base 8
int octal = 0144; //the 0 at the start indicates octal

// 100 in base 16
int hexa = 0x64; //the 0x at the start indicates hexadecimal
```
*String literals* in Java are specified by enclosing a sequence of chars between a double quotes
```
//regular string
"Hello World!"

// \n indicates a new line
"two\nlines"

// \" indicates that the following double quote isn't enclosing the 
// literal
"\"This is in quotes\""
```
*String & char* types of literals can contain any Unicode characters
```
// \u indicates that the numbers are representing a Unicode char
char a = '\u0001';
String a = "\u001";
```
**Special escape sequences** for String and char literals

| notation | character represented                |
| -------- | ------------------------------------ |
| *\n*     | newline 0x0a                         |
| *\r*     | carriage return 0x0d                 |
| *\f*     | formfeed 0x0c                        |
| *\b*     | backspace 0x08                       |
| *\s*     | space 0x20                           |
| *\t*     | tab                                  |
| *`\"`*   | double quote                         |
| `\'`     | single quote                         |
| `\\`     | backslash                            |
| *\ddd*   | <u>octal</u> char ddd                |
| *\uxxxx* | <u>hexidecimal</u> UNICODE char xxxx |
**JAVA VARIABLE/IDENTIFIER**
*Identifiers* are the names of variables, methods, clsses, packages, and interfaces
*Rules in naming a variable/identifier:*
1. must begin with a
	- letter of the alphabet
	- `_` (discouraged)
	- `$` (discouraged)
2. after the first character, can contain
	- letters
	- digits 0-9
	- <u>NO</u> spaces or special characters
3. can be any length, but don't make it too long
4. uppercase ≠lowercase
	- ALL UPPERCASE are used for <u>constants</u>
	- use camelCase
# **System.Out**
<u>print()</u> is a method in Java used to display text on the console
**System.out.print()**
 - accepts a single value of any primitive or reference data types
 - after it prints, the <u>cursor</u> remains at the end of the text in the console
 *Example:*
 ```
 class MyFirstPrint {
	public static void main(String[] args) {
		System.out.print("Hello");
		System.out.print("World");
	}
 }
 ```
 output: `HelloWorld`
**System.out.println()**
- <u>println()</u> is also used to display text
- after it prints, the <u>cursor</u> goes to the start of the next line in the console
*Example:*
 ```
 class MyFirstPrint {
	public static void main(String[] args) {
		System.out.println("Hello");
		System.out.println("World");
	}
 }
 ```
 output:
 `Hello`
 `World`
# **Scanner**
For the program to read data, you have to import <u>java.util.Scanner</u> at the top of the class file: `import java.util.Scanner;`, wherein <u>import</u> is a keyword that declares a Java library class to be used
```
Scanner sc = new Scanner(System.in);
// declare the object and name it as sc
// initialize with predifined standard input obj
```
To read values of a certain data type:
- nextBoolean()
- nextByte()
- nextDouble()
- nextFloat()
- nextInt()
- nextLine()
- nextLong()
- nextShort()
- next().charAt(0)
*Syntax:*
`variable name = className.nextType()`
```
// imports scanner
import java.util.Scanner;

public class ScannerExample {
	public static void main(String[] args) {
		// declares scanner object sc
		Scanner sc = new Scanner(System.in);
		
		// string in
		String fullname = sc.nextLine();
		
		// number in
		int yearOfBirth = sc.nextInt();
		long mobileNo = sc.nextLong();
		float balance = sc.nextFloat();
		double gpa = sc.nextDouble();
		
		// bool in
		boolean enroll = sc.nextBoolean();
		
		// theres more code in the lg but im not
		// typing allat
	}
}
```
# **Control Structures**
**if-then**
*Syntax:*
```
if (expression) { 
	// then statement(s)
}
```
![[Pasted image 20260918110300.png]]
**if-then-else**
*Syntax:*
```
if (expression) {
	// then statement(s)
} else {
	// then statement(s)
}
```
![[Pasted image 20260918110508.png]]
**if-then-if-then-else**
*Syntax:*
```
if (expression) {
	// then statement(s)
} else if (expression2) {
	// then statement(s)
}
… // another possible else-if bock
} else {
	// then statement(s)
}
```
**switch statement**
*Syntax:*
```
switch (variable/expression) {
	case value1:
		// statement(s) of case1
		break;
	case value2:
		// statement(s) of case2
		break;
	… // another possible case
	default:
		// default statement(s)
}
```
![[Pasted image 20260918111031.png|372]]
# **String Methods**
There are 2 ways to create a String in Java
1. String literal - `String str2 = "Welcome";` (preferred)
2. Using new keyword - `String str1 = new String("Welcome")`

| method               | description                                                                                     |
| -------------------- | ----------------------------------------------------------------------------------------------- |
| *equals()*           | compares two strings<br>returns <u>true</u> if they match<br>returns <u>false</u> if not<br>A≠a |
| *equalsIgnoreCase()* | compares two strings ignoring<br>case, A = a                                                    |
| *toUpperCase()*      | converts a string to <u>UPPERCASE</u>,<br>a → A                                                 |
| *toLowerCase()*      | converts a string to <u>lowercase</u>,<br>A → a                                                 |
# **Loop Statements**
**while statement**
*Syntax:*
```
while (expression) {
	// code inside the body of the loop
}
```
![[Pasted image 20260918113314.png|344]]
**do while statement**
*Syntax:*
```
do {
	// code inside the body of the loop
} while (expression);
```
![[Pasted image 20260918113448.png|250]]
**for statement**
*Syntax:*
```
for (initialization; expression; increment) {
	// code inside the body of the loop
}
```
![[Pasted image 20260918113653.png|354]]
<u>break</u> example: (stops the loop)
```
class ForLoopWithBreak {
	public static void main(String[] args) {
		for (int i = 0; i < 10; i++) {
			// if the value of i is 5, the loop terminates
			if (i == 5) {
				break;
			}
			System.out.println(i);
		}
	}
}
```
output:
```
1
2
3
4
```
<u>continue</u> example: (skips the current iteration of a loop and moves to the end of the loop)
```
class ForLoopWithContinue {
	public static void main(String[] args) {
		for (int i = 0; i < 10; i++) {
			// if the value of i is between 2 and 8, continue executes
			if (i > 2 && i < 8) {
				continue;
			}
			System.out.println(i);
		}
	}
}
```
output:
```
1
2
8
9
10
```
# **Arrays**
*Declaring an array variable:*
`elementType arrayRefVar[] = new elementType[arraySize];` or
`elementType[] arrayRefVar = new elementType[arraySize];`
Example:
`double[] myList = new double[5];`
- declares an array variable ==myList==
- creates an array of 5 elements of ==double== type
- assigns its reference to ==myList==

The following for loop assigns **0** to **myList[0]**, **1** to **myList[1]**, etc.
```
for (int i=0; i < myList.length; i++) {
	myList[i] = i;
}
```

| for loop i     | array element = value |
| -------------- | --------------------- |
| when **i = 0** | myList[0] = 0         |
| when **i = 1** | myList[1] = 1         |
| when **i = 2** | myList[2] = 2         |
| when **i = 3** | myList[3] = 3         |
| when **i = 4** | myList[4] = 4         |
**Array Initializers**
An array initializer combines the ==declaration==, ==creation==, and ==initialization== of an array in one statement using:
`elementType[] arrayRefVar = {value0, value1, ... , valueN};`
Example:
`double[] myList = {0.2, 0.4, 0.6, 0.8, 0.10};`

| array element | element value |
| ------------- | ------------- |
| **myList[0]** | 0.2           |
| **myList[1]** | 0.4           |
| **myLIst[2]** | 0.6           |
| **myList[3]** | 0.8           |
| **myList[4]** | 0.10          |
**Processing Arrays**
*Asking the user to enter 5 values and store it in **gradeList** reference variable:*
```
public static void main(String[] args) {
	Scanner keyboard = new Scanner(System.in); //scanner class
	double[] gradeList = new double[5]; //declares and creates the array
	   
    System.out.println("Enter " + gradeList.length + " values: \n");
	   for (int i=0; i < gradeList.length; i++) {
		   System.out.print("gradeList[" + i + "]: ");
		   gradeList[i] = keyboard.nextDouble();
	   }
}
```   
*Displaying array*
```
System.out.println("Entered values in the gradeList: ");
for (int i=0; i < gradeList.length; i++) {
	System.out.println("gradeList[" + i + "]: " + gradeList[i]);
}
```
## **Multi-dimensional Arrays**
- A multi-dimensional array is an array containing one or more arrays
- A array is nothing but an array of arrays
- Can be defined in simple words as array of arrays. Data in multidimensional arrays are stored in tabular form (in row major order)
*Syntax:*
`data_type[1st dimension][2nd dimension][]...[Nth dimension] array_name = new data_type[size1][size2]...[sizeN]`
Example: 
```
//2D array with 10 rows and 20 columns
int[][] twoD_arr = new int[10][20];

//3D array with 10 rows, 20 columns, and 30 somethings
int[][][] threeD_arr = new int[10][20][30];
```
**2D array**
*Representation of 2D array in Tabular Format:* 3 rows and 3 columns

|         | Column 0 | Column 1 | Column 2 |
| ------- | -------- | -------- | -------- |
| *Row 0* | x[0][0]  | x[0][1]  | x[0][2]  |
| *Row 1* | x[1][0]  | x[1][1]  | x[1][2]  |
| *Row 2* | x[2][0]  | x[2][1]  | x[2][2]  |
*Indirect Method of Declaration:*
Declaration Syntax:
`data_type[][] array_name = new data_type[x][y];`
Example:
`int[][] arr = new int[10][20];`

Initialization Syntax:
`array_name[row_index][column_index] = value;`
Example:
`arr[0][0] = 1;`
*Direct Method of Declaration:*
Syntax:
`data_type[][] array_name = {{row 1}, {row 2}};`
Example:
`int[][] myNumbers = {{10, 20, 30}, {11, 21, 31}};`
*Accessing a 2D array*
```
int[][] myNumbers = { {1, 2, 3, 4}, {5, 6, 7} };
int x = myNumbers[1][2];
System.out.println(x); // Outputs 7
```
==myNumbers== in Tabular Representation:

|                   | Column 0 | Column 1 | Column 2 | Column 3 |
| ----------------- | -------- | -------- | -------- | -------- |
| *Row 0* (array 1) | 1        | 2        | 3        | 4        |
| *Row 1* (array 2) | 5        | 6        | 7        | null     |
`arr[x][y]` where `x` is the row index and `y` is the column index