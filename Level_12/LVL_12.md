# Level 08 A

## Coding Philosophy: Debugging

If you have problems with your code try printing out the value of your variables using `System.out.println` or the QuintOS `log` function. `log` shows the value of variables in the JavaScript console so you can see how your code is actually working.

# Level 08 B

## eraseRect

```java
eraseRect(row, col, w, h);
```

Erases text within the specified rectangle.

## textRect

Make boxes using `textRect(row, col, w, h)` around the blank spaces and letters just like in the Wheel of Fortune TV show.

```java
textRect(5, 5, 3, 3); // make a 3x3 rect at row 5 column 5 (5,5)
text("w", 6, 6); // make letter 'w' at row 6 column 6 (6,6)
```

Use `for` loops to make all the boxes for the phrase!

```txt
┌─┐┌─┐┌─┐┌─┐┌─┐
│W││h││e││e││ │
└─┘└─┘└─┘└─┘└─┘
```

# Level 08 C

## delay

The `sleep` function of the `Thread` class is used to delay the rate at which letters are displayed.

```js
void delay(milliseconds) {
	try {
		// waits for the specified amount of milliseconds
		Thread.sleep(milliseconds);
	} catch (InterruptedException e) {
		System.err.println("delay failed");
		System.exit(0);
	}
}
```

You can use the `delay` function in your code to pause the program for the specified amount of time.

```java
// you need to make the function asynchronous to use await
void takeFive() {
	System.out.println("start!");
	delay(5000)
	System.out.println("5 seconds passed");
}

takeFive();
```

## String toUpperCase and toLowerCase

```java
String str = 'Hello!';
String up = str.toUpperCase(); // up -> "HELLO!"
String low = str.toLowerCase(); // low -> "hello!"
```

These functions do not change the original value of the string.

## substring String

```java
str.substring(start, end);
```

This function returns a subsection of the string, starting at the start index and ending and the end index. It does not change the original value of the string. The `end` index is optional.

## replace String

```java
String str = 'The cat jumped over the moon. The cat meowed.';
String result = str.replace("cat", "dog");
System.out.println(result);
// -> "The dog jumped over the moon. The cat meowed."
```

This function takes two input parameters, the first input parameter is replaced in the string by the second. Note that it only does one replacement.

This function does not change the original value of the string.
