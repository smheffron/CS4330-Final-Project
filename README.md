# CS4330-Final-Project
Shelby Heffron, Ethan Schutzenhofer, Clayton Cornett, Matt Gambino  
  
## Java vs. Swift

4330 Language Comparison

## Language Purpose

#### Java
* Java was intended to be written for the code to be used and ran on any device
* Response to C and C++, wanted to make coding large projects easier by implementing an object oriented style. 
* Java places an emphasis on reliability and developer friendly features over speed. (Ex. features like the Garbage collector).

#### Swift
* Swift was created to improve object oriented programming for the creation of iOS and desktop apps
* Improving safety on unexpected behavior in code played a large role in the creation of Swift (Ex. Optionals)
* Created to replace Objective C for iOS development and C based languages
* Swift provides easier to read code with a more simple and logical syntax 

## Unique features of the language

#### Java
* Garbage collector - runs in the background to free memory that no longer has any use (references)
* JVM - Java Virtual Machine, allows code to be run on any machine that has the JVM

#### Swift
* Optionals - a type that can be something or be null. Prevents unintended crashing of your program due to null references
* Syntax features that make it easier to read (Example: no semicolons to end lines and named parameters)  
 
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
* Closures in Swift are self contained blocks of functionality that can be passed around (Similar to lambdas in java)

## Name Spaces

#### Java
* Uses packages which are a collection of classes.
* You can use “import” in code to use other classes from another package.
```Java
import java.shape.Rectangle;
import java.io.File;
import java.io.FileReader;
```
#### Swift
* Uses Modules which is a single unit of code distribution.
* You can use modules by using the keyword “import”.
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
* No destructors in Java, taken care of by garbage collection when object has no references.

#### Swift

* Similar to Java, uses fields and methods
* Uses class name for creating new instances, does not use a “new” keyword
* To initialize something in a class you can use the init keyword
* Deinit is automatically called, it is used to run code when an object is destroyed

```Swift
class student {

  var studentName : String
  var age : Int
  var grade : Int
  }
  
let studrecord = student()
```

## Instance reference name in data type (class)

#### Java
* Uses the “this” keyword
```Java
void randomFunction( String name, int age){
  this.name = name;
  this.age = age;
}
```
#### Swift
* Uses the “self” keyword

```Swift
init(name : String, age : Int){
  self.name = name
  self.age = age
}
```
## Properties

#### Java
* Have to write your own getters and setters
* Does not have computed properties
```Java
private String name;

public void setName(String name) {
    this.name = name;
}
public String getName() {
    return name;
}
```
#### Swift
* Has a defined get and set method
* Has backing variables
* Supports computed properties
```Swift
get {
let age : Int
return age
}
set(age){
 self.age = age
}
//Computed properties
struct Point {
    var x = 0.0, y = 0.0
}

struct Size {
    var width = 0.0, height = 0.0
}

struct Rect {
    var origin = Point()
    var size = Size()
    var center: Point {
        get {
            let centerX = origin.x + (size.width / 2)
            let centerY = origin.y + (size.height / 2)
            return Point(x: centerX, y: centerY)
        }
        set(newCenter) {
            origin.x = newCenter.x - (size.width / 2)
            origin.y = newCenter.y - (size.height / 2)
        }
    }
}

var square = Rect(origin: Point(x: 0.0, y: 0.0),
                  size: Size(width: 10.0, height: 10.0))

let initialSquareCenter = square.center
square.center = Point(x: 15.0, y: 15.0)

print("square.origin is now at (\(square.origin.x), \(square.origin.y))")
// Prints "square.origin is now at (10.0, 10.0)"
```
## Interfaces / protocols

#### Java
* Supports interfaces, implements as many as it wants
* Can only contain a method signature and fields
* Use the keyword implements to implement an interface
```Java
public class MyController implements MyInterface{
}
```
#### Swift
* Support protocols
* Can specify properties that must be implemented, you can use more than one protocol, and must be used in <>
* Use the : to implement a protocol
```Swift
protocol MyProtocol{
// blah blah
}

struct Structure : MyProtocol{

}
```
## Inheritance / extension

