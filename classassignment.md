# Class Assignment

This repository contains solutions to basic programming problems written in JavaScript.

---

## 1. Fibonacci Series

This program prints the Fibonacci series up to `n` numbers.

## Logic
The Fibonacci series starts with two numbers 0 and 1. After that, every next number is obtained by adding the previous two numbers. For example, 0 + 1 = 1, then 1 + 1 = 2, then 1 + 2 = 3, and the series keeps growing in this way.

In the program, we store the first two numbers in variables and run a loop for n times. During each iteration we print the current number and calculate the next number by adding the previous two numbers. Then we update the variables and repeat the process until the required number of Fibonacci values is generated.

### Code

```javascript
function fibonacci(n) {
    let a = 0, b = 1;
    let res = [];

    for (let i = 0; i < n; i++) {
        res.push(a);
        let next = a + b;
        a = b;
        b = next;
    }

    return res;
}

console.log(fibonacci(10));

---

## 2. Sum of Total Digits in a Number

This program calculates the sum of digits of a given number.

##Logic
The goal of this program is to find the sum of all digits in a number. For example, if the number is 1234, we add all digits like 1 + 2 + 3 + 4 to get the total sum.

In the program, we start with a variable sum set to 0. We take the last digit of the number using the modulus operator %. That digit is added to sum. Then we remove the last digit by dividing the number by 10. This process repeats until the number becomes 0, and the final value of sum is the total of all digits.\

### Code

```javascript
function sumOfDigits(num) {
    let sum = 0;

    while (num > 0) {
        sum += num % 10;
        num = Math.floor(num / 10);
    }

    return sum;
}

console.log(sumOfDigits(1234));


---

## 3. Palindrome

This program checks whether a number or string is a palindrome.

##Logic
A palindrome is a number or word that reads the same forward and backward. For example, 121 and madam are palindromes because reversing them gives the same value.

In the program, we first convert the value into a string so it can be easily reversed. Then we reverse the string and compare it with the original value. If both are the same, the program returns true, which means it is a palindrome. If they are different, it means the value is not a palindrome.

### Code

```javascript
function isPalindrome(value) {
    let str = value.toString();
    let reversed = str.split('').reverse().join('');

    return str === reversed;
}

console.log(isPalindrome(121));
console.log(isPalindrome(123));

---


## 4. Print Triangle Pattern

This program prints a triangle pattern using `*`.

##Logic
This program prints a triangle pattern using star (*) symbols. Each row of the triangle contains stars equal to the row number. For example, the first row prints one star, the second row prints two stars, and so on.

In the program, we use a loop that runs from 1 to the total number of rows. In each iteration, we print the star character repeated the same number of times as the current row number. As the loop continues, the number of stars increases, forming a triangle pattern.

### Code

```javascript
function printTriangle(rows) {
    for (let i = 1; i <= rows; i++) {
        console.log("*".repeat(i));
    }
}

printTriangle(5);


---

#5 Factorial

This program calculates the factorial of a number.

##Lgic
Factorial of a number means multiplying that number with all positive integers before it. For example, the factorial of 5 is 5 × 4 × 3 × 2 × 1 = 120.

In the program, we start with a variable result set to 1. Then we use a loop from 1 to the given number n. During each iteration we multiply result by the current number. After the loop finishes, the final value stored in result is the factorial of the number.


### Code

```javascript
function factorial(n) {
    let result = 1;

    for (let i = 1; i <= n; i++) {
        result *= i;
    }

    return result;
}

console.log(factorial(5));



