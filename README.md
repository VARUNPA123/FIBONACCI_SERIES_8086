# FIBONACCI SERIES USING 8086 MICROPROCESSOR

## AIM
To write an assembly language program in 8086 to generate the Fibonacci Series up to N terms and store the sequence in memory.

## APPARATUS REQUIRED
Personal Computer with MASM Software

## PROBLEM ANALYSIS
The first and second term of the Fibonacci series are 00 and 01. The third element is given by the sum of the first and second element. The fourth element is given by sum of second and third element, and so on. In general, an element of fibonacci series is given by sum of immediate two previous element.

## ALGORITHM
1. Set SI-register as pointer for Fibonacci series.
2. Set CL-register as count for number of elements to be generated.
3. Increment the pointer (SI).
4. Initialize the first element of Fibonacci series as 00H in AL-register.
5. Store first element in memory.
6. Increment the pointer (SI).
7. Increment AL to get second element (01H) of Fibonacci series in AL-register.
8. Store the second element in memory.
9. Decrement the count (CL-register) by 02.
10. Decrement the pointer (SI).
11. Get the element prior to last generated element in AL.
12. Get the last generated element in BL.
13. Add the previous two elements (AL and BL) to get the next element in AL.
14. Increment the pointer.
15. Store the next element (AL) of the Fibonacci series in memory.
16. Decrement the count (CL).
17. If the content of CL is not zero then go to step 10, otherwise stop.

## FLOW CHART
<img width="967" height="585" alt="image" src="https://github.com/user-attachments/assets/7dd62d35-fc40-403a-894f-cf84e620a8ac" />

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


## OUTPUT IMAGE FROM MASM SOFTWARE

<img width="643" height="397" alt="image" src="https://github.com/user-attachments/assets/b4be7f7f-8784-4375-8d5e-c9ccfa68968f" />
<img width="643" height="222" alt="image" src="https://github.com/user-attachments/assets/a2186cb3-f924-41f5-8dc0-a3d04ded28ad" />


## RESULT
Thus, the Assembly Language Programs for 8086 to perform arithmetic operations (Addition, Subtraction, Multiplication, and Division) using both direct and indirect methods were successfully written and executed using MASM.
