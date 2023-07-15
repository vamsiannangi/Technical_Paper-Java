#Technical Paper
##Topic

You joined a new project. The project codebase is difficult to manage. Your team lead has asked to study a few concepts and refactor the codebase. Create a report on OOP with code samples.
One of the best possible solutions to the above-mentioned scenario that can help developers to manage the codebase is to implement OOP paradigm.

##Introduction
As per my team lead's instructions, I have studied various concepts and proposed refactoring strategies to improve the codebase. This report focuses on the application of Object-Oriented Programming (OOP) principles in refactoring the project codebase. By adhering to these principles, we aim to enhance code organization, reusability, and maintainability.
##Key Concepts of OOP
###1.Classes and Objects
Classes are blueprints or templates that define the structure and behavior of objects. They encapsulate data (attributes) and functions (methods) related to a specific concept or entity. Objects are instances of classes, representing real-world entities or concepts.
```java
 // Class definition
public class Main {
	
	static String Employee_name;
	static float Employee_salary;

	static void set(String n, float p) {
		Employee_name = n;
		Employee_salary = p;
	}

	static void get() {
		System.out.println("Employee name is: " +Employee_name );
		System.out.println("Employee CTC is: " + Employee_salary);
	}

	public static void main(String args[]) {
		GFG.set("Rathod Avinash", 10000.0f);
		GFG.get();
	}
}


```

###2.Encapsulation

Encapsulation ensures that the internal details of an object are hidden and can only be accessed through well-defined public interfaces. It combines data and methods within a class, protecting the data from external modifications.

```java
class BankAccount {
    private double balance;
    
    public void deposit(double amount) {
        balance += amount;
    }
    
    public double getBalance() {
        return balance;
    }
}

BankAccount account = new BankAccount();
account.deposit(1000);
double balance = account.getBalance();

```
###3.Inheritance

Inheritance allows the creation of new classes (derived classes) based on existing classes (base or parent classes). Derived classes inherit properties and behaviors from their parent classes, promoting code reuse and establishing an "is-a" relationship.
![Image]![Alt text](inheritence.jpg)





```java
class Animal {
    void eat() {
        System.out.println("Animal is eating");
    }
}

class Dog extends Animal {
    void bark() {
        System.out.println("Dog is barking");
    }
}

Dog myDog = new Dog();
myDog.eat(); // Inherited from Animal
myDog.bark();

```

###4.Polymorphism

Polymorphism allows objects of different types to be treated interchangeably through a common interface. It enables methods to be overridden in derived classes, providing different implementations while maintaining a consistent interface.
```java
class Shape {
    void draw() {
        System.out.println("Drawing a shape");
    }
}

class Circle extends Shape {
    @Override
    void draw() {
        System.out.println("Drawing a circle");
    }
}

Shape myShape = new Circle(); // Polymorphic assignment
myShape.draw(); // Calls overridden method in Circle class

```
###5.Abstraction
Abstraction focuses on capturing the essential features and behaviors of a concept while hiding unnecessary implementation details. Abstract classes and interfaces provide common contracts that subclasses adhere to, enabling code reuse and modular design.
```java
abstract class Vehicle {
    abstract void start();
    abstract void stop();
}

class Car extends Vehicle {
    @Override
    void start() {
        System.out.println("Car engine started");
    }
    
    @Override
    void stop() {
        System.out.println("Car engine stopped");
    }
}

Vehicle myVehicle = new Car();
myVehicle.start();
myVehicle.stop();

```




###Conclusion

Object-Oriented Programming provides a powerful set of concepts and principles for designing and developing software systems. By leveraging classes, objects, encapsulation, inheritance, polymorphism, abstraction, and composition, developers can create modular, maintainable, and extensible code. This report presented an overview of these OOP concepts with code samples to demonstrate their usage. By embracing OOP, developers can enhance code organization, promote code reuse, and build robust and scalable applications.


####References
[GeeksForGreeks](https://www.geeksforgeeks.org/object-oriented-programming-oops-concept-in-java/)
[ORACLE](https://docs.oracle.com/javase/tutorial/java/concepts/)
[Inheritance](https://simplesnippets.tech/inheritance-in-java-types-of-inheritance/)
