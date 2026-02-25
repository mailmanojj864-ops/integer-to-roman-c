# 🏛 Integer to Roman (C Implementation)

This repository contains a C solution to the **Integer to Roman** problem (LeetCode - Medium).

The solution converts a given integer (1 ≤ num ≤ 3999) into its corresponding Roman numeral using an optimized Greedy Algorithm approach.

---

## 📌 Problem Statement

Roman numerals are represented by seven different symbols:

| Symbol | Value |
|--------|--------|
| I      | 1      |
| V      | 5      |
| X      | 10     |
| L      | 50     |
| C      | 100    |
| D      | 500    |
| M      | 1000   |

Roman numerals are formed by appending values from highest to lowest, including special subtractive cases:

- 4 → IV  
- 9 → IX  
- 40 → XL  
- 90 → XC  
- 400 → CD  
- 900 → CM  

---

## 🚀 Approach

This solution uses a **Greedy Algorithm**:

1. Maintain two arrays:
   - Integer values (including subtractive values)
   - Corresponding Roman symbols
2. Traverse from largest to smallest value.
3. While the number is greater than or equal to the current value:
   - Append the Roman symbol
   - Subtract the value from the number
4. Repeat until the number becomes 0.

This guarantees the correct Roman numeral representation.

---

## 🧠 Algorithm Design

We use a pre-defined mapping:

```
1000 → M
900  → CM
500  → D
400  → CD
100  → C
90   → XC
50   → L
40   → XL
10   → X
9    → IX
5    → V
4    → IV
1    → I
```

The algorithm iteratively reduces the number using the largest possible Roman value.

---

## ⏱ Time Complexity

**O(1)**

- The maximum input value is 3999.
- The number of Roman symbols is fixed (13 values).
- Therefore, execution time is constant.

---

## 💾 Space Complexity

**O(1)**

- The output string has a bounded maximum size (Roman representation of 3999 is less than 20 characters).
- No extra dynamic data structures are used.

---

## 🛠 Technologies Used

- C Programming Language
- Standard Library Functions (`malloc`, `strcat`)

---

## 📎 Example

### Input:
```
num = 1994
```

### Output:
```
MCMXCIV
```

---

## 🎯 Key Learning Outcomes

- Greedy algorithm design
- Handling subtractive numeral cases
- Efficient string construction in C
- Clean and modular problem-solving approach
