# OOPS concepts

OOPS stands for Object Oriented Programing Structure

## Class

Class is a blueprint.  
Which has `Fields`, `Properties`, `Methods`.

```csharp
public class Customer {
    private string _fullname; // Field

    public string FirstName{get;set;} // Property

    public void Add(){
        // Method
    }
}
```

</br>

## Object

Instance of `class`.

</br>

## Encapsulation

Creating group of related methods, properties and other members as a single object.

</br>

## Inheritance

Ability to derive methods and properties from another class

There are 4 types of Inheritance available:

- **Single**  
  If class is inherited from one base class, it's known as single inheritance.

```csharp
public class A {
}

public class B : A {
}
```

- **Multilevel**  
  If class is inherited from one base class, and that base class is also inherited from another base class, it's known as multilevel inheritance.

```csharp
public class A {
}

public class B : A {
}

public class C : B {
}
```

- **Multiple**  
  If class is inherited from more than one base class, it's known as multiple inheritance.  
  Multiple inheritance is not allowed in C#, java. So interfaces are used insted of classes.  
  Multiple inheritance is allowed in C++.

```csharp
public class A {
}

public class B {
}

public class C : A, B {
}
```

- **Hierarchical**  
  If more than one class is inherited from the base class, it's known as hierarchical inheritance.

```csharp
public class A {
}

public class B : A {
}

public class C : A {
}
```

</br>

## Polymorphism

Declaring same methods but different forms.

Polymorphism can be achived by many techniques:

- **Method overloading** (Compile time polymorphism)  
  Method overloading means declaring methods with same name but different types of argument and numbers of arguments.  
  Whenever an object is bound with their functionality at the compile-time, this is known as the compile-time polymorphism.

```csharp
public class A {
    public int Add(int a, int b){
        return a + b;
    }

    public double Add(double a, double b){
        return a + b;
    }
}
```

- **Method overriding** (Run time polymorphism)(Late binding)  
  Method overriding means override base class method in child class using `override` keyword.  
  Whenever an object is bound with the functionality at run time, this is known as runtime polymorphism.

```csharp
public class A {
    public int Add(int a, int b){
        return a + b;
    }
}

public class B : A {
    public override int Add(int a, int b){
        return a + b + 10;
    }
}

```

  </br>

## Abstraction

Hide everything other than relevant data.
Use access modifiers like `private`, `public`, `protected` for abstraction.
