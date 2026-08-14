# Day-87-Check-Palindrome

Day 87/100 - Python Program to Check if a Given String is Palindrome

# Check if a String is a Palindrome

A program to dynamically evaluate whether a user-provided string reads the same forwards and backwards, utilizing Python's string slicing and sanitization methods.

## 📝 Description

This program analyzes a string of text inputted by the user to determine if it is a palindrome.

The core logic is efficiently handled within the `is_palindrome(s)` function. To ensure accurate evaluation regardless of how the user types, the script first sanitizes the input. It uses `s.replace(" ", "")` to remove any spaces and `.lower()` to convert all characters to lowercase. This means phrases with varied spacing or capitalization will be accurately processed into a uniform sequence.

After the string is sanitized, the function evaluates `s == s[::-1]`. This statement uses Python's extended slicing syntax `[::-1]` to instantly reverse the string, and the `==` operator to check if this reversed version perfectly matches the sanitized original. It returns a boolean `True` or `False`, which the driver code uses to print a cleanly formatted result.

---

## 🎯 Problem Statement

### Input:

* **Input 1:** A string of text provided by the user via the terminal prompt.



### Output:

* If True: A formatted string stating: "[input_string] is a palindrome.".


* If False: A formatted string stating: "[input_string] is not a palindrome.".



### Rules:

1. The program must prompt the user to input a string using `input()`.


2. The core logic must be encapsulated in a function named `is_palindrome(s)`.


3. The function must sanitize the string by removing spaces and converting it to lowercase.


4. The function must evaluate the string against its reversed self using `s[::-1]` and return a boolean value.


5. The driver code must capture the returned value in an `if/else` block and print the appropriate statement to the console.



---

## 💡 Examples

### Example 1 (Standard Word)

**Input:**

```text
racecar

```

**Output:**

```text
racecar is a palindrome.

```

**Explanation:** The word "racecar" reads exactly the same backwards as it does forwards. The slicing `[::-1]` produces an identical string, so the function returns `True`.

### Example 2 (Sentence with Spaces and Mixed Cases)

**Input:**

```text
Taco cat

```

**Output:**

```text
Taco cat is a palindrome.

```

**Explanation:** Before checking for the palindrome, the sanitization logic converts the string into "tacocat". Because this contiguous, lowercase block of text is a perfect palindrome, the program correctly identifies the original phrase as one.

### Example 3 (Not a Palindrome)

**Input:**

```text
Python

```

**Output:**

```text
Python is not a palindrome.

```

**Explanation:** The sanitized string "python" reversed is "nohtyp". Because these two sequences do not match, the function returns `False`, triggering the `else` block to print the negative result.

---

## 🚀 How to Use

1. **Clone this repository** (or save the script as "Day 87.py").

```bash
git clone https://github.com/adiaryaz/Day-87-Check-Palindrome.git
cd check-palindrome

```

2. **Run the program**:

```bash
python "Day 87.py"

```

Enter any word, phrase, or sentence when prompted to instantly discover if it is a perfect palindrome!
