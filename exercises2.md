# H17X34 Python Exercises 2

## Python Skills Covered

*   Creating and manipulating lists
*   Appending, inserting and removing items
*   Looping through lists using `for` and `while`
*   Building new lists based on conditions
*   Sorting lists
*   Calculating totals and averages
*   Casting input to integers
*   Using counters and accumulators

## 1. Search for a student name in a list

Write a program that stores 10 student names in a list. Ask the user to enter a name to search for and output a message indicating whether the name was found.

### Hint

<details>
<summary>Show hint</summary>

Use the `in` operator to check whether the name exists in the list.

</details>

### Suggested solution

<details>
<summary>Show solution</summary>

```python
pupils = ["sarah", "james", "michael", "susan", "gerry",
          "abigail", "david", "emma", "lucy", "mark"]

search = input("Enter a name to search for: ").lower()

if search in pupils:
    print("Name found in the list.")
else:
    print("Name not found.")
```

</details>


## 2. Modify the list `thisnames`

Given the list:

```python
thisnames = ["sarah", "james", "michael", "susan", "gerry"]
```

### 2a. Add the name "jimmy" to the end of the list

Show the amended list.

### Hint

<details><summary>Show hint</summary>
Use the `.append()` method.
</details>

### Suggested solution

<details><summary>Show solution</summary>

```python
thisnames.append("jimmy")
print(thisnames)
```

</details>


### 2b. Add the name "abigail" as the third item

Show the amended list.

### Hint

<details><summary>Show hint</summary>
Use `.insert(position, value)` remembering that lists start at index 0.
</details>

### Suggested solution

<details><summary>Show solution</summary>

```python
thisnames.insert(2, "abigail")
print(thisnames)
```

</details>


### 2c. Remove "gerry" from the list

Show the amended list.

### Hint

<details><summary>Show hint</summary>
Use `.remove("gerry")`.
</details>

### Suggested solution

<details><summary>Show solution</summary>

```python
thisnames.remove("gerry")
print(thisnames)
```

</details>


### 2d. Create a new list containing only the names with the letter "s"

Create `newlistwiths` and add names from `thisnames` that contain an "s". Show the new list.

### Hint

<details><summary>Show hint</summary>
Loop through the list and check `"s" in name`.
</details>

### Suggested solution

<details><summary>Show solution</summary>

```python
newlistwiths = []

for name in thisnames:
    if "s" in name:
        newlistwiths.append(name)

print(newlistwiths)
```

</details>


### 2e. Sort both lists alphabetically and display them

### Hint

<details><summary>Show hint</summary>
Use `.sort()` on each list.
</details>

### Suggested solution

<details><summary>Show solution</summary>

```python
thisnames.sort()
newlistwiths.sort()

print("Sorted thisnames:", thisnames)
print("Sorted newlistwiths:", newlistwiths)
```

</details>


## 3. Working with a list of numbers

Given:

```python
thesenumbers = [1, 7, 9, 4, 2, 9, 12, 13, 17]
```

### 3a. Loop through the items and add them up

Output the total.

### Hint

<details><summary>Show hint</summary>
Start with `total = 0` and add each number in the loop.
</details>

### Suggested solution

<details><summary>Show solution</summary>

```python
thesenumbers = [1, 7, 9, 4, 2, 9, 12, 13, 17]

total = 0
for num in thesenumbers:
    total += num

print("Total:", total)
```

</details>


### 3b. Get the length of the list and calculate the average

Output the average number.

### Hint

<details><summary>Show hint</summary>
Use `len(thesenumbers)` and divide total by the length.
</details>

### Suggested solution

<details><summary>Show solution</summary>

```python
length = len(thesenumbers)
average = total / length

print("Average:", average)
```

</details>


## 4. Create a list of user-entered numbers

Create an empty list called `userinputlist`.  
Use a `while` loop to ask the user to enter 5 numbers.  
Convert each input into an integer and add it to the list.  
Output the final list.

### Hint

<details><summary>Show hint</summary>
Use a counter variable, increase it inside the loop, and stop when it reaches 5.
</details>

### Suggested solution

<details><summary>Show solution</summary>

```python
userinputlist = []

count = 0
while count < 5:
    num = int(input("Enter a number: "))
    userinputlist.append(num)
    count += 1

print(userinputlist)
```

</details>
