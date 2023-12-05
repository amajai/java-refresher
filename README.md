# Java Refresher

Are you looking to quickly brush up on your Java skills and solidify your knowledge? You're in the right place! This repository is designed as a comprehensive Java refresher, providing a structured approach to revisiting key Java concepts and features.

Whether you're a Java beginner looking to strengthen your foundation or a seasoned developer aiming to refresh your skills, this repository provides a valuable resource to enhance your Java proficiency.

Let's embark on this Java refresher journey together! Happy coding! 🖥️💡

---

You can customize it further based on the specific content and features of your repository.

## 1. Foundation
Java is a high-level object-oriented language. It was developed to not be dependent on a system software or hardware. It comes with a compiler that complies with the Java code we write into a byte code which can be run on any system machine. 

Example of a Program to print Hello World:
```java
public class Main { // important base code class.
    private String name;
    public static void main(String[] args) { // main method to run code
        System.out.println("This will be printed");
    }
}
```

In Java, every line of code needs to run inside a base class `Main`.

### Function
```java
public static void main(String[] args)
```
- `public` - anyone can access it.
- `private` - only the class itself can access the variable or method.
- `static` - you can run this method without creating an instance of `Main`. Replace with `class` if its the base class
- `void` - that this method doesn't return anything.
- `main` - method name.
- `String[]` - argument parameter (array of strings)
- `args` - argument

## 2. Variables and type

### Primitives in Java:
- boolean - 1 byte
- byte - 1 byte
- int - 4 bytes
- short - 2 bytes
- long - 8 bytes
- float - 4 bytes
- double - 8 bytes
- char - 2 bytes

### Numbers
Declare and assign a variable
```java
int num = 5;
```
Same as
```java
int num;
num = 5;
```
### Char and String
Example of char and string:
```java
char c = 'a';
String s = "Hello World!"; 
```
Concat num with string:
```java
int num = 2;
String s = "I have " + num + " cars";
```
### Boolean
```java
boolean b = false;
boolean c = !false;

int isTrue = 0;
if (isTrue) { // Will passs
}
```
### Type casting
```java
double d = (double) 4.5;
```

## 3. Conditionals
Boolean variables to evaluate conditions.
Example 1:
```java
int a = 4;
if (a == 4) {
    System.out.println("It is true!");
}
```
Example 2:
```java
int a = 1;
int b = 2;
boolean result;
result = a < b; // true
result = a == b; // false
result = a != b; // true
result = a > b || a < b; // true
result = !result; // false
```
### == and equals
```java
String a = new String("Wow");
String b = new String("Wow");
String sameA = a;

boolean r1 = a == b;      // This is false, since a and b are not the same object
boolean r2 = a.equals(b); // This is true, since a and b are logically equals
boolean r3 = a == sameA;  // This is true, since a and sameA are really the same object
```
## 4. Arrays

```java
int[] arr;
arr = new int[10];
System.out.println(arr.length); // 10

arr[0] = 4; // set value

int[] arr = {1, 2, 3, 4, 5}; // assign array
for (int i=0; i < arr.length; i++) {
    System.out.println(arr[i]);
}
```
## 5. Loops
```java
// for loop
for (int i = 0; i < 3; i++) {}

// while loop
while (condition) {}

// Foreach loop
int[] arr = {2, 0, 1, 3};
for (int el : arr) {
    System.out.println(el);
}
```

## 6. Object
```java
class Point {
    int x;
    int y;
}

Point p = new Point();
```

Define constructor:
```java
class Point {
    int x;
    int y;

    Point(int x, int y) {
        this.x = x;
        this.y = y;
    }
}

Point p = new Point(1, 3); \ can add arguments
```

Defining more than one constructor:
```java
class Point {
    int x;
    int y;

    Point() {
        this(0, 0);
    }

    Point(int x, int y) {
        this.x = x;
        this.y = y;
    }

    Point center(Point p) {
        return new Point((x + p.x) / 2, (y + p.y) / 2);
    }
}
```

## 7. Compiling and Running with Arguments
```java
public class Arguments {
    public static void main(String[] args) {
        for (int i = 0; i < args.length; i++) {
            System.out.println(args[i]);
        }
    }
}

javac Arguments.java
java Arguments arg0 arg1 arg2
```

## 8. Inheritance
```java
public class Animal {
    public void sound () ________________
    {                                    |
        System.out.println("");          |
    }                                    |
}                                        |
                                         |---- Polymorphism allows us to perform a single action in different ways
class Dog extends Animal {               |
    public void sound () _______________ |
    {
        System.out.println("Bark!");
    }
}
```

### Overloading
Overloading is when multiple functions with the same name but different parameters
```java
class Mul {
    static int Multiply(int a, int b)
    {
        return a * b;
    }

    static int Multiply(int a, int b, int c)
    {
        return a * b * c;
    }

    static int Multiply(int a, int b, int c, int d)
    {
        return a * b * c * d;
    }
}
```

## 9. Abstract Classes
```java
abstract class Shape {
    int x, y;

    Shape(int initialX, int initialY) {
        x = initialX;
        y = initialY;
    }

    abstract void draw();
}

class Circle extends Shape {
    int radius;

    Circle(int x, int y, int radius) {
        super(x, y); // Invoke the constructor of the superclass (Shape)
        this.radius = radius;
    }

    @Override
    void draw() {
        // Implementation of the draw method specific to Circle
        System.out.println("Drawing a circle at coordinates (" + x + ", " + y + ") with radius " + radius);
    }
}
```
## 10. Interfaces
```java
interface Animal {
    boolean feed(boolean timeToEat);
    void groom();
    void pet();
}

class Tiger implements Animal {
    boolean feed(boolean timeToEat) {
      return true
    }
    void groom() {
    }
    void pet() {
    }
}
```
