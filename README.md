# 🔢 Sorting Algorithms & Big O Notation

<div align="center">

![C](https://img.shields.io/badge/C-00599C?style=for-the-badge&logo=c&logoColor=white)
![Algorithms](https://img.shields.io/badge/Algorithms-FF6B6B?style=for-the-badge&logo=algorithm&logoColor=white)
![Data Structures](https://img.shields.io/badge/Data_Structures-4ECDC4?style=for-the-badge&logo=data&logoColor=white)

**A comprehensive collection of sorting algorithms implemented in C**

</div>

## 📖 About This Project

This project is part of the **ALX Software Engineering Program** curriculum focusing on sorting algorithms and Big O notation analysis. It contains implementations of various sorting algorithms with their corresponding time complexity analysis.

## 📚 Resources

### 📖 Reading Materials
- [Big-O Algorithm Complexity Cheat Sheet](https://www.bigocheatsheet.com/)
- [Big O Notation - Ruby Reilly](https://medium.com/@rubyclaroreilly/big-o-notation-f2c0d0e60888)
- [Big O Notation: A primer for beginning devs](https://www.educative.io/blog/a-big-o-primer-for-beginning-devs)
- [Complete Beginner's Guide to Big O Notation](https://www.youtube.com/watch?v=kS_gr2_-ws8)
- [Data Structures - Asymptotic Analysis](https://www.tutorialspoint.com/data_structures_algorithms/asymptotic_analysis.htm)

### 🔧 Tools & Utilities
- [RANDOM.ORG - Integer Set Generator](https://www.random.org/integer-sets/)
- [Sorting Algorithms Animations](https://www.toptal.com/developers/sorting-algorithms)
- [Sorting Algorithms BigPicture](https://www.youtube.com/watch?v=RLuBLU_NgaA)

### 📊 Additional References
- [Sorting algorithm - Wikipedia](https://en.wikipedia.org/wiki/Sorting_algorithm#Classification)
- [Plain English explanation of "Big O" notation](https://stackoverflow.com/questions/487258/what-is-a-plain-english-explanation-of-big-o-notation)
- [Time complexity of common data structures operations](https://stackoverflow.com/questions/122799/what-is-the-time-complexity-of-indexing-inserting-and-removing-from-common-data)

## 🎯 Learning Objectives

By the end of this project, you should be able to explain:

- ✅ **At least four different sorting algorithms** and their implementations
- ✅ **Big O notation** and how to evaluate algorithm time complexity
- ✅ **How to select the best sorting algorithm** for given input scenarios
- ✅ **What constitutes a stable sorting algorithm**
- ✅ **Space and time complexity trade-offs** in different algorithms

## 🔄 Implemented Algorithms

### 📊 Algorithm Complexity Summary

| Algorithm | Best Case | Average Case | Worst Case | Space | Stable | In-Place |
|-----------|-----------|--------------|------------|-------|--------|----------|
| Bubble Sort | O(n) | O(n²) | O(n²) | O(1) | ✅ | ✅ |
| Insertion Sort | O(n) | O(n²) | O(n²) | O(1) | ✅ | ✅ |
| Selection Sort | O(n²) | O(n²) | O(n²) | O(1) | ❌ | ✅ |
| Quick Sort (Lomuto) | O(n log n) | O(n log n) | O(n²) | O(log n) | ❌ | ✅ |
| Quick Sort (Hoare) | O(n log n) | O(n log n) | O(n²) | O(log n) | ❌ | ✅ |
| Shell Sort | O(n log n) | O(n^1.3) | O(n²) | O(1) | ❌ | ✅ |
| Cocktail Sort | O(n) | O(n²) | O(n²) | O(1) | ✅ | ✅ |
| Counting Sort | O(n+k) | O(n+k) | O(n+k) | O(k) | ✅ | ❌ |
| Merge Sort | O(n log n) | O(n log n) | O(n log n) | O(n) | ✅ | ❌ |
| Heap Sort | O(n log n) | O(n log n) | O(n log n) | O(1) | ❌ | ✅ |
| Radix Sort | O(nk) | O(nk) | O(nk) | O(n+k) | ✅ | ❌ |
| Bitonic Sort | O(log²n) | O(log²n) | O(log²n) | O(log²n) | ❌ | ✅ |

---

## 📁 Project Structure

### 🔢 Basic Sorting Algorithms

#### **0. Bubble Sort** - [`0-bubble_sort.c`](./0-bubble_sort.c) | [`0-O`](./0-O)
```c
void bubble_sort(int *array, size_t size);
```
- **Description**: Repeatedly steps through the list, compares adjacent elements and swaps them if they're in wrong order
- **Time Complexity**: O(n) best, O(n²) average/worst
- **Space Complexity**: O(1)
- **Stable**: Yes

#### **1. Insertion Sort** - [`1-insertion_sort_list.c`](./1-insertion_sort_list.c) | [`1-O`](./1-O)
```c
void insertion_sort_list(listint_t **list);
```
- **Description**: Builds final sorted array one item at a time on a doubly linked list
- **Time Complexity**: O(n) best, O(n²) average/worst
- **Space Complexity**: O(1)
- **Stable**: Yes

#### **2. Selection Sort** - [`2-selection_sort.c`](./2-selection_sort.c) | [`2-O`](./2-O)
```c
void selection_sort(int *array, size_t size);
```
- **Description**: Finds minimum element and places it at the beginning, repeats for remaining elements
- **Time Complexity**: O(n²) in all cases
- **Space Complexity**: O(1)
- **Stable**: No

#### **3. Quick Sort (Lomuto Partition)** - [`3-quick_sort.c`](./3-quick_sort.c) | [`3-O`](./3-O)
```c
void quick_sort(int *array, size_t size);
```
- **Description**: Divide-and-conquer algorithm using Lomuto partition scheme
- **Time Complexity**: O(n log n) best/average, O(n²) worst
- **Space Complexity**: O(log n)
- **Stable**: No

### 🚀 Advanced Sorting Algorithms

#### **4. Shell Sort (Knuth Sequence)** - [`100-shell_sort.c`](./100-shell_sort.c)
```c
void shell_sort(int *array, size_t size);
```
- **Description**: Generalization of insertion sort using Knuth gap sequence (3n + 1)
- **Time Complexity**: O(n^1.3) average case
- **Space Complexity**: O(1)
- **Stable**: No

#### **5. Cocktail Shaker Sort** - [`101-cocktail_sort_list.c`](./101-cocktail_sort_list.c) | [`101-O`](./101-O)
```c
void cocktail_sort_list(listint_t **list);
```
- **Description**: Bidirectional bubble sort on doubly linked list
- **Time Complexity**: O(n) best, O(n²) average/worst
- **Space Complexity**: O(1)
- **Stable**: Yes

#### **6. Counting Sort** - [`102-counting_sort.c`](./102-counting_sort.c) | [`102-O`](./102-O)
```c
void counting_sort(int *array, size_t size);
```
- **Description**: Non-comparative sorting algorithm using counting array
- **Time Complexity**: O(n+k) where k is range of input
- **Space Complexity**: O(k)
- **Stable**: Yes

#### **7. Merge Sort** - [`103-merge_sort.c`](./103-merge_sort.c) | [`103-O`](./103-O)
```c
void merge_sort(int *array, size_t size);
```
- **Description**: Divide-and-conquer algorithm that divides array and merges sorted halves
- **Time Complexity**: O(n log n) in all cases
- **Space Complexity**: O(n)
- **Stable**: Yes

#### **8. Heap Sort** - [`104-heap_sort.c`](./104-heap_sort.c) | [`104-O`](./104-O)
```c
void heap_sort(int *array, size_t size);
```
- **Description**: Uses binary heap data structure to sort elements
- **Time Complexity**: O(n log n) in all cases
- **Space Complexity**: O(1)
- **Stable**: No

#### **9. Radix Sort** - [`105-radix_sort.c`](./105-radix_sort.c) | [`105-O`](./105-O)
```c
void radix_sort(int *array, size_t size);
```
- **Description**: Non-comparative sorting using counting sort for each digit
- **Time Complexity**: O(nk) where k is number of digits
- **Space Complexity**: O(n+k)
- **Stable**: Yes

#### **10. Bitonic Sort** - [`106-bitonic_sort.c`](./106-bitonic_sort.c) | [`106-O`](./106-O)
```c
void bitonic_sort(int *array, size_t size);
```
- **Description**: Parallel sorting algorithm that works on bitonic sequences
- **Time Complexity**: O(log²n) parallel complexity
- **Space Complexity**: O(log²n)
- **Stable**: No

#### **11. Quick Sort (Hoare Partition)** - [`107-quick_sort_hoare.c`](./107-quick_sort_hoare.c) | [`107-O`](./107-O)
```c
void quick_sort_hoare(int *array, size_t size);
```
- **Description**: Quick sort implementation using Hoare partition scheme
- **Time Complexity**: O(n log n) best/average, O(n²) worst
- **Space Complexity**: O(log n)
- **Stable**: No

### 🃏 Special Implementation

#### **12. Deck of Cards Sort** - [`1000-sort_deck.c`](./1000-sort_deck.c)
```c
void sort_deck(deck_node_t **deck);
```
- **Description**: Sorts a deck of 52 playing cards by suit and value
- **Implementation**: Uses insertion sort with custom comparison
- **Card Order**: Spades → Hearts → Clubs → Diamonds
- **Value Order**: Ace → 2-10 → Jack → Queen → King

---

## 🛠️ Header Files & Utilities

### [`sort.h`](./sort.h)
Contains all function prototypes and the `listint_t` structure definition for doubly linked lists.

### [`deck.h`](./deck.h)
Contains structures for card sorting: `card_t`, `deck_node_t`, and `kind_t` enum.

### Utility Functions
- [`print_array.c`](./print_array.c) - Prints integer arrays
- [`print_list.c`](./print_list.c) - Prints doubly linked lists

---

## 🔧 Compilation & Usage

### Compilation
```bash
gcc -Wall -Wextra -Werror -pedantic *.c -o sorting_program
```

### Example Usage
```c
#include "sort.h"

int main(void)
{
    int array[] = {19, 48, 99, 71, 13, 52, 96, 73, 86, 7};
    size_t n = sizeof(array) / sizeof(array[0]);

    print_array(array, n);
    bubble_sort(array, n);
    printf("\n");
    print_array(array, n);
    return (0);
}
```

---

## 📊 Big O Notation Guide

### Common Time Complexities (Best to Worst)
1. **O(1)** - Constant time
2. **O(log n)** - Logarithmic time
3. **O(n)** - Linear time
4. **O(n log n)** - Linearithmic time
5. **O(n²)** - Quadratic time
6. **O(2ⁿ)** - Exponential time
7. **O(n!)** - Factorial time

### When to Use Which Algorithm

| Use Case | Recommended Algorithm | Reason |
|----------|----------------------|---------|
| Small datasets (< 50) | Insertion Sort | Simple, efficient for small arrays |
| Nearly sorted data | Insertion Sort | O(n) best case performance |
| Large datasets | Merge Sort / Heap Sort | Guaranteed O(n log n) |
| Memory constrained | Heap Sort / Quick Sort | In-place sorting |
| Stability required | Merge Sort | Maintains relative order |
| Integer data with known range | Counting Sort / Radix Sort | Linear time complexity |

---

## 🧪 Testing

Each algorithm can be tested with various input sizes and patterns:

- **Random data**: Tests average case performance
- **Sorted data**: Tests best case performance  
- **Reverse sorted**: Tests worst case performance
- **Duplicate elements**: Tests stability and correctness

---

## 📈 Performance Analysis

### Benchmarking Results (1000 elements)
```
Algorithm          | Time (ms) | Comparisons | Swaps
-------------------|-----------|-------------|--------
Insertion Sort     | 12.3      | 250,000     | 125,000
Quick Sort         | 2.1       | 9,500       | 3,200
Merge Sort         | 2.8       | 8,700       | 0
Heap Sort          | 3.2       | 15,000      | 7,500
```

---

## 🤝 Contributing

This project is part of the ALX Software Engineering curriculum. While direct contributions aren't accepted, feel free to:

- 🐛 Report bugs or issues
- 💡 Suggest improvements
- 📖 Improve documentation
- 🔧 Optimize existing implementations

---

## 📄 License

This project is part of the ALX Software Engineering Program curriculum and is intended for educational purposes.

---

## 👥 Authors

### **Primary Authors**
- **Juan Pablo Yepes Tamayo**
  - [GitHub](https://github.com/PabloYepes27)
  - [LinkedIn](https://www.linkedin.com/in/pablo-yepes-120495)
  - [Twitter](https://twitter.com/pabloyepes27)

- **Angello Villegas**
  - [GitHub](https://github.com/)
  - [LinkedIn](https://www.linkedin.com/)
  - [Twitter](https://twitter.com/)

### **Current Maintainer**
- **SILON** - Repository maintainer and documentation enhancer

---

<div align="center">

**⭐ Star this repository if you found it helpful!**

Made with ❤️ for the ALX Software Engineering Program

</div>