# FIBONACCI SERIES USING 8086 MICROPROCESSOR

## AIM
To write an assembly language program in 8086 to generate the Fibonacci Series up to N terms and store the sequence in memory.

## APPARATUS REQUIRED
Personal Computer with MASM Software

## ALGORITHM
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


## PROGRAM
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

## Output Table
| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| ----------------------- | ------------------------ |
| 1200:12                 | 1204:24                  |
| 1201:34                 | 1205:68                  |
| 1202:12                 | 1206:00                  |
| 1203:34                 | 1207:C4                  |


## Manual Calculations
<img width="1600" height="824" alt="image" src="https://github.com/user-attachments/assets/8414af0c-263e-4407-b710-e2ec6d97b9f1" />

## OUTPUT IMAGE FROM MASM SOFTWARE

<img width="637" height="395" alt="mpmc_add" src="https://github.com/user-attachments/assets/4504a489-38d3-4316-924e-b61b7ef55b9c" />

<img width="637" height="402" alt="mpmc_addout" src="https://github.com/user-attachments/assets/707a6219-1aac-436a-92ea-e7067f7421ba" />

## RESULT
Thus, the Assembly Language Programs for 8086 to perform arithmetic operations (Addition, Subtraction, Multiplication, and Division) using both direct and indirect methods were successfully written and executed using MASM.
