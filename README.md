# FACTORIAL-OF-A-NUMBER
# FACTORIAL OF A NUMBER USING 8051 (Keil)

## AIM
To write and execute an Assembly language program to perform the factorial of a number using 8051 Keil.

---

## APPARATUS REQUIRED
- Personal computer with Keil software

---

## ALGORITHM
1. **Start**
2. **Input**: Read the number `n`.
3. **Initialize**:
   - Set factorial to `1`.
   - Set `i` to `1`.
4. **Loop**: While `i` is less than or equal to `n`:
   - Multiply factorial by `i`.
   - Increment `i` by `1`.
5. **Output**: Store or print the value of factorial.
6. **End**

---

## FLOWCHART
<img width="506" height="525" alt="image" src="https://github.com/user-attachments/assets/f3b47187-6f0f-490c-8704-f2973cb2b276" />


---

## PROGRAM
```asm
ORG 0000H
MOV DPTR,#4500H
MOVX A,@DPTR
MOV R0,A
INC DPTR
ACALL FACTORIAL
MOVX @DPTR,A
SJMP THIN
FACTORIAL:DEC R0
CJNE R0,#01H,PRODUCT
SJMP THICK
PRODUCT:MOV B,R0
MUL AB
ACALL FACTORIAL
THICK: RET
THIN:RET
END


```
OUTPUT

OUTPUT Input: 05H Output: 78H

In Keil, after execution:

Memory Location 4500H : 05H Memory Location 4501H : 78H

So,

5! = 120 (decimal) = 78H


---
MANUAL CALCULATIONS
MANUAL CALCULATIONS Given number = 5

Factorial of 5:

5! = 5 × 4 × 3 × 2 × 1

= 20 × 3 × 2 × 1

= 60 × 2 × 1

= 120

Therefore,

5! = 120 (decimal) = 78H


---

RESULT

Thus, the factorial of a number was calculated and executed successfully using 8051 Keil.

---


