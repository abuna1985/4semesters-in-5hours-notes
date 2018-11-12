# Lesson 1 - Big-O and Recursion

## Important Takeaways

* Big O is a way we can evaluate how efficient an algorithm can be.
    * With Big O, we focus on how much time a function will need to complete with a given **a number of inputs**
    * we use the variable _n_ to represent the **number of inputs**

* **Example**: If a function takes __100 milliseconds__ to complete with _1 input_ and __150 milliseconds__ with _1000 inputs_, the difference is so small that the extra __50 milliseconds__ between would not affect the environment it is running in.
  * But if a function takes __100 milliseconds__ with_ 1 input_ and __10 seconds__ with _1000 inputs_, that difference would definitely affect the environment that the function is running in.

**Big O strips away unimportant details of a function and let's us focus on the important parts to determine that difference in number of inputs and time.**

## Math Example of Big O Notation
**Example**: 3x<sup>2</sup> + x + 1

### When x is 5:
* 3(5<sup>2</sup>) + 5 + 1
* 75 + 5 + 1
* The answer is 81

When x is 5,000,000
* 3(5000000<sup>2</sup>) + 5000000 + 1
* 75000000000000 + 5000000 + 1
* The answer is 75,000,005,000,001

* Big O allows to focus on the the biggest term in the equation and move all the other parts away.
    * With 3x<sup>2</sup> + x + 1, the biggest term is x<sup>2</sup>. 
        * so the Big O of this equation is O(n<sup>2</sup>)
            * O takes the 3(), x and 1
            * We are just focus on the n<sup>2</sup> because the equation is going to take n*n time to go through a number of inputs.
* Big O can be applied to things like time and memory usage.
* **Disclaimer**: Big O does a lot more things mathematically, but for now we are just focusing on how this applies to programming algorithms.

## Code Example of Big O Notation

### Example #1
```javascript
function crossThenAdd(input) {
    var answers = [];
    for (var i = 0; i < input.length; i++) {
        var goingUp = input[i];
        var goingDown = input[input.length-1-i];
        answers.push(goingUp + goingDown);
    }
    return answers;
}
```

* The Big O for this equation is O(n)
    * This is because we are looping through the input array and using each element.

### Example #2
```javascript
function find(needle, haystack) {
    for(var i = 0; i < haystack.length; i++) {
        if (haystack[i] === needle) return true;
    }
}
```
* The Big O for this equation is also O(n)
    * If the needle is the last element of the haystack array, then we would have to loop through each element once.