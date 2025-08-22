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
| 1200:12                 |               1204:24
  1201:34                 |              1205:68
| 1202:12                 |
| 1203:34                 |

#### Manual Calculations


![WhatsApp Image 2025-08-22 at 11 09 00_859a1b72](https://github.com/user-attachments/assets/35e2ef35-2bb4-4713-b749-a9a75b5726a3)


## OUTPUT IMAGE FROM MASM SOFTWARE
<img width="640" height="480" alt="Screenshot (8)" src="https://github.com/user-attachments/assets/870d58de-df3e-4149-b615-f907e561b9b4" />
<img width="640" height="480" alt="Screenshot (12)" src="https://github.com/user-attachments/assets/4ee570b4-7fa7-4e48-a792-70681c15d936" />


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

```
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
| 1200:12                 |      1204:00
  1201:34                  |     1205:00
| 1202:12
| 1203:34              |                          |

#### Manual Calculations

![WhatsApp Image 2025-08-22 at 11 12 59_e3662d35](https://github.com/user-attachments/assets/0c30694b-765e-4c90-84a5-d22452e566d6)

## OUTPUT SCREEN FROM MASM SOFTWARE
<img width="640" height="480" alt="Screenshot (15)" src="https://github.com/user-attachments/assets/3396b2e1-db3a-444c-a64d-13eae2619795" />

<img width="640" height="480" alt="Screenshot (13)" src="https://github.com/user-attachments/assets/da81f21e-4259-46f4-a6c8-d7da2fadeaf1" />

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
| 1200:12                  |     1204:44
  1201:34                 |      1205:51
| 1202:12                |       1206:97
| 1203:34              |        1207:0A              |

#### Manual Calculations

![WhatsApp Image 2025-08-22 at 11 27 59_e72d4686](https://github.com/user-attachments/assets/92a291b1-ac9c-4135-9a1b-9dec0edc2499)



## OUTPUT SCREEN FROM MASM SOFTWARE
<img width="640" height="480" alt="Screenshot (19)" src="https://github.com/user-attachments/assets/a7796991-c745-415e-b67a-00a80acf2b51" />
<img width="640" height="480" alt="Screenshot (17)" src="https://github.com/user-attachments/assets/ab664247-a39e-44f7-846c-1504a88d0f37" />


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
| 1200:12                       
  1201:34                   |   1204:01
| 1202:12                  |    1205:00
| 1203:34                  |   1206:00                   |

#### Manual Calculations

![WhatsApp Image 2025-08-22 at 11 33 31_973a8001](https://github.com/user-attachments/assets/75aa6e55-46e0-4562-8042-66aae30a8664)

## OUTPUT FROM MASM SOFTWARE
<img width="640" height="480" alt="Screenshot (23)" src="https://github.com/user-attachments/assets/181025e8-0da2-443a-80c3-f3cc1f619dbd" />

<img width="640" height="480" alt="Screenshot (22)" src="https://github.com/user-attachments/assets/29be2be7-0f67-457c-8062-0892fbdaf1ce" />


## RESULT

Thus, the Assembly Language Programs for 8086 to perform arithmetic operations (Addition, Subtraction, Multiplication, and Division) using both direct and indirect methods were successfully written and executed using MASM.
