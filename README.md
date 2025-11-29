# Arithmetic-operation-using-8086
# 8086 Assembly Language Programs for Arithmetic Operations

## AIM

To write and execute Assembly Language Programs to perform arithmetic operations for the 8086 microprocessor.

---

## APPARATUS REQUIRED

* Personal Computer with MASM Software

---

## 1. ADDITION

#### Algorithm

1. Initialize memory location in HL register.
2. Store 1st data.
3. Increment HL to enter 2nd data.
4. Move 2nd number to accumulator.
5. Decrement HL.
6. Add value in memory with accumulator.
7. Store result.
8. Stop.


## FLOW CHART
<img width="707" height="1024" alt="image" src="https://github.com/user-attachments/assets/b5a7062d-e294-47cd-9683-a40de25e82de" />


#### Program

```asm
CODE SEGMENT
ASSUME CS: CODE, DS: CODE
ORG 1000H
MOV SI,2000H
MOV CL,00H
MOV AX,[SI]
MOV BX,[SI+02H]
ADD AX,BX
JNC L1
INC CL
L1:
MOV [SI+04H],AX
MOV [SI+06H],CL
MOV AH,4CH
INT 21H
CODE ENDS
END
```

#### Output Table

| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| ----------------------- | ------------------------ |
|        1200=12                 |        1204=24                  |
|1201=34|
|1202=12|1205=68|
|1203=34|
#### Manual Calculations

![WhatsApp Image 2025-09-06 at 13 05 23_1ff23fc2](https://github.com/user-attachments/assets/398617e0-d9a2-4d4d-b5a4-6449aab45080)


---

## OUTPUT IMAGE FROM MASM SOFTWARE
<img width="640" height="282" alt="Screenshot 2025-09-06 114149" src="https://github.com/user-attachments/assets/c72ab401-0c17-4abc-a6e9-e9222f17535f" />

## 2. SUBTRACTION

#### Algorithm

1. Initialize memory and store 1st data.
2. Increment to get 2nd data.
3. Move 2nd data to accumulator.
4. Subtract memory content.
5. Store result.

## FLOWCHART

<img width="578" height="797" alt="image" src="https://github.com/user-attachments/assets/564c3c7a-33ce-4a1c-8920-beb5c24b9b47" />


#### Program
```asm
CODE SEGMENT
ASSUME CS: CODE, DS: CODE
ORG 1000H
MOV SI,2000H
MOV CL,00H
MOV AX,[SI]
MOV BX,[SI+02H]
SUB AX,BX
JNC L1
INC CL
L1:
MOV [SI+04H],AX
MOV [SI+06H],CL
MOV AH,4CH
INT 21H
CODE ENDS
END
```

#### Output Table

| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| ----------------------- | ------------------------ |
 1200=12                 |        1204=00                |
|1201=34|
|1202=12|1205=00|
|1203=34|

#### Manual Calculations

![WhatsApp Image 2025-09-06 at 13 05 23_e79a7a7a](https://github.com/user-attachments/assets/c48605ef-80de-4511-a400-d2a5a1943768)


---


## OUTPUT SCREEN FROM MASM SOFTWARE
<img width="635" height="267" alt="Screenshot 2025-09-06 114539" src="https://github.com/user-attachments/assets/565050dc-4489-4440-8949-b0ff36021fd0" />

## 3. MULTIPLICATION

#### Algorithm

1. Initialize memory and store operands.
2. Move operands to registers.
3. Multiply.
4. Store result.

##FLOWCHART

<img width="569" height="906" alt="image" src="https://github.com/user-attachments/assets/88be88ff-2896-4a88-b73d-84ccffd2fcf9" />



#### Program

```asm
CODE SEGMENT
ASSUME CS: CODE, DS: CODE
ORG 1000H
MOV SI,2000H
MOV DX,0000H
MOV AX,[SI]
MOV BX,[SI+02H]
MUL BX
MOV [SI+04H],AX
MOV [SI+06H],DX
MOV AH,4CH
INT 21H
CODE ENDS
END
```

#### Output Table

| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| ----------------------- | ------------------------ |
 1200=12                 |        1204=44                 |
|1201=34|1205=51
|1202=12|1206=97|
|1203=34|1207=0A|

#### Manual Calculations

![WhatsApp Image 2025-09-06 at 13 05 24_91f0a35b](https://github.com/user-attachments/assets/623839d5-d8b0-4893-b1e6-ef729ee441d3)


---

## OUTPUT SCREEN FROM MASM SOFTWARE
<img width="637" height="371" alt="Screenshot 2025-08-20 161433" src="https://github.com/user-attachments/assets/ff240b3b-3674-4611-b1e8-7be7313502c2" />

## 4. DIVISION

#### Algorithm

1. Load memory location of operands.
2. Perform division.
3. Store result.

   ## FLOWCHART
<img width="1065" height="802" alt="image" src="https://github.com/user-attachments/assets/25b4a483-0d42-494b-8639-1af3ea17191b" />


#### Program

```asm
CODE SEGMENT
ASSUME CS: CODE, DS: CODE
ORG 1000H
MOV SI,2000H
MOV DX,0000H
MOV AX,[SI]
MOV BX,[SI+02H]
DIV BX
MOV [SI+04H],AX
MOV [SI+06H],DX
MOV AH,4CH
INT 21H
CODE ENDS
END
```

#### Output Table

| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| ----------------------- | ------------------------ |
 1200=12                 |        1204=01              |
|1201=34|1205=00|
|1202=12|1206=00|
|1203=34|1207+00|

#### Manual Calculations

![WhatsApp Image 2025-09-06 at 13 14 43_dd500c62](https://github.com/user-attachments/assets/46896b75-8adb-4f1b-8eb9-539ac7ba055a)

---
## OUTPUT FROM MASM SOFTWARE
<img width="633" height="279" alt="Screenshot 2025-09-06 114957" src="https://github.com/user-attachments/assets/68da89bb-ea6d-4572-a9fa-d6a72bf9b4de" />



## RESULT

Thus, the Assembly Language Programs for 8086 to perform arithmetic operations (Addition, Subtraction, Multiplication, and Division) using both direct and indirect methods were successfully written and executed using MASM.
