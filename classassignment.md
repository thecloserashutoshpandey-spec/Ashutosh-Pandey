# Class Assignment

This repository contains solutions to basic programming problems written in JavaScript.

---

## 1. Fibonacci Series

This program prints the Fibonacci series up to `n` numbers.

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



