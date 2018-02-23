# Java CheatSheet

## Starting Point
```java
// class name MUST be that same as the file name
// For example: FileName.java

public class FileName {
    public static void main(String[] args) {
        // Your code here.
    }
}
```


## Variables
```java
int x = -3;
double y = 5.6;
String n = "Jim";
char c = 'G';
boolean isAlive = true;
```

## Printing
```java
System.out.print("Hello");      
System.out.println("Hello");    // new line after "Hello"
int x = 3;
System.out.println("X is " + x + "."); // concatenation
```

## User Input
```java
import java.util.Scanner;
Scanner input = new Scanner(System.in);
int x = Integer.parseInt(input.nextLine());
double y = Double.parseDouble(input.nextLine());
int z = input.nextInt();
String n = input.next();
```

## Boolean Logic
### Comparison Operators
```java
x > 4   // x greater than 4
x < 10  // x less than 10
x >= 5  // x greater than or equal to 5
x <= 7  // x less than or equal to 7
x == 3  // x equal to 3
x != 2  // x not equal to 2

// For Strings, dont use ==
// use .equals() method.
String n = "Hello";
n.equals("Hello");
```

### Compound Boolean
```java
// Operators
&&      // AND
||      // OR
!       // NOT
```

```java
// Usage
x > 0 && x < 10     // x greater than 0 AND x less than 10
x == 5 || x == 7    // x equal to 5 OR x equal to 7
```

## If Statements
```java
if (x > 400) {
    System.out.println("X is positive and greater than 400.")
} else if (x > 0) {
    System.out.println("X is a positive number.")
} else {
    System.out.println("X is not positive.")
}
```

## Nested if
```java
if (name.equals("Jim")) {
    System.out.println("I once knew a Jim! Smith was his name.");
    if (lastName.equals("Smith")) {
        System.out.println("Jim Smith! I knew it was you!");
    }
}
```

## While loop
```java
int x = 0;
while (x < 10) {
    System.out.println(x);
    x += 1;
}
```

## Do while
```java
do {
    System.out.println("Enter password");
    String password = input.nextLine();
} while (password != "The Correct Password");
```

## For loop
```java
for (int x = 0; x < 10; x += 1) {
    System.out.println(x);
}
```

