# Exercises

1. Create two functions: `double` and `square`.
`double` should take a number and return the number times two.
```
const double = num => num * 2;

```
`square` should take a number and return the number squared.
```
const square = num => num * num

```
 * Create a third function `doubleSquare` that uses both of the functions to return a number that is first doubled and then squared.
 ```
 const double = num => num * 2;
 const square = num => num * num;
 const doubleSquare = num => square(double(num));
 console.log(doubleSquare(2));

 ```

2. Create a function `classyGreeting` that takes as input the strings `firstName`  and `lastName`,
and returns a string with a greeting using the two.
```
const classyGreeting=(...args)=> `Hi my name is  ${args[0]}${args[1]}`
console.log(classyGreeting('Thomas', ' Perez'));

```

  * Create a second function `yell`  that takes string as input and returns the string in all capitalized letters.
  ```
  const yell = word => word.toUpperCase();
  console.log(yell('hello'));

  ```
  * Create a third function  `yellGreeting`  that will take the `firstName`  and `lastName`  as inputs and yell a greeting using the two.
```
const classyGreeting=(...args)=> `Hi my name is  ${args[0]}${args[1]}`
const yell = word => word.toUpperCase();
const yellGreeting = (firstname,lastname)=>
yell(classyGreeting(firstname,lastname))
console.log(yellGreeting('Thomas', ' Perez'));
```
3. The [concat](https://www.w3schools.com/jsreF/jsref_concat_array.asp) array method is used to merge two (or more) arrays.
Write a `removeDupes` function that takes an array as an argument and returns a copy without any duplicate elements.
Then, write a function `concatAndRemoveDupes`  that combines two arrays and removes any duplicates.
```
function removeDupes(arr){
  let answer = [];
  for(let i = 0; i < arr.length; i++)
  answer.push(i)
  if(answer === answer){
    console.log(answer - 1);
  } else {

  }
return arr
}
console.log(removeDupes(['luigi','toad','mario','bowser','mario']));

```

  _Hint:_ Use the array method `includes`, an object, or a Set. Or the spread operator instead of concat.  

4. Given a list of grades, we can get the median grade by sorting the list and taking the middle element, or the average of the two middle elements.
Create the functions `sort` and `middleElement`, and then use them to create the functions `median`.

let grades = [91, 85, 100, 92, 88];

console.log(median(grades)); // Should log 91
```
const median = (arr) => {
  arr = sort(arr);
  let midIdx = Math.floor(arr.length / 2)
  if(arr.length % 2 === 0 ){
    return (arr[midIdx -1] + arr[midIdx] / 2)
  } else {
    return arr[midIdx]
  }
  }
  const sort = (arr) => {
    return arr.sort((a,b) => a - b)
  }
let answer = median([91, 85, 100, 92, 88])
console.log(answer);

```

5. Write a function called `repeat` that takes in a string and numberOfTimes. The function should log to the screen the string however
many times as numberOfTimes. If the user does not enter a numberOfTimes it should default to 2.
```
const repeat = (string , numOfTimes) => {
  if ( numOfTimes > 0){
    return string.repeat(numOfTimes);
  } else if (numOfTimes === 0){
      return string.repeat(2);
    } else {
      return '';
    }
    return repeat
}
console.log(repeat('tommy', 5 ));
```

6. Using the spread operator, write a function that can take any number of arguments and return the sum of all of them.
```
const operator = (...arg) => {
  let answer = 0;
  for (let i = 0; i < arg.length; i++){
  answer += arg[i]
  }
return answer
}
console.log(operator(1,2,3,4,5));
```

7. Write a function called `adder` takes in one number and returns a function that will add that number with another number.
Using `adder` create an `add5` and an `add9` function. Hint: Closures!
