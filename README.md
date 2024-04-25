# Polymorphism-in-Java

Polymorphism is one of the fundamental concepts in object-oriented programming (OOP) languages like Java. It allows objects of different classes to be treated as objects of a common superclass. This feature enables flexibility and extensibility in code design and promotes code reusability.

## Table of Contents

- [Introduction to Polymorphism](#introduction-to-polymorphism)
- [Types of Polymorphism](#types-of-polymorphism)
  - [Compile-time Polymorphism (Method Overloading)](#compile-time-polymorphism-method-overloading)
  - [Run-time Polymorphism (Method Overriding)](#run-time-polymorphism-method-overriding)
- [Example Code](#example-code)
- [Benefits of Polymorphism](#benefits-of-polymorphism)
- [Conclusion](#conclusion)
- [Further Reading](#further-reading)

## Introduction to Polymorphism

Polymorphism comes from the Greek words "poly" meaning many and "morph" meaning form. In Java, polymorphism refers to the ability of an object to take on multiple forms. This is achieved through inheritance, where subclasses can override or overload methods defined in their superclass.

## Types of Polymorphism

### Compile-time Polymorphism (Method Overloading)

Method overloading allows a class to have multiple methods with the same name but different parameters. The compiler determines which method to call based on the number and type of arguments passed to it at compile time.

### Run-time Polymorphism (Method Overriding)

Method overriding occurs when a subclass provides a specific implementation of a method that is already defined in its superclass. The decision of which method to execute is made at runtime based on the type of object.

## Example Code

```java
// Superclass
class Animal {
    void makeSound() {
        System.out.println("Some sound");
    }
}

// Subclass 1
class Dog extends Animal {
    @Override
    void makeSound() {
        System.out.println("Bark");
    }
}

// Subclass 2
class Cat extends Animal {
    @Override
    void makeSound() {
        System.out.println("Meow");
    }
}

public class Main {
    public static void main(String[] args) {
        Animal animal1 = new Dog();
        Animal animal2 = new Cat();

        animal1.makeSound(); // Output: Bark
        animal2.makeSound(); // Output: Meow
    }
}
