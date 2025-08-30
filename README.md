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
<img width="221" height="464" alt="image" src="https://github.com/user-attachments/assets/05d45fc9-7cf2-4ee3-a258-08d524b34975" />



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
<img width="422" height="296" alt="image" src="https://github.com/user-attachments/assets/0600c520-79f4-44b1-9696-3044e4dfb1fc" />


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

<img width="272" height="553" alt="image" src="https://github.com/user-attachments/assets/945df404-62b2-49c5-9d60-f6a43ecb4cd3" />



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

<img width="301" height="256" alt="image" src="https://github.com/user-attachments/assets/fdbddb3f-7356-419f-a951-b03a46038699" />


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
<img width="372" height="520" alt="image" src="https://github.com/user-attachments/assets/61369b31-fd91-43db-9f2e-46b283405b3f" />



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
<img width="332" height="222" alt="image" src="https://github.com/user-attachments/assets/7e5495da-d7d9-4a0f-b296-a4de4fe3adf2" />


## OUTPUT SCREEN FROM MASM SOFTWARE
<img width="640" height="480" alt="Screenshot (19)" src="https://github.com/user-attachments/assets/a7796991-c745-415e-b67a-00a80acf2b51" />
<img width="640" height="480" alt="Screenshot (17)" src="https://github.com/user-attachments/assets/ab664247-a39e-44f7-846c-1504a88d0f37" />


## 4. DIVISION

#### Algorithm

1. Load memory location of operands.
2. Perform division.
3. Store result.

   ## FLOWCHART

<img width="254" height="402" alt="image" src="https://github.com/user-attachments/assets/f03b293a-f898-4539-aa96-96a33cf4d84b" />


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
<img width="221" height="105" alt="image" src="https://github.com/user-attachments/assets/a5eba1e3-aa85-4e8b-aaeb-2dd93be8555a" />


## OUTPUT FROM MASM SOFTWARE
<img width="640" height="480" alt="Screenshot (23)" src="https://github.com/user-attachments/assets/181025e8-0da2-443a-80c3-f3cc1f619dbd" />

<img width="640" height="480" alt="Screenshot (22)" src="https://github.com/user-attachments/assets/29be2be7-0f67-457c-8062-0892fbdaf1ce" />


## RESULT

Thus, the Assembly Language Programs for 8086 to perform arithmetic operations (Addition, Subtraction, Multiplication, and Division) using both direct and indirect methods were successfully written and executed using MASM.
