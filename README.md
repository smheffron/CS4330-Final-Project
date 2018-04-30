# CS4330-Final-Project
Shelby Heffron, Ethan Schutzenhofer, Clayton Cornett, Matt Gambino  
  
## Java vs. Swift

4330 Language Comparison

## Language Purpose

#### Java
* It was intended to be written for the code to be used on any device
* Response to C and C++, wanted to make coding easier by making it object oriented and run on any platform. Emphasis on reliability over speed. (Ex. features like the Garbage collector).
* It was made to improve/replace with C and C++, it is more developer friendly and easier to manage large programs

#### Swift
* Created to improve object oriented programming for the creation of IOS apps and also desktop apps
* Improve safety on unexpected behavior in code (Ex. Optionals)
* Created to replace Objective C for IOS development and C based languages. Also adds easier to read code with more simple syntax 

## Unique features of the language

#### Java
* Garbage collector - runs in the background to get rid of memory that no longer has use
* JVM - Java virtual machine, allows code to be run on any machine that has the JVM

#### Swift
* Optionals - a type that can be something or be null. Prevents unintended crashing of your program
* Syntax features that make it easier to read (Example: no semicolons to end lines)  
 
```Swift
func greet(person: String) -> String {
   let greeting = "Hello, " + person + "!"
   return greeting
}

print(greet(person: "Anna"))
// Prints "Hello, Anna!"
print(greet(person: "Brian"))
// Prints "Hello, Brian!"
```
Closures - self contained blocks of functionality that can be passed around (Similar to lambdas in java)

## Name Spaces

#### Java
Uses packages which are a collection of classes
You can use “import” in code to use other classes from another package
```Java
import java.shape.Rectangle;
import java.io.File;
import java.io.FileReader;
```
#### Swift
Uses Modules which is a single unit of code distribution
You can use modules by using the keyword “import”
```Swift
import UIKit
```

## Types

#### Java
* 8 primitive types
  * btye, short, int, long, float, double, boolean, char
* Reference/class types (Ex. String, Integer)

```Java
byte bite = 12;
short shrt = 30,000;
int i = 135;
long loong = 10,000,000,000,000;
double doubldouble = 1.234567;
float yourboat = 1.234;
boolean waterIsWet = true;
char c = 'c';
String s = "Ethan is Awesome";
Integer num = new Interger();
```

#### Swift
* Supports the same 8 primitive types
* Has tuples - a group of different values represented as one
* Dictionary types - key values pairs
* Optional type - a variable that can be something or null
* Value types - Structures and Enumerations

```Swift
let bite = 12;
var tuple = ("Ethan", 20)
optional : Int? = 2
```
## Classes

#### Java 
* Has fields and methods, can use instance variable or class variables (Static). Can have modifiers such as public, private, static, final, abstract. 
* Uses constructor that is of the same name as the name of the class. Initial letters should be capitalized. Called using the “new” keyword”. 
* The information sent to the constructor is used to set the fields of the class
```Java
public Actor(String first, String last)
{
    firstName = first;
    lastName = last;
}
```
No destructors in Java, taken care of by garbage collection when object has no references

#### Swift


