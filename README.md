<div align="center">

# The Expensive Expert

**The Expensive Expert**  
is a simple Java console application for tracking incomes and expenses. This project demonstrates **Object-Oriented Programming (OOP)** principles: **Encapsulation, Inheritance, Abstraction, and Polymorphism**.  

</div>

---

## Features

- Add and track incomes.
- Add and track expenses.
- View total savings.
- Display all transactions.
- Demonstrates core OOP concepts clearly.

---

## OOP Principles Demonstrated

### 1️⃣ Encapsulation
Encapsulation hides the internal state of objects and provides controlled access through methods.  

```java
class Expense {
    private String name;
    private double amount;

    public Expense(String name, double amount) { 
        this.name = name; 
        this.amount = amount; 
    }

    public String getName() { return name; }
    public double getAmount() { return amount; }
}
````

Here, `name` and `amount` are private and accessed via getters.

---

### 2️⃣ Inheritance

Inheritance allows classes to reuse fields and methods from a parent class.

```java
class Transaction {
    protected double amount;
    public Transaction(double amount) { this.amount = amount; }
}

class Income extends Transaction {
    public Income(double amount) { super(amount); }
}

class Expense2 extends Transaction {
    public Expense2(double amount) { super(amount); }
}
```

`Income` and `Expense2` inherit behavior from `Transaction`.

---

### 3️⃣ Abstraction

Abstraction hides implementation details and exposes essential features through abstract classes.

```java
abstract class AbstractTransaction {
    protected double amount;
    public AbstractTransaction(double amount) { this.amount = amount; }
    public abstract void display();
}

class IncomeAbs extends AbstractTransaction {
    public IncomeAbs(double amount) { super(amount); }
    public void display() { System.out.println("Income: PHP " + amount); }
}
```

The abstract method `display()` must be implemented by subclasses.

---

### 4️⃣ Polymorphism

Polymorphism allows objects of different types to be treated as the same parent type, while methods behave differently.

```java
List<TransactionPoly> transactions = List.of(
    new IncomePoly(5000),
    new ExpensePoly("Food", 1500)
);

for (TransactionPoly t : transactions) t.display(); // behaves differently based on object type
```

---

## How to Run

1. Clone or copy the Java files.
2. Compile all files:

```bash
javac *.java
```

3. Run the main class:

```bash
java TheExpensiveExpert
```

4. Follow the console menu to manage incomes, expenses, and view savings.

---

## Example Output

```
---- All Transactions ----
Income: PHP 5000
Food - PHP 1500
Transport - PHP 800
Savings: PHP 2700
```

---

<div align="center">

## Authors (Alphabetical by Last Name)

* Justine Ciara Bendong
* John Patrick Bariata
* Aliana Nicole Magsanga

</div>
```

