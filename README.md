# Assignment 3 — ADS (QuickSort Implementation)

## Overview

This project is a Java console application that implements the **QuickSort algorithm** using a recursive divide-and-conquer approach.

The program:

- Reads an array size from the user
- Accepts integer elements
- Sorts the array using QuickSort
- Prints the sorted result

The sorting logic is implemented manually without using built-in sorting utilities.

---

## Project Structure

```

ADS-3-assignment-master/
│
├── src/
│   └── Main.java
│
├── ADS 3 assignment.iml

```

All logic is implemented in:

```

src/Main.java

````

---

## Algorithm Details

### QuickSort Strategy

- Uses **last element as pivot**
- Partitions the array into:
  - Elements smaller than pivot
  - Elements greater than or equal to pivot
- Recursively sorts left and right subarrays

---

## Implemented Methods

### `quickSort(int[] array)`

Public method that starts sorting:

```java
sort(array, 0, array.length - 1);
````

---

### `sort(int[] array, int low, int high)`

Recursive method:

* Checks if `low < high`
* Finds pivot index using `partition`
* Recursively sorts:

  * Left subarray
  * Right subarray

---

### `partition(int[] array, int low, int high)`

Partition logic:

* Pivot = `array[high]`
* Moves all elements smaller than pivot to the left
* Places pivot in correct sorted position
* Returns pivot index

---

### `swap(int[] array, int i, int j)`

Utility method for swapping elements.

---

## How It Works

### Step 1 — Input

The program asks:

```
Enter Array size:
```

Then reads array elements:

```
Enter elements of array:
```

Example input:

```
Enter Array size: 5
Enter elements of array:
4 2 7 1 3
```

---

### Step 2 — Sorting

QuickSort is executed:

```java
quickSort(numbers);
```

---

### Step 3 — Output

Program prints:

```
Sorted Array:
1 2 3 4 7
```

---

## Time Complexity

| Case       | Complexity |
| ---------- | ---------- |
| Best Case  | O(n log n) |
| Average    | O(n log n) |
| Worst Case | O(n²)      |

Worst case occurs when the array is already sorted and pivot selection is poor (since last element is used as pivot).

---

## How to Run

### Compile

```bash
javac src/Main.java
```

### Run

```bash
java -cp src Main
```

Or run directly from an IDE (e.g., IntelliJ IDEA).

---

## Technologies Used

* Java
* Standard Library (`java.util.Scanner`)
* Manual implementation of QuickSort algorithm

---

## Purpose

This project was created as part of an **Algorithms and Data Structures (ADS)** assignment to demonstrate:

* Understanding of QuickSort
* Recursive divide-and-conquer approach
* Partition-based sorting
* In-place array manipulation
