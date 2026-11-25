## 1 Differnce between compiled and interpreted language
   -compiled language-it is a language that has been translated to object code as a whole using the compilers. An example is C,C++.
   -Interpreted language -It is a language that has been translated to object code line by line  using an interpreter before execution. An example is the JavaScript and Python.
## 2 Describe what happens when you type gcc main.c -o mainand then ./main. and when you type node app.js.
  -When you type gcc main.c -o;then GCC being a compiler will compile the whole source code as whole and create another file that is the main that contains the object code that is mainly understable to the computer only.Similarly when you type ./main its like telling the computer to run the machine code.
  -When i type node app.js the the node.js will reads the content of my app.js file and run it line by line to produce an output
  -The main file that is created by the gcc is a compiled source code and in machine form.
  -The main file can be openned in my editor but i cannot understand what it mean but it is understable by the machine.
## 3 The meaning of JIT and why it makes JavaScript faster
 -JIT(Just-In-T)-it is used to translate code such as bytecode,intermediate language into machone code while the program is running.
 -it makes JavaScript faster by compiling frequently executed code into machine code at runtime,allowing the CPU to execute it directly instead of interpreting it line by line. 
## 4 Difference betweeen statically typed language and dynamically typed language.and when the type error is found.
 -In statically typed languages the variable types are checked before the program is executed. Therefore the errrors are found while you write the code.
 -In dynamically typed language the varriable types are checked during execution. The type error are found when the code runs.
##  5 "compiled" and "statically typed".Are two seperate ideas.Is every compiled language statically typed? give one example that prove your answer.
 -Not every compiled language is Statically typed.
 -compilation translate the source code into another form before or during execution while static typing checks variable type at compiling time rather than runtime.
 -Compiled: Julia compiles code to native machine code using just-in-time (JIT) compilation.
 Dynamically typed: Variable types are evaluated at runtime, allowing values and type dispatch to be resolved dynamically during execution.
## 6. Table

| Language | Compiled or interpreted? | Static or dynamic typing? |
| --- | --- | --- |
| C | Compiled | Static |
| Java | Compiled | Static |
| Python | Interpreted | Dynamic |
| JavaScript | Interpreted | Dynamic |
| TypeScript | Compiled | Static |
| Go | Compiled | Static |
| PHP | Interpreted | Dynamic |
## PART B1
## 1 Copy error message and say which line caused it
 -Type 'number' is not assignable to type 'string'.ts(2322)
let username: string
 -it has been caused by line 2
## 2 We never wrote : string anywhere. How did TypeScript know userName is a string?(Hint: look up "type inference".)
 -It used the type inference, a feature where the compiler automatically determines the type of a variable,return value,based on how it is initialized or used—even when you don't write an explicit type annotation like string.
## 3. Look in the folder after running tsc .Was an app.js file created? Open it. Are the types still there
 -Yes, it is still created and the types are still there with no error.
## 4 Run the same three lines with node. What is printed, why doesn't JavaScript complain?
 -JavaScript is dynamically typed hence the variable type are checked during execution.
## PART B2
## 1. Explain each error in your own words. Hint: in C, what is the difference between 'V' and "V"?
 -Double quotation on the char variable.The double quotes are used to initialize a string.
 -Passing argument 1 of printf makes pointer from an integer-The printf(username)must be  format string not a raw char value as  printf(username).Passing it like that makes the compiler treat the 
 -'V'-It is a character since it has single quotation marks
  -"V"-It is a string it has double qoutation marks
## 2 . gcc did not complain about userName= 1  . Why not? Hint: what kind of value does char really store? 
 -The datatype char is used to store single characters.It also chaecks the variable at execution time.
## 3. Fix the program so it compiles and prints v.Then change it so that it stores and print the full name Valentine.
 #include<stdio.h>
 int main()
 {
 char userName[]="Valentine";
 printf("%s",userName);
 return 0;}
## 4. Were these errors found before the program ran, or while it ran? Did a main program file get created?
 -The errors were found while the program run.
 -The main file was not created.
  ## PART B3-JAVASCRIPT
## 1. What does each typeof print? 
 -let userName = "Valentine"
 console.log(typeof userName)-It prints string because the username 'Valentine' is written in double quotes.
 userName = 1
console.log(typeof userName)-It prints a number 
## What does this tell you about JavaScript's typing?
 -It is a dynamically typed language therefore it only checks the varianble type at run-time.
## 2. What error does pI = 12444 throw? Is it a type error like in B1, or a different kind of rule?
 -It throws a TypeError
 -A constant variable cannot be redeclared.
## 3. In one sentence, compare when the mistake is caught in B1, B2 and B3
 -In B1 and B2 the mistakes are realised before the program runs at compiling time.
 -In B3 the mistakes are realised at run-time or execution time.
## PART C— Variables and Data Types (15 points)
  ## 2 . In class we covered five primitive types: string, number, boolean, null and undefined.JavaScript has seven. Find the other two, then write one example of each.
 -Symbol-used to represent a unique identifier.
   e.g const userId=symbol("id");
 -BigInt- used to store and operate larger whole numbers.
   e.g const hugeNumber=4955555553322463737;

## 3. Predict what typeof returns for each value, then log it:   
 -"hello"- String
 -42-Number
 -3.14-Number
 -true-Boolean
 null-Object
 undefined-undefined
 ## One answer is surprising. Which one, and why does JavaScript do that?
 -null; It returns an object which is a bug from the very first version of JavaScript
## 4  We wrote let age = null and let cart = undefined  in class. Explain the difference between null and undefined. When would you use each one?
 -Null is an intentional assignment representing no value.
   -It is used when you want to intentionally clear a value.
 -Undefined is means that the varriable is declared but not assigned a value.
   -it is used when a value has not been initialized.
## 5. What is the value of someVariable after let someVariable;? Log it to check.
 -Undefined
## PART E5
## FILL THE TABLE
|Boy   |girl   |Rule 1 |Rule 2 |Rule 3| Rule 4|

|-----|---------|------|-------|-------|------|
| true  | true   |true  |true  |false  |false  |
|true   | false  |false |true  |true   |false   |
|false  |true    |false |true  |false  |false   |
|false  |false   |false |false |false  |true   |

