# 01_intro_to_programming_for_beginners

## How Numbers Started

- Around **100,000 years ago**, humans didn't have a proper number system.
- One of the earliest counting methods was the **tally mark system**.
- Example:
  - Each goat was matched with one stone.
  - If `stone count == goat count`, then all goats were present.

- This was simple but not practical for large numbers.

## Early Number Systems

- One of the early number systems was used by the **Egyptians**.
- Another important ancient system was the **Babylonian Base-60 (Sexagesimal)** number system.
- These systems worked, but they were not as efficient as the modern decimal system.

## Decimal Number System (Base 10)

- The modern decimal number system uses digits:

```text
0 1 2 3 4 5 6 7 8 9
```

- Total digits = **10**
- Base = **10**
- The concept of **0** and the decimal number system was developed in **India**.

---

## Why Computers Were Needed

- The main task of a computer is to **calculate things**.
- Earlier, computers were huge machines.
- They needed many people to operate.
- They were accurate, but they were not very fast.

---

## Transistor Revolution

- A major revolution came with the invention of the **transistor**.
- It replaced large vacuum tubes and made computers:
  - Smaller
  - Faster
  - More reliable
  - More power-efficient

---

## Binary Number System

A transistor has two states:

- ON → `1`
- OFF → `0`

Because of this, computers understand only two values:

```text
0 and 1
```

This is called the **Binary Number System**.

- Base = **2**
- Digits = `0` and `1`

---

## Number Systems

| Number System | Base | Digits   |
| ------------- | ---: | -------- |
| Binary        |    2 | 0, 1     |
| Octal         |    8 | 0–7      |
| Decimal       |   10 | 0–9      |
| Hexadecimal   |   16 | 0–9, A–F |

---

## Number System Conversion

### Decimal → Binary

Method:

- Keep dividing the number by **2**.
- Write down each remainder.
- Read the remainders **from bottom to top**.

Example: Convert `13` to binary.

| Division   | Remainder |
| ---------- | --------: |
| 13 ÷ 2 = 6 |         1 |
| 6 ÷ 2 = 3  |         0 |
| 3 ÷ 2 = 1  |         1 |
| 1 ÷ 2 = 0  |         1 |

Result:

```text
13₁₀ = 1101₂
```

---

### Binary → Decimal

Multiply each bit by its power of 2.

Example:

```text
1101₂
```

Calculation:

```text
1 × 2³ = 8
1 × 2² = 4
0 × 2¹ = 0
1 × 2⁰ = 1

8 + 4 + 0 + 1 = 13
```

Result:

```text
1101₂ = 13₁₀
```

---

### Decimal → Octal

Keep dividing by **8**.

Example: Convert `83`.

| Division    | Remainder |
| ----------- | --------: |
| 83 ÷ 8 = 10 |         3 |
| 10 ÷ 8 = 1  |         2 |
| 1 ÷ 8 = 0   |         1 |

Result:

```text
83₁₀ = 123₈
```

---

### Octal → Decimal

Example:

```text
123₈
```

Calculation:

```text
1 × 8² = 64
2 × 8¹ = 16
3 × 8⁰ = 3

64 + 16 + 3 = 83
```

Result:

```text
123₈ = 83₁₀
```

---

### Decimal → Hexadecimal

Keep dividing by **16**.

Example: Convert `26`.

| Division    | Remainder |
| ----------- | --------: |
| 26 ÷ 16 = 1 |    10 = A |
| 1 ÷ 16 = 0  |         1 |

Result:

```text
26₁₀ = 1A₁₆
```

---

### Hexadecimal → Decimal

Example:

```text
1A₁₆
```

Calculation:

```text
1 × 16¹ = 16
A = 10

10 × 16⁰ = 10

16 + 10 = 26
```

Result:

```text
1A₁₆ = 26₁₀
```

---

### Binary → Octal

- Group bits into **3** from right to left.

Example:

```text
110101₂
```

```text
110 101
```

```text
110 = 6
101 = 5
```

Result:

```text
110101₂ = 65₈
```

---

### Octal → Binary

Replace every octal digit with **3 binary bits**.

Example:

```text
65₈
```

```text
6 = 110
5 = 101
```

Result:

```text
65₈ = 110101₂
```

---

### Binary → Hexadecimal

Group bits into **4** from right to left.

Example:

```text
11101010₂
```

```text
1110 1010
```

```text
1110 = E
1010 = A
```

Result:

```text
11101010₂ = EA₁₆
```

---

### Hexadecimal → Binary

Replace each hexadecimal digit with **4 binary bits**.

Example:

```text
2F₁₆
```

```text
2 = 0010
F = 1111
```

Result:

```text
2F₁₆ = 00101111₂
```

---

## BCD (Binary Coded Decimal)

BCD stores **each decimal digit separately** using 4 bits.

Example:

Decimal:

```text
59
```

Binary of the whole number:

```text
59 = 111011₂
```

BCD:

```text
5 = 0101
9 = 1001

BCD = 0101 1001
```

So:

```text
59 (Binary) = 111011₂
59 (BCD)    = 0101 1001
```

---

## Homework

- Convert `25` from Decimal to Binary.
- Convert `111101₂` to Decimal.
- Convert `145₈` to Decimal.
- Convert `255₁₀` to Hexadecimal.
- Convert `7B₁₆` to Decimal.
- Convert `10111010₂` to Hexadecimal.
- Convert `A5₁₆` to Binary.
- Convert `94` into BCD.

## Excess Code (XS-3 Code)

Excess-3 (XS-3) is a **non-weighted Binary Coded Decimal (BCD)** code.

Rule:

- Add **3** to every decimal digit.
- Convert the result to **4-bit binary**.

---

### Decimal → Excess-3

#### Example 1: Convert `5`

Step 1:

```text
5 + 3 = 8
```

Step 2:

```text
8 = 1000₂
```

Result:

```text
5 → 1000 (Excess-3)
```

---

#### Example 2: Convert `29`

Convert each digit separately.

Digit `2`

```text
2 + 3 = 5
5 = 0101
```

Digit `9`

```text
9 + 3 = 12
12 = 1100
```

Result:

```text
29 → 0101 1100
```

---

#### Example 3: Convert `483`

```text
4 + 3 = 7  → 0111
8 + 3 = 11 → 1011
3 + 3 = 6  → 0110
```

Result:

```text
483 → 0111 1011 0110
```

---

### Excess-3 → Decimal

Rule:

- Split into **4-bit groups**.
- Convert each group to decimal.
- Subtract **3** from each digit.

### Example 1

```text
1000
```

```text
1000₂ = 8

8 - 3 = 5
```

Result:

```text
1000 → 5
```

---

#### Example 2

```text
0101 1100
```

First group:

```text
0101 = 5

5 - 3 = 2
```

Second group:

```text
1100 = 12

12 - 3 = 9
```

Result:

```text
0101 1100 → 29
```

---

### Example 3

```text
0111 1011 0110
```

```text
0111 = 7  → 7 - 3 = 4
1011 = 11 → 11 - 3 = 8
0110 = 6  → 6 - 3 = 3
```

Result:

```text
0111 1011 0110 → 483
```

---

### Difference Between Binary, BCD, and Excess-3

| Decimal | Binary |    BCD    | Excess-3  |
| ------: | :----: | :-------: | :-------: |
|       5 |  101   |   0101    |   1000    |
|       9 |  1001  |   1001    |   1100    |
|      25 | 11001  | 0010 0101 | 0101 1000 |
|      59 | 111011 | 0101 1001 | 1000 1100 |

---
