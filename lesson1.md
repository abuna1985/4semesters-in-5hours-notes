# Lesson 1 - Big-O and Recursion

## Important Takeaways

* Big O is a way we can evaluate how efficient an algorithm can be.
  * With Big O, we focus on how much time a function will need to complete with a given **a number of inputs**
    * we use the variable _n_ to represent the **number of inputs**

* **Example**: If a function takes __100 milliseconds__ to complete with _1 input_ and __150 milliseconds__ with _1000 inputs_, the difference is so small that the extra __50 milliseconds__ between would not affect the environment it is running in.
  * But if a function takes __100 milliseconds__ with_ 1 input_ and __10 seconds__ with _1000 inputs_, that difference would definitely affect the environment that the function is running in.

* Big O strips away unimportant details of a function and let's us focus on the important parts to determine that difference in number of inputs and time.