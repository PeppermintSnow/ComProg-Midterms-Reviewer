# ComProg1 Reviewer

## Data Types
- `int`
  - A  **whole number** consisting of an optional sign (+ or -) followed by a sequence of digits.
  - Often used for **loops and conditional statements**.
  - `int x = 9;`
- `float`
  - Consists of an optional sign (+ or -), followed by one or more digits, a decimal point and/or one or more further digits.
  - A **decimal number** that can only handle **7 decimal digits**.
  - `float x = 3.1415927;`
- `double`
  - A special float that can store **more (15) decimal digits**.
  - Often used for **scientific/financial** computations or anywhere where **accuracy matters**.
  - `double x = 3.141592653589793;`
- `char`
  - A variable that **stores a single character**; it can be a single letter, number, or symbol.
  - Acts as a **string when initialized as an array**.
  - `char x = 'a';`
  - `char y[5] = "abcde";`
---
## Arithmetic Operators
### Unary Operators
> Operators which require a **single operand/variable**.

| Operator | Operation | Description | Example |
| -------- | -------- | -------- | -------- |
| `+` | Unary Plus | Indicates a positive value | `+x` |
| `-` | Unary Minus | Indicates a negative value | `-x` |
| `++` | Increment | Increases value by 1 | `++x` or `x++` |
| `--` | Decrement | Decreases value by 1| `--x` or `x--` |

### Binary Operators
> Operators which require **two operands/variables**.

| Operator | Operation | Description | Example |
| -------- | -------- | -------- | ------- |
| `+` | Addition | Returns the sum of two variables | `x + y` |
| `-` | Subtraction | Returns the difference between two variables | `x - y` |
| `*` | Multiplication | Returns the product of two variables | `x * y` |
| `/` | Division | Returns the quotient of two variables; omits the remainder | `x / y` |
| `%` | Modulus | Returns the remainder of two variables; omits the quotient | `x % y` |

### Combined Operators
> Shorthand operations

| Shorthand | Equivalent |
| ------------------ | ----------------- |
| `x += y` | `x = x + y` |
| `x -= y` | `x = x - y` |
| `x *= y` | `x = x * y` |
| `x /= y` | `x = x / y` |
| `x %= y` | `x = x % y` |

### Relational Operators
> **Compares two values** and returns either `true (1)` or `false (0)`.

| Operator | Description | Example |
| -------- | ----------- | ------- |
| `>` | Greater than | `x > y` |
| `<` | Less than | `x < y` |
| `>=` | Greater than or equal to | `x >= y` |
| `<=` | Less than or equal to | `x <= y` |
| `==` | Equal to | `x == y` |
| `!=` | Not equal to | `x != y` |

### Logical Operators
> **Compares two values88 and returns either `true (1)` or `false (0)`, with the exception of `! (Not/Negation)` which reverses the value of a variable.

| Operator | Description | Example |
| -------- | ----------- | ------- |
| `&&` | And | `x && y` |
|  `\|\|` | Or | `x \|\| y` |
| `!` | Not (Negation) | `!x` |
---
## Conditional Statements
### If-else statement
> **Checks if an expression is true or false**, then decides which block of code to run.

Structure:
``` C
if (condition1) {
    // run this code if condition1 is true;
} else if (condition2) {
    // run this code if condition1 is false and condition2 is true;
} else {
    // run this code if none of the expressions are true;
}
```
In simpler terms...
- `if`: "If `condition1` is true, do this."
- `else if`: "If `condition1` was `false`, check if `condition2` is true, then do this."
- `else`: "If all conditions were `false`, do this."

Sample Code:
``` C
#include <stdio.h>
int main(void){
    int num = 0;
    
    if (num > 0) {
        // First check if the number is greater than 0.
        printf("The number is greater than zero!");
    } else if (num < 0) {
        // If it isn't greater than 0, it goes on to check if the number is less than 0.
        printf("The number is less than zero!");
    } else {
        // If both conditions were not met, it concludes that the number is 0. 
        printf("The number is zero!");
    }
}
```
[![W3Schools]][Link1]

### Ternary Operator
> A **shorthand for If-else** statements.
It's called **ternary** because it takes **three parameters**: the **condition**, a **value if true**, and a **value if false**.

Structure:
``` C
condition ? true : false;
```
Is equivalent to:
``` C
if (condition) {
    // true;
} else {
    // false;
}
```
Simply put, think of it as a mini if-else statement.
- If the condition is **true**, it picks the value on the **left** of the colon.
- If the condition is **false**, it picks the value on the **right** of the colon.

