# 🐍 Python Data Structures: Master Summary
> A comprehensive guide to Lists, Tuples, Sets, and Dictionaries in Python.

---



## 📋 1. Lists
Description: A list in Python is a mutable, ordered collection of elements that can store items of different data types. Lists are created using square brackets [] or the list() constructor.


Below is a table summarizing the in-built functions of lists with a one-line explanation and example:

### `🛠️ Core Functions`

| Function | Description | Example | 
| :--- | :--- | :--- |
| `append(x)` |	Adds an element to the end of the list. |	`[1, 2].append(3)` → `[1, 2, 3]`  |
| `extend(iterable)` |	Adds all elements of an iterable to the end of the list. |	`[1, 2].extend([3, 4]) → [1, 2, 3, 4]` |
| `insert(index, x)` |	Inserts an element at a specified index. |	`[1, 2].insert(1, 100) → [1, 100, 2]` |
| `pop([index])` |	Removes and returns the element at the specified index (default is last). |	`[1, 2, 3].pop() → [1, 2]` |
| `remove(x)` |	Removes the first occurrence of the specified element. |	`[1, 2, 3].remove(2) → [1, 3]` |
| `clear()` |	Removes all elements from the list. |	`[1, 2, 3].clear() → []` |
| `count(x)` |	Returns the number of occurrences of the specified element. |	`[1, 2, 2, 3]; print(l.count(2)) → 2` |
| `reverse()` |	Reverses the order of the list. |	`[1, 2, 3]; l.reverse() → [3, 2, 1]` |
| `sort()` |	Sorts the list in ascending order. | `[3, 1, 2]; l.sort() → [1, 2, 3]` |
| `copy()` |	Returns a shallow copy of the list. |	`l=[1, 2, 3]; l2 = l.copy() → [1, 2, 3]` |
---

  
###  `Extra Problem Definition`

+ Problem Definition with Solution: Problem: Replace odd numbers in a list with 0. <br> Solution:

```
l = [1, 2, 3, 4]
ans = [i if i % 2 == 0 else 0 for i in l]
print(ans)

# Output: [0, 2, 0, 4]
```

<br><br><br><br>

---

## 2 | Copy
### `🧬 Shallow vs. Deep Copy`

Description: Copying in Python refers to creating a duplicate of an object. There are three types of copying: shallow copy, deep copy, and reference assignment.

Types of Copy:

+ Shallow Copy: Creates a new object but copies references of nested objects. Changes to nested objects affect both the original and the copy.

  Example:
<br>

```
l1 = [10, 20, [30, 40]]
shallow_copy = l1.copy()
shallow_copy[2].append(50)
print(l1)
# Output: [10, 20, [30, 40, 50]]

print(shallow_copy)
# Output: [10, 20, [30, 40, 50]]
```

+ Deep Copy: Creates a new object and recursively copies all nested objects. Changes to nested objects do not affect the original.
  
  Example:
<br>

```
import copy
l1 = [10, 20, [30, 40]]
deep_copy = copy.deepcopy(l1)
deep_copy[2].append(50)
print(l1)
# Output: [10, 20, [30, 40]]

print(deep_copy)
# Output: [10, 20, [30, 40, 50]]
```

+ Reference Assignment: Both variables point to the same object. Changes to one affect the other. Example:

```
l1 = [10, 20, [30, 40]]
ref_copy = l1
ref_copy.append(50)
print(l1)
# Output: [10, 20, [30, 40], 50]

print(ref_copy)
# Output: [10, 20, [30, 40], 50]
```

---

<br><br><br><br>

## 📦 3. Tuple

**Description:**  A tuple in Python is an **immutable**, **ordered** collection of elements.  
+ Tuples are created using parentheses `()` or the `tuple()` constructor.

### 🔹 Tuple Packing and Unpacking

#### 📥 Packing  
Assigning multiple values to a single tuple variable.

```python
t = 1, 2, 3, 4
print(t)

# Output: (1, 2, 3, 4)
```

📤 Unpacking
Assigning tuple elements to individual variables.
```
t = (1, 2, 3, 4)
a, b, c, d = t
print(a, b, c, d)

# Output: 1 2 3 4
```

### `🛠️ In-built Functions of Tuple`


| Function	| Description	| Example | 
| :--- | :--- | :--- |
| `count(x)` | Returns the number of occurrences of the specified element.	| `t = (1, 2, 2, 3); print(t.count(2)) → 2` |
| `index(x)` |	Returns the index of the first occurrence of the specified element.	| `t = (1, 2, 3); print(t.index(2)) → 1` |
---

---

<br><br><br><br>

## 🔢 4. Set

**Description:**  
A set in Python is an **unordered** collection of **unique** elements.  
+ Sets are **mutable**, but they do **not allow duplicate values**.  
+ Sets are created using curly braces `{}` or the `set()` constructor.

---

### 🔹 Set Creation Methods

#### 1️⃣ Using Curly Braces `{}`

```python
s = {1, 2, 3}
print(s)

# Output: {1, 2, 3}

2️⃣ Using set() Constructor
s = set([1, 2, 3])
print(s)

# Output: {1, 2, 3}
```

### `🛠️ In-built Functions of Set`


| Function | Signature | Example |
| :--- | :--- | :---: |
| `Add` | `add(element)` | Adds a single element {17, 26}. |
| `Update` | `update(iterable)` | Adds multiple elements {18, 26}. |
| `Remove` | `remove(element)` | **Raises KeyError** if not found {20, 26}. |
| `Discard` | `discard(element)`| **No error** if not found-> {22, 26]. |
| `Pop` | `pop()` | Removes/returns an arbitrary element ->{24, 26}. |
| `Clear` | `clear()` | Removes all elements -> {25, 27}. |

---

## 📖 4. Dictionaries
[cite_start]Dictionaries store data in **Key-Value** pairs[cite: 27, 28].

### 🏗️ Creation Methods
1.  [cite_start]**Braces:** `{1: "One"}` [cite: 28]
2.  [cite_start]**`dict()`:** `dict([(1, "One")])` [cite: 29]
3.  [cite_start]**`zip()`:** `dict(zip([1], ["One"]))` [cite: 29]
4.  [cite_start]**`enumerate()`:** `dict(enumerate(["One"], start=1))` [cite: 29]

### 🔧 Key Methods
* [cite_start]**`keys() / values() / items()`**: View keys, values, or (key, value) tuples[cite: 30, 31, 32].
* [cite_start]**`get(key, default)`**: Safely gets a value; returns default if key is missing[cite: 33].
* [cite_start]**`setdefault(key, val)`**: Returns value; sets it to `val` if key is missing[cite: 34].
* [cite_start]**`popitem()`**: Removes and returns the last key-value pair[cite: 40].

---

## 🚀 5. Comprehensions
[cite_start]A concise way to create new collections[cite: 41].

| Type | Syntax Example |
| :--- | :--- |
| **List** | `[i**2 for i in range(5)]` |
| **Tuple** | `tuple(i**2 for i in range(5))` |
| **Set** | `{i**2 for i in range(5)}` |
| **Dict** | `{i: i**2 for i in range(5)}` |

![Wave](https://capsule-render.vercel.app/api?type=waving&color=0:00c6ff,100:0072ff&height=120&section=footer)
