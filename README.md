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
<img width="1920" height="1200" alt="Screenshot (40)" src="https://github.com/user-attachments/assets/5fed39e1-2fa3-40a6-855d-83cd088f76c4" />

<img width="1411" height="167" alt="Screenshot 2025-11-02 143937" src="https://github.com/user-attachments/assets/09c7c60b-726c-4938-bb4c-c1ee13e80f58" />

---
MANUAL CALCULATIONS
![fact_calculation](https://github.com/user-attachments/assets/db0ec196-d8e5-4fb6-8944-ad50bcbc27c9)


RESULT

Thus, the factorial of a number was calculated and executed successfully using 8051 Keil.

---