Sample Code:
```C
#include <stdio.h>
int main(void){
    int num = 1;
    
    printf("The number is %s.",
        (num > 0) ? "Greater than 0" : "Less than 0";
        /* 
        This is equivalent to:
            If (num > 0) {
                printf("The number is Greater than 0.");
            } else {
                printf("The number is Less than 0.");
            }
        */
    )
}
```
[![W3Schools]][Link2]

### Switch case
> A conditional statement **used when you have multiple possible values** for a variable and wish to **handle each value differently**.
> Preferred when there are **many cases** to check because it **makes the code look cleaner and easier to read**.
> Think of it as another if-else statement but for a lot of conditions.

Structure:
```C
switch (variable) {
    case value1:
        // Run this code if variable == value1
        break;
    case value2:
        // Run this code if variable == value2
        break;
    case value3:
        // Run this code if variable == value3
        break;
    case value4:
        // Run this code if variable == value4
        break;
    default:
        // Run this code if none of the cases match.
}
```
- `switch (variable)`: `variable` represents the variable being tested.
- `case value`: Represents a value to be matched/tested with the `variable`.
- `break`: Used to exit the `switch` statement after a case has been matched and executed.
- `default`: Similar to the `else` statement, runs the code if there were no matches.

Sample Code:
```C
#include <stdio.h>
int main(void){
    int day = 6;
    
    switch (day) {
        // Tests variable "day" for matches
        case 1:
            // If (day == 1)
            printf("Sunday");
            break;
        case 2:
        // If (day == 2)
            printf("Monday");
            break;
        case 3:
        // If (day == 3)
            printf("Tuessday");
            break;
        case 4:
        // If (day == 4)
            printf("Wednesday");
            break;
        case 5:
        // If (day == 5)
            printf("Thursday");
            break;
        case 6:
        // If (day == 6)
            printf("Friday");
            break;
        case 7:
        // If (day == 7)
            printf("Saturday");
            break;
        default:
        // Else; if there were no matches.
            printf("Error!");
            break;
    }
}
```
[![W3Schools]][Link3]

---
## Loops
> Used to **repeat blocks of code**.

### While Loop
> Repeats a block of code **as long as the given condition is true**.

Structure:
```C
while (condition) {
    // Run this code until the condition is false;
}
```
- `condition`: The expression to be evaluated each iteration of the loop; if it is true, the `loop body` is executed.
- `loop body`: The code inside the loop, which is executed each iteration.

Note:
- The loop **stops** when the condition becomes `false`.
- Make sure that there is a **line of code** which eventually **makes the condition `false`** within the `loop body`.
- **Infinite loops are not fun to deal with :(**

Sample Code:
```C
#include <stdio.h>
int main(void){
    int num = 1;
    
    while (num <= 5) {
        // Prints the value of variable num while it is less than or equal to 5
        printf("%d", num);
        num++; // Increment variable num to eventually end the loop
    }
}
```
[![W3Schools]][Link4]

### For Loop
> Repeats a block of code **a specific number of times**.

Structure:
```C
    for (initialization; condition; increment) {
        // Code to execute every iteration
    }
```
- `initialization` happens **only once**, before the loop starts.
- `condition` is **evaluated before each iteration**. If `condition` is `true`, the loop runs, otherwise, it stops.
- `increment` takes effect after every iteration. It **updates the loop variable** to eventually stop the loop.

Sample Code:
```C
#include <stdio.h>
int main(void){
    for (int i = 0; i <= 5; i++) {
        // Prints the value of variable i every iteration.
        printf("%d", i);
    }
}
```

### Do-While Loop
> Similar to the While loop, except the **condition is checked after** an iteration. Meaning the **loop will always run atleast once**, regardless whether the condition is true or false.

Structure:
```C
do {
    // Run this code
} while (condition)
```
- `loop body` runs atleast once regardless if the condition is met.
- `condition` is evaluated after every iteration.

Sample Code:
```C
#include <stdio.h>
int main(void){
    int num = 0;

    do {
    // Doesn't check the condition the first time it executes.
        printf("%d", num);
        num++;
    } while (num <= 5);
}
```
[![W3Schools]][Link5]

<!------------------------------>
[W3Schools]: https://img.shields.io/badge/W3Schools-04AA6D?logo=w3schools&logoColor=fff
[Link1]: https://www.w3schools.com/c/tryc.php?filename=demo_if_else_if
[Link2]: https://www.w3schools.com/c/tryc.php?filename=demo_if_ternary
[Link3]: https://www.w3schools.com/c/tryc.php?filename=demo_switch_default
[Link4]: https://www.w3schools.com/c/tryc.php?filename=demo_while_loop
[Link5]: https://www.w3schools.com/c/tryc.php?filename=demo_for_loop
[Link6]: https://www.w3schools.com/c/tryc.php?filename=demo_while_do
