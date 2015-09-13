# Javascript-Tutorial
Intended to introduce JavaScript to those familiar with Java or other Object Oriented languages. Emphasizes concepts that Purdue SIGART plans to use in our Snake AI.

## Background
 * JavaScript is NOT a compiled language. You simply load an HTML file into a browser that is linked to a JavaScript file, and it executes.
 * You typically don't run JavaScript by itself. It's typically linked to in an HTML file.
 * JavaScript is a client side scripting language.

## Hello World!
You just need one of these lines, no need to even put it in a function. Any code outside of a function will simply be executed when the program loads.
```
window.alert("Hello, World!"); // Creates a pop-up window that says "Hello World!"
document.write("Hello, World!"); // Writes to the HTML document
console.log("Hello, World!"); // Writes to the JavaScript Console
```

## Variables and Numerical Expressions
Unlike Java and some other compiled languages, you do not need to specify the type of variable you are working with in JavaScript. It just figures it out for you.
```
var numStudents = 72; // Example of an int
var minimalWage = 7.5; // Example of a double
var myName = "Bill Gates"; // Example of a string
var type = 'c'; // Actually a string, not a char. There is no primitive char type in JavaScript.
var happy = true; // Example of a boolean variable
```
You can also have constants, like in Java:
```
const PI = 3.14159265;
```
You can also use numerical operations, again, similar to Java:
```
5 + 2      // Results in 7
5 - 2      // Results in 3
5 * 2      // Results in 10
5 / 2      // Results in 2.5. We don't care that 5 and 2 are both integers, JavaScript gives us a double in return.
5 $ 2      // Modulus, results in 1.
```
Boolean operations are also very similar to Java:
```
1 == 1    // equals
1 != 1    // does not equal
1 > 1     // Greater than
1 < 1     // Less than
1 <= 1    // Less than or equal to
1 >= 1    // Greater than or equal to
&&        // Used as the AND operator
||        // Used as the OR operator
!         // Used as the NOT operator
```
## Strings
You can declare strings with either double or single quotations, and you can use quotations inside a string so long as they don't match the ones outside the string:
```
var nameOne = "Steven";
var nameTwo = 'Daniel';
var motto = "Don't be evil";
var passage = '"Hello, Nick," said Harry.';
```
Some operations you can use on strings:
```
var example = "This is a String";
var len = example.length; // Returns the length of a string
var longExample = "Hello " + "World!"; // equals "Hello World!"
var stringPlusNumber = "Size: " + 55; // equals "Size: 55"
var res = example.charAt(0); // gets the 0th character of the string
"Hello!" === "Hello!" // how you compare strings for equallity
```
Escape characters work just like in most other languages, include '\n' for newline and '\t' for tabs.

## Control Flow
Literally nearly identical to Java, except for the for statement:
```
if (condiction) {
  // statements
} else {
  // statements
}

// numbers and strings can be used in switch statements
switch (expression) {
  case item1:
    // stuff
    break;
  case item2:
    // stuff
    break;
  // etc
}

while (condition) {
  // stuff
}

do {
  // stuff
} while (condition);

for (i = 0; i < 10; i++) { // executes 10 times
  // stuff
}
```

## Arrays
Declare arrays just like other variables, and you can print them as you would expect:
```
var people = ["Bill", "Bob", "Sam"]; // This is a variable
console.log(people); // Works as expected
```
Access elements as you would expect:
```
people[0] = "Dan";
var name = people[0];
```
Methods for arrays:
```
var number = people.length; // The length of the people array
var sorted = people.sort(); // Returns a sorted array
people.push("Frank"); // Adds "Frank" to the end of the list
people.splice(3, 1); // Removes the element at index 3. Note that the 1 represents the number of elements to be removed.
```
As a final note, if you want to initialize an empty array, you should use:
```
var points = [];
```
## Functions
Operatres as one would expect. Here is the syntax:
```
function sum(n1, n2) { // A function called "sum" that takes two params and returns their sum.
  return n1 + n2;
}
```

## Objects (Defining using Functions, or Constructors)
Here is an example of a declaration:
```
function President (firstName, lastName, number) {
  this.firstName = firstName;
  this.lastName = lastName;
  this.number = number;
  this.getName = function() {
    return this.firstName + " " + this.lastName;
  };
  return this;
}
```
And to use it...
```
var underwood = new President("Frank", "Underwood", 46);
var name = underwood.getName();
```
To access object parameters, either for obtaining or changing their values, use:
```
object.variableName OR object["variableName"]
// for example...
var name = president.firstName + " " + president.lastName;
```

## Objects (Defining using Object Literals)
Here is a definition of an object:
```
var president = {
  firstName:"Frank",
  lastName:"Underwood",
  number:46
}
```
To define a method, use:
```
var president = {
  firstName:"Frank",
  lastName:"Underwood",
  number:46
  getName: function() {
    return this.firstName + " " + this.lastName;
  }
}
```
And to call it...
```
var name = president.getName();
```
