
# Access Modifiers in TypeScript OOP

Introduction

Access Modifiers are an important part of Object-Oriented Programming (OOP) in TypeScript. They control how we can access the properties and methods of a class. TypeScript provides three main access modifiers: public, private, and protected. TypeScript also provides the readonly keyword, which prevents a property from being reassigned after it has been initialized.

Detailed Body

1.Public

The public modifier allows us to access a property or method from anywhere. It is the default modifier in TypeScript.

Example:


class Student {
    public name: string = "Mehedi";
}

const student = new Student();
console.log(student.name);


Here, we can access the name property from outside the class because it is public.

2.Private

The private modifier allows us to access a property only inside its own class. We cannot directly access it from outside the class.


class Account {
    private balance: number = 5000;
}


Here, the balance property is private, so it cannot be accessed directly outside the Account class.

3.Protected

The protected modifier allows access inside the same class and its child classes. It cannot be accessed directly from outside the class.


class Employee {
    protected name: string = "Rakib";
}

class Manager extends Employee {
    showName(): string {
        return this.name;
    }
}


Here, the Manager class can access the name property because it extends the Employee class.

4.Readonly

The readonly keyword prevents a property from being reassigned after initialization. We can assign its value when declaring it or inside the constructor.


class Product {
    readonly id: number = 101;
}


Here, we cannot assign a new value to the id property after initialization.

 Conclusion

In conclusion, access modifiers help us control access to class properties and methods. Public, private, and protected define where we can access class members. Readonly helps prevent properties from being reassigned. Using these features makes our code more organized and easier to manage.