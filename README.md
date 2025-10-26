# Arithmetic-operation-using-8086
# 8086 Assembly Language Programs for Arithmetic Operations

## AIM
To write and execute Assembly Language Programs to perform arithmetic operations for the 8086 microprocessor.

## APPARATUS REQUIRED
Personal Computer with MASM Software

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
| 1200:12                 | 1204:24                  |
| 1201:34                 | 1205:68                  |
| 1202:12                 | 1206:00                  |
| 1203:34                 | 1207:C4                  |


#### Manual Calculations
<img width="1600" height="824" alt="image" src="https://github.com/user-attachments/assets/8414af0c-263e-4407-b710-e2ec6d97b9f1" />

## OUTPUT IMAGE FROM MASM SOFTWARE

<img width="637" height="395" alt="mpmc_add" src="https://github.com/user-attachments/assets/4504a489-38d3-4316-924e-b61b7ef55b9c" />

<img width="637" height="402" alt="mpmc_addout" src="https://github.com/user-attachments/assets/707a6219-1aac-436a-92ea-e7067f7421ba" />

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
| 1200:12                 | 1204:00                  |
| 1201:34                 | 1205:00                  |
| 1202:12                 | 1206:00                  |
| 1203:34                 | 1207:C4                  |

#### Manual Calculations

<img width="1600" height="706" alt="image" src="https://github.com/user-attachments/assets/14cd765f-4c6a-4480-9405-851ef951cb7c" />

## OUTPUT SCREEN FROM MASM SOFTWARE

<img width="638" height="397" alt="mpmc_sub" src="https://github.com/user-attachments/assets/804300e2-8727-4d70-b5ce-54480fbbc7b9" />

<img width="627" height="398" alt="mpmc_subout" src="https://github.com/user-attachments/assets/d9d0755b-1164-4e29-8870-537e2934bde3" />

## 3. MULTIPLICATION

#### Algorithm
1. Initialize memory and store operands.
2. Move operands to registers.
3. Multiply.
4. Store result.

#### FLOWCHART
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
| 1200:12                 | 1204:44                  |
| 1201:34                 | 1205:51                  |
| 1202:12                 | 1206:97                  |
| 1203:34                 | 1207:0A                  |

#### Manual Calculations

<img width="1600" height="1238" alt="image" src="https://github.com/user-attachments/assets/9e867f2c-0f9e-42e3-8f5a-cefec3fbf839" />

## OUTPUT SCREEN FROM MASM SOFTWARE

<img width="640" height="398" alt="mpmc_mul" src="https://github.com/user-attachments/assets/4fe62bed-81f2-4a2b-b207-d28a9058af1e" />

<img width="632" height="397" alt="mpmc_mulout" src="https://github.com/user-attachments/assets/4c533a4c-9393-4608-be45-6ad5273fae64" />

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
| 1200:12                 | 1204:01                  |
| 1201:34                 | 1205:00                  |
| 1202:12                 | 1206:00                  |
| 1203:34                 | 1207:00                  |

#### Manual Calculations

<img width="1600" height="755" alt="image" src="https://github.com/user-attachments/assets/fb6497a0-e6dd-4d6b-a147-f8e23b9b33db" />

## OUTPUT FROM MASM SOFTWARE
<img width="637" height="402" alt="mpmc_div" src="https://github.com/user-attachments/assets/471d3213-c320-4f9b-9c4a-c9cd9cf76230" />

<img width="637" height="401" alt="mpmc_divout" src="https://github.com/user-attachments/assets/83c273bb-91d0-47a8-8b7f-d1655428e32d" />

## RESULT
Thus, the Assembly Language Programs for 8086 to perform arithmetic operations (Addition, Subtraction, Multiplication, and Division) using both direct and indirect methods were successfully written and executed using MASM.
