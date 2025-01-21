<link rel="stylesheet" href="https://cs.westminsteru.edu/~greg/styles.css">

<p id="header">Lab 1 - Java Refresher</p>

### Due: By the Start of the Next Lab Period

### How Labs are Managed and Graded

1. Select a partner on your own. 
2. Work as a pair to complete the lab. At the end of the lab period, share all files with each partner.
3. Each partner will submit the lab separately. 
4.  If you do not finish the lab during the lab period, you may either get together outside of class to complete it or complete it on your own. If you choose to complete it on your own, be sure to indicate this in your submission. 

### Objectives

The objectives of this lab are:

1. Review the Java language.
2. Apply enumerated data types.
3. Create and use Java objects.
4. Verify your code functions correctly by running unit tests.

### Overview

This lab will involve designing a class named `GenericCoin` that represents a coin and that you can "flip" to either heads or tails. You will test your implementation using a provided unit test and then write Java code that uses your `GenericCoin` class. There is also an extra credit portion where you can write a simple game that uses the `GenericCoin` class.


### Create an IntelliJ Project

Create a project from version control and copy-paste the following URL:

`https://github.com/greggagne/202-lab1.git`

The `src` folder will have the following Java classes:

- `GenericCoin.java`
- `UseGenericCoin.java`
- `CoinTest.java`

### Develop the GenericCoin Class

Add some comments to your class including your name, date, and brief description of what the class does:

```java
/**
 * @author YOUR NAME GOES HERE
 * 
 * This class provides the functionality of a generic coin
 * that maintains the the side (heads or tails) of the coin.
 */
 
 public class GenericCoin
 {
    . . .
 }
```

Your class will maintain the side (heads/tails) using an **enumerated** data type:

```java
public enum CoinSide {HEADS, TAILS};
```

Create an instance variable that represents the current side of the coin. Use the enumeration type `CoinSide` as the data type for this instance variable. You should declare a `CoinSide` instance variable in the same way that you would declare any other instance variable. However, this object can only have two values, `CoinSide.HEADS` and `CoinSide.TAILS`.

Usage Examples

```java
public enum CoinSide {HEADS, TAILS}; // CoinSide is a new data type

private CoinSide side;					// side is of type CoinSide

```

```java
side = CoinSide.HEADS;					// sets side to HEADS
```

```java
if (side == CoinSide.TAILS) {
	// some logic if side is set to tails ...
}
```

Your `GenericCoin` class must have the following methods (be sure to use these method signatures!)

* A default constructor that initializes the side to heads:
	* `public GenericCoin()`

* Three mutators:
	* `public void setToHeads()` that sets the coin to heads
	* `public void setToTails()` that sets the coin to tails
	* `public void toss()` that randomly sets the coin to either heads or tails. Use the `java.lang.Math.random()` method to set the coin to heads 50% of the time and tails 50% of the time.

* Three accessors:
	* `public boolean isHeads()` returns true if the coin is set to heads
	* `public boolean isTails()` returns true if the coin is set to tails
	* `public String toString()` returns the String "Heads" or "Tails" based on the side of the coin.

	
Be sure to comment your code as you develop it.

### Test Your Implementation

Test your implementation of `GenericCoin` using the `CoinTest.java` unit tests.

If your `GenericCoin` class works properly, you should see the green output. Red indicates an error. Be sure to fix all logic errors before proceeding to the next step.

### Develop a Separate Class that Uses GenericCoin

Now that you know your `GenericCoin` class works properly, add code to the  `UseGenericCoin.java` class that creates and uses `GenericCoin` objects. You may place all logic in the `main()` method of this class.

Initially, create two `GenericCoin` objects and toss both coins 100 times each. Next, report the percentage of heads for each coin. You output will be similar to what is shown below:

```
Coin 1 landed on heads 48.0% of the time.
Coin 2 landed on heads 44.0% of the time.
```

Next, report which coin landed upon heads most often, and output the difference between the number of heads of the two coins. As an illustration, your program would print **one** of the following example outputs: 

```
The first coin was heads 3 more times.
```
```
The second coin was heads 7 more times.
```
```
Both coins had the same number of heads.
```

### Extra Time? Write a Game for Extra Credit

Create a new program called `CoinGame.java` that asks the user to guess whether the coin will be heads or tails. Then, flip the coin and report the results of the coin toss. Provide fun messages if the user guesses correctly or not! Repeat until the user is done playing the game.

After the user is done, report the number of coin tosses, and how many times the user guessed correctly. Also, include the percentage of correct guesses.

The `java.util.Scanner` class is a good choice for capturing user input.

### Lab Submission

At the completion of the lab period, be sure to share the Java files with your partner. This ensures both partners have all the necessary files. **Both** lab partners must upload the following files to the Canvas submission box for Lab - Java Refresher:

* `GenericCoin.java`
* `UseGenericCoin.java`
* `CoinGame.java` (if you completed this step.)

A rubric will be provided for the Canvas submission box for this lab.

