# Switch Statements in JavaScript

<details>
<summary>Table of content</summary>

- [Switch](#switch)
- [Basic Syntax](#basic-syntax)
- [Breakdown](#switch-breakdown)
- [Example](#example)

</details>

## Switch

In JavaScript, a `switch` statement is a control flow statement that allows you to compare a value against multiple possible case values and execute code based on the first matching case. It's often used as an alternative to long chains of `if-else` statements when you have several possible conditions to check.

[Back to the top](#switch-statements-in-javascript)

### Basic syntax

```js
switch (expression) {
  case value1:
    // code to be executed if expression === value1
    break;

  case value2:
    // code to be executed if expression === value2
    break;

  // more cases if needed

  default:
  // code to be executed if none of the cases match
}
```

[Back to the top](#switch-statements-in-javascript)

### Switch breakdown

Let's breakdown the different parts of a switch statment.

- `expression`: The value or expression that is being evaluated.

- `case value1:`, `case value2:`: Each `case` represents a possible value of the expression. If the expression matches one of the values, the corresponding code block is executed. Remember to use the `:` directly after the value to match against the expression.

- `break`: This keyword is used to exit the `switch` statement once a match is found. If you omit the `break`, execution will continue to the next case regardless of whether it matches.

- `default`: This is an optional case that is executed if none of the previous cases match. It's similar to an `else` statement in an `if-else` chain.

[Back to the top](#switch-statements-in-javascript)

### Example

Imagine you have a day of the week represented by a number _( 1 for Sunday, 2 for Monday, and so on )_. You want to output the corresponding day name. Here's how you could use a switch statement for this:

```js
let day = 3;
let dayName;

switch (day) {
  case 1:
    dayName = "Sunday";
    break;
  case 2:
    dayName = "Monday";
    break;
  case 3:
    dayName = "Tuesday";
    break;
  case 4:
    dayName = "Wednesday";
    break;
  case 5:
    dayName = "Thursday";
    break;
  case 6:
    dayName = "Friday";
    break;
  case 7:
    dayName = "Saturday";
    break;
  default:
    dayName = "Invalid day";
}

console.log(dayName); // Outputs "Tuesday" for day = 3
```
In this example, the `switch` statement checks the value of the day variable and assigns the corresponding day name to the `dayName` variable. If the value of `day` doesn't match any of the cases, the default case is executed, assigning "Invalid day" to `dayName`.

In summary, a `switch` statment provides a more cleaner alternative to a longer `if-else` chain and most of the times makes your code more readable and maintainable. 

One thing to note here is that the value next to the case must be a value that can be compared using strict equality with the value that is computed from the expression. The expression can be complicated as long as it results in some sort of value.