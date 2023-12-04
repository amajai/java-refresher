# Java Refresher

Are you looking to brush up on your Java skills and solidify your knowledge? You're in the right place! This repository is designed as a comprehensive Java refresher, providing a structured approach to revisiting key Java concepts and features.

## Benefits:
- **Structured Learning Path**: Follow a well-organized learning path that covers fundamental Java concepts and advanced topics.
- **Hands-On Exercises**: Reinforce your understanding through hands-on exercises and coding challenges.
- **Revision Materials**: Access concise revision materials to quickly recap essential Java principles.

Whether you're a Java beginner looking to strengthen your foundation or a seasoned developer aiming to refresh your skills, this repository provides a valuable resource to enhance your Java proficiency.

Let's embark on this Java refresher journey together! Happy coding! 🖥️💡

---

You can customize it further based on the specific content and features of your repository.

## 1. Foundation
Java is a high-level object-oriented language. It developed to not be dependant on a system software or hardware. It comes with a complier where it complies a Java code we write into a byte code which can be run on any system machine. 

Example of Program to print Hello world:
```java
public class Main { // important base code class.
    public static void main(String[] args) { // main method to run code
        System.out.println("This will be printed");
    }
}
```

In Java, every line of code needs to run inside a base class `Main`.

```java
public static void main(String[] args)
```
- `public` - anyone can access it.
- `static` - you can run this method without creating an instance of `Main`. Replace with `class` if its the base class
- `void` - that this method doesn't return anything.
- `main` - method name.
- `String[]` - argument parameter
- `args` - argument
