# 🐍 Python Data Structures: Master Summary
> A comprehensive guide to Lists, Tuples, Sets, and Dictionaries in Python.

---



## 📋 1. Lists
Lists are ordered, mutable sequences.

### 🛠️ Core Functions
| Function | Description | Example |
| :--- | :--- | :--- |
| `append(x)` | [cite_start] Adds an element to the end[cite: 1]. | [cite_start]`[1, 2].append(3)` → `[1, 2, 3]` [cite: 2] |
| `extend(i)` | [cite_start] Adds elements of an iterable to the end[cite: 2]. | [cite_start]`[1].extend([2, 3])` → `[1, 2, 3]` [cite: 3] |
| `insert(i, x)` | [cite_start] Inserts element at specific index[cite: 3]. | [cite_start]`[1, 3].insert(1, 2)` → `[1, 2, 3]` [cite: 4] |
| `copy()` | [cite_start] Creates a shallow copy[cite: 4]. | [cite_start]`l1.copy()` [cite: 5] |

### 🧬 Shallow vs. Deep Copy
* [cite_start]**Shallow Copy:** Copies the outer list but references the same inner mutable objects[cite: 5]. [cite_start]Changes to nested objects affect the copy[cite: 6, 7].
* [cite_start]**Deep Copy:** Creates a completely independent copy, including all nested objects[cite: 8]. [cite_start]Changes to the original do not affect the copy[cite: 8, 9].

---

## 💎 2. Tuples
[cite_start]Tuples are **immutable** sequences[cite: 10].

* [cite_start]**Definition:** Uses `()` or `tuple()`[cite: 10].
* [cite_start]**Packing:** Assigning multiple values to one variable (e.g., `t = 1, 2, 3`)[cite: 12].
* [cite_start]**Unpacking:** Extracting values into individual variables (e.g., `a, b, c = t`)[cite: 13].

### 🔍 Methods
* [cite_start]**`count(x)`**: Returns the number of occurrences of `x`[cite: 14].
* [cite_start]**`index(x)`**: Returns the index of the first occurrence of `x`[cite: 15].

---

## 🎡 3. Sets
[cite_start]Sets are unordered collections of **unique** elements[cite: 15, 16].

### ⚡ Operations Comparison
| Function | Signature | Error Handling |
| :--- | :--- | :--- |
| **Add** | `add(element)` | [cite_start]Adds a single element[cite: 17, 26]. |
| **Update** | `update(iterable)` | [cite_start]Adds multiple elements[cite: 18, 26]. |
| **Remove** | `remove(element)` | [cite_start]**Raises KeyError** if not found[cite: 20, 26]. |
| **Discard** | `discard(element)` | [cite_start]**No error** if not found[cite: 22, 26]. |
| **Pop** | `pop()` | [cite_start]Removes/returns an arbitrary element[cite: 24, 26]. |
| **Clear** | `clear()` | [cite_start]Removes all elements[cite: 25, 27]. |

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
