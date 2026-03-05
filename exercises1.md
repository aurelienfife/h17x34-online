# H17X 34 Python Exercises 1

## Python Skills Covered

*   Collecting user input with `input()`
*   Displaying output using `print()`
*   Working with strings, including concatenation and f-strings
*   Converting data types such as `int()` and `float()`
*   Performing basic arithmetic calculations
*   Using conditional statements (`if`, `elif`, `else`)
*   Creating simple decision‑based program flow
*   Using dictionaries for word lookup and basic data mapping

## 1. Ask for the user’s name

Write a program that asks the user to enter their name, then prints:

“Hello *name*”

### Hint

<details>
<summary>Show hint</summary>

Use `input()` to read a string, then print it with concatenation or an f-string.

</details>

### Suggested solution

<details>
<summary>Show solution</summary>

```python
name = input("Enter your name: ")
print(f"Hello {name}")
```

</details>

***

## 2. Ask for firstname and surname, then concatenate

Ask for firstname and second name in separate inputs. Output:

“Hello <firstname> <secondname>”.

### Hint

<details>
<summary>Show hint</summary>

Collect two inputs and join them with a space.

</details>

### Suggested solution

<details>
<summary>Show solution</summary>

```python
first = input("Enter your first name: ")
second = input("Enter your second name: ")
print(f"Hello {first} {second}")
```

</details>

***

## 3. Age check for nightclub

Ask the user how old they are.  
If age is 18 or over, print “welcome to the nightclub”.  
If under 18, print “sorry you are too young to attend our virtual nightclub”.

### Hint

<details>
<summary>Show hint</summary>

Convert the input to an integer using `int()`.

</details>

### Suggested solution

<details>
<summary>Show solution</summary>

```python
age = int(input("How old are you? "))

if age >= 18:
    print("welcome to the nightclub")
else:
    print("sorry you are too young to attend our virtual nightclub")
```

</details>

***

## 4. Area of a floor

Ask for the length and breadth of a floor. Calculate the area and display it.

### Hint

<details>
<summary>Show hint</summary>

Area is calculated using length \* breadth.

</details>

### Suggested solution

<details>
<summary>Show solution</summary>

```python
length = float(input("Enter the length: "))
breadth = float(input("Enter the breadth: "))

area = length * breadth
print(f"The area of the floor is {area}")
```

</details>

***

## 5. Favourite class

Ask the user what their favourite class is.  
If they say Python, print “I am glad you chose that option”.  
Otherwise print “Oh, really, what about Python”.

### Hint

<details>
<summary>Show hint</summary>

Use `.lower()` for case insensitive comparison.

</details>

### Suggested solution

<details>
<summary>Show solution</summary>

```python
subject = input("What is your favourite class? ")

if subject.lower() == "python":
    print("I am glad you chose that option")
else:
    print("Oh, really, what about Python")
```

</details>

***

## 6. Observing number and string concatenation

Try the example shown in class involving adding numbers and strings.

### Hint

<details>
<summary>Show hint</summary>

Python does not allow adding a number directly to a string.

</details>

### Typical observation

<details>
<summary>Show explanation</summary>

You will see an error similar to:

    TypeError: can only concatenate str (not "int") to str

Python requires numbers to be converted using `str()`.

</details>

***

## 7. Bags of grit cost calculator

Each bag costs £6.  
If more than 6 bags are ordered, postage is not added.  
Otherwise postage is £3.

### Hint

<details>
<summary>Show hint</summary>

Use an if statement to decide whether to add postage.

</details>

### Suggested solution

<details>
<summary>Show solution</summary>

```python
bags = int(input("How many bags of grit would you like? "))

cost = bags * 6
if bags <= 6:
    cost += 3

print(f"Total cost: £{cost}")
```

</details>

***

## 8. Car sales commission

Ask how many cars were sold today.  
Commission is £100 per car.  
If more than 10 cars are sold, a bonus of £150 is added.

### Hint

<details>
<summary>Show hint</summary>

Calculate commission first, then add the bonus if needed.

</details>

### Suggested solution

<details>
<summary>Show solution</summary>

```python
cars = int(input("How many cars did you sell today? "))

commission = cars * 100
bonus = 150 if cars > 10 else 0

print(f"Commission: £{commission}")
print(f"Bonus: £{bonus}")
```

</details>

***

## 9. Translate 3 English words into another language

Ask the user to enter one of three English words. Output the translation.

### Hint

<details>
<summary>Show hint</summary>

Use a dictionary mapping English words to translations.

</details>

### Suggested solution (English to French)

<details>
<summary>Show solution</summary>

```python
dictionary = {
    "cat": "chat",
    "dog": "chien",
    "house": "maison"
}

word = input("Enter a word (cat, dog, house): ").lower()

if word in dictionary:
    print(dictionary[word])
else:
    print("Word not found.")
```

</details>

***

## 10. Exam score feedback

Ask the user what score they got.  
If over 80, print “you have a very high score”.  
If between 50 and 79, print “you have done quite well”.  
If below 50, print “You will need to study a bit more”.

### Hint

<details>
<summary>Show hint</summary>

Use if, elif and else for the three ranges.

</details>

### Suggested solution

<details>
<summary>Show solution</summary>

```python
score = int(input("Enter your exam score: "))

if score > 80:
    print("you have a very high score")
elif 50 <= score <= 79:
    print("you have done quite well")
else:
    print("You will need to study a bit more")
```

</details>
