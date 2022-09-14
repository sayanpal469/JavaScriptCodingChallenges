![javascript](images/logo.png)

<h1 align="center" id='header'>JavaScript Coding Challenges </h1>

## 1. Multiples of 3 or 5

If we list all the natural numbers below 10 that are multiples of 3 or 5, we get 3, 5, 6 and 9. The sum of these multiples is 23. Finish the solution so that it returns the sum of all the multiples of 3 or 5 below the number passed in.

Note: If the number is a multiple of both 3 and 5, only count it once. Also, if a number is negative, return 0.

```js
const solution = (number) => {
  //Write Your solution Here
};

console.log(solution(0)); // 0
console.log(solution(-15)); // 0
console.log(solution(10)); // 23
console.log(solution(20)); // 78
console.log(solution(200)); // 9168
```

<details><summary style="cursor:pointer">Solution</summary>

```js
const solution = (number) => {
  let sum = 0;
  for (let i = 0; i < number; i++) {
    if (i % 3 === 0 || i % 5 === 0) {
      sum += i;
    }
  }
  return sum;
};
```

</details>

---
**[⬆ Back to Top](#header)**

## 2. Sum of an array

Take an array of integer data type of size 10 And pritn the sum of those 10 integers.


```js
const solution = (array) => {
  //Write Your solution Here
};

console.log(solution([1, 2, 3, 4, 5, 6, 7, 8, 9, 10])); // 55
console.log(solution([22, 11, 55, 66, 77, 88, 99, 44, 33, 10 ])); // 505
console.log(solution([12, 12, 65, 36, 87, 18, 79, 14, 73, 70 ])); // 466
```

<details><summary style="cursor:pointer">Solution</summary>

```js

const solution = (array) =>{
    let sum = 0;
    for(let i = 0; i < array.length; i++){
        sum += array[i];
    }
    return sum;
};
```

</details>

---
**[⬆ Back to Top](#header)**


## 3. Even or Odd

Create a function that takes an integer as an argument and returns "Even" for even numbers or "Odd" for odd numbers.

```js
const evenOrOdd = (number) => {
  //Write Your solution Here
};

console.log(evenOrOdd(0)); // 'Even'
console.log(evenOrOdd(2)); // 'Even'
console.log(evenOrOdd(3)); // 'Odd'
console.log(evenOrOdd(-3)); // 'Odd'
```

<details><summary style="cursor:pointer">Solution</summary>

```js
//Solution 1
const evenOrOdd = number => number % 2 === 0 ? 'Even' : 'Odd';

//Solution 2
const evenOrOdd = (number) =>{
    if(number % 2 === 0){
        return 'Even';
    }else{
        return 'Odd';
    }
}
```

</details>

---
**[⬆ Back to Top](#header)**




## 4. Find the biggest integer.

Say you are given the following array of integer data type. Now write a program which will find the biggest integer and print the integer with it's index.

```js
const solution = (array) => {
  //Write Your solution Here
};

console.log(solution([10, 20, 30, 40, 50])); // 50 - 4
console.log(solution([5, 10, 15, 20, 25, 30])); // 30 - 5
console.log(solution([44, 665, 221, -434, 643, 123])); // 665 - 1
console.log(solution([-34, 64, -1, 0, 45])); // 64 - 1
```

<details><summary style="cursor:pointer">Solution</summary>

```js
const solution = (array) =>{
    let biggestNumber = 0;
    let index 
    for(let i = 0; i < array.length; i++){
        if(array[i] > biggestNumber){
            biggestNumber = array[i];
            index = i;
        }
    }
    return {biggestNumber, index};
}
```

</details>

---
**[⬆ Back to Top](#header)**




## 5.  Find the largest number among the three numbers.

Write a program to find largest of three given numbers is discussed here. Inpup three integers from the user and find the largest number among them. Given three numbers num1, num2, num3. The task is to find the largest number among the three numbers.
```js
const solution = (num1, num2, num3)=> {
  //Write Your solution Here
};

console.log(solution(10, 20, 30,)); //30
console.log(solution(100,- 20, 30,)); //100
console.log(solution(100, 229, 30,)); //229
```

<details><summary style="cursor:pointer">Solution</summary>

```js

const solution = (num1, num2, num3)=>{

    if(num1 > num2 && num1 > num3){
        return num1;
    }
    else if(num2 > num1 && num2 > num3){
        return num2;
    }else{
        return num3;
    }
}
```

</details>

---
**[⬆ Back to Top](#header)**



## 6. Clock

The clock shows h hours (0 <= h <= 23), m minutes (0 <= m <= 59) and s seconds (0 <= s <= 59) after midnight. Your task is to write a function which returns the time since midnight in milliseconds. There are 1,000 milliseconds in a second.

```js
const solution = (h, m, s)=> {
  //Write Your solution Here
};


console.log(solution(0, 0, 0)); // 0
console.log(solution(0, 1, 1)); // 61000
console.log(solution(1, 0, 0)); // 3600000
console.log(solution(1, 0, 1)); // 3601000
console.log(solution(1, 1, 1)); // 3661000
```

<details><summary>Solution</summary>

```js
const solution = (h, m, s) =>{
    if(0<=h <=23 && 0<= m <= 59 && 0 <= s <= 59){
        return (h * 60 * 60 + m * 60 + s ) * 1000;
    }
}

```

</details>

---

**[⬆ Back to Top](#header)**


## 7. Reverse Word.

Take word and print the word in reverse order if you take 'BANGLADESH' your program should return or print 'HSEDALGNAB'.

```js
const solution = (word)=> {
  //Write Your solution Here
};


console.log(solution('BANGLADESH')); //HSEDALGNAB
console.log(solution('PROGRAMMING')); //GNIMMARGORP
console.log(solution('DEVELOPMENT')); //TNEMPOLEVED
```

<details><summary>Solution</summary>

```js
const solution = (word) =>{
    let reverseWord = '';
    for(let i= word.length - 1; i >= 0; i--){
        reverseWord += word[i];
    }

    return reverseWord;
}

```

</details>

---

**[⬆ Back to Top](#header)**


## 8. Vowel and Consonant

Take a small letter alphabet as a functuion peramitter and print whether it is VOWEL or CONSONANT.

```js
const solution = (letter)=> {
  //Write Your solution Here
};


console.log(solution('a')); // VOWEL
console.log(solution('u')); // VOWEL
console.log(solution('k')); // CONSONANT
```

<details><summary>Solution</summary>

```js
//Solution 1
const solution = (letter) => {
    return letter === 'a' || letter === 'e' ||  letter === 'i' || letter === 'o' || letter === 'u' ? 'VOWEL' :  'CONSONANT';
}

//Solution 2
const solution = (letter) =>{
    if(letter === 'a' || letter === 'e' ||  letter === 'i' || letter === 'o' || letter === 'u'){
        return 'VOWEL';
    }else{
        return 'CONSONANT';
    }
}

```

</details>

---

**[⬆ Back to Top](#header)**