#### Java
* Uses extends keyword to extend a superclass
* Subclasses can use some of the superclass functionality
* Can only extend one class
```Java
public class MountainBike extends Bicycle {
// mountainbike code
}
```
#### Swift
* Uses a : to extend another class
* Only extend one class
* Subclasses can use some of the superclass functionality
```Swift
extension SomeType{
// some code
}
```
## Reflection

#### Java
* Can obtain the names of all its members, and examine and manipulate a class
* You can see the methods and fields of an unknown type to determine its type
```Java
Method[] methods = MyObject.class.getMethods();

for(Method method : methods){
    System.out.println("method = " + method.getName());
}
```
#### Swift
* Allows read only access to properties, however you cannot access computed properties using reflection
```Swift
let booClassMirror = Mirror(reflectiong: Book.self)
print(bookCLassMirror.children.count)
```
## Memory Management

#### Java
* The garbage collector handles memory management for Java by adding objects to a heap when the JVM is started. 
* When the heap becomes full objects are collected when they have no references to them

#### Swift
* Swift uses automatic reference counting to keep track of the number of references to an object
When the reference count reaches zero, the object is destroyed

## Comparisons of references and values

#### Java
* Use .equals() to compare values
* Use == to compare references
```Java
String foo = new String("abc");
String bar = new String("abc");

if(foo==bar)
// False (The objects are not the same)

bar = foo;

if(foo==bar)
// True (Now the objects are the same)
```

#### Swift
* Use == to compare values
* Uses === to see if two objects have the same reference

## Null/nil references

#### Java
* Uses Null
* Does not have any built in features to handle null references

#### Swift
* Uses nil
* Has optionals and unwrapping to prevent/deal with null values

## Errors and exception handling
#### Java
* Uses try and catch to catch exceptions and uses throw to throw the exception
* Swift
* Errors are represented by values of types that can conform to the Error protocol 
```Java 
enum VendingMachineError: Error {
   case invalidSelection
   case insufficientFunds(coinsNeeded: Int)
   case outOfStock
}
```
## Lambda expressions, closures, or functions as types

#### Java
* Uses lambda as a first step towards functional programming
* Uses anonymous inner classes

#### Swift
* Uses closures - self contained blocks of functionality that can be passed around
* Has functions as types which allows you to pass functions as parameters to other functions and to return functions

## Implementation of listeners and event handlers
#### Java
* Lambdas are used as listener which are tied into the UI
* When a listener event goes off it will go through the chain and trigger the proper event handler

#### Swift
* IBOutlet is one specific notation used to connect the UI to the code
* Responders are similar to handlers in Java

## Singleton

#### Java
* Constructor is private, and you make a static method that has your return type object of a singleton class
* Not all Java Singletons are thread safe because the instance can be accessed through multiple threads.
* Can be lazily instantiated
  * If an instance already exist then it returns the reference object if not the object will only be created when needed.

#### Swift
* Make the initializer private and make a static constant property which gives other objects access to the singleton object.
* It is possible to make swift singletons thread safe
* Use the keyword ‘Lazy’ to lazily instantiate 

## Procedural Programming

#### Java
* Java is strictly an OO-language and can only achieve procedural-like programming is by putting all the code in Main

#### Swift 
* Swift is a multi-paradigm language designed for both OO and procedural programming

## Functional Programming

#### Java
* In Java 8 functions became first class which means they can be stored as objects, passed as arguments for other functions, and can be returned

#### Swift
* Swift can do Functional Programming and swift also treats functions as first class

## Multithreading

#### Java
* In Java threads can be created by implementing runnable or extending the Thread class. The UI is not thread safe. 

#### Swift 
* Swift’s threading is based off the way Objective-C handled threads.
* Uses the NS option queue in order to execute NS operations in parallel
  

