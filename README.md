a# Arithmetic-operation-using-8086
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
| 1200:12 24:1204 |                          |


      1201:34               68:1205
      1202:12               00:1206
      1203:34               c4:1207                                

#### Manual Calculations





![WhatsApp Image 2025-09-14 at 18 34 02_f186cfe6](https://github.com/user-attachments/assets/553e6044-8ea9-4f21-970c-60079bc75383)





## OUTPUT IMAGE FROM MASM SOFTWARE

<img width="310" height="350" alt="image" src="https://github.com/user-attachments/assets/c6a9df00-b986-4312-9ac2-6817c431efba" />

<img width="794" height="470" alt="Screenshot 2025-09-14 173740" src="https://github.com/user-attachments/assets/c2fd3fe0-e55b-4f7b-a1b2-782f12f7cd34" />



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
|1200:12 24:1204                         |                          |



      1201:34               68:1205
      1202:12               00:1206
      1203:34               c4:1207                              

#### Manual Calculations

![WhatsApp Image 2025-09-14 at 18 17 53_065773eb](https://github.com/user-attachments/assets/fdbb6e44-4cd5-4209-a4d5-4186a1333283)







## OUTPUT SCREEN FROM MASM SOFTWARE

<img width="330" height="375" alt="image" src="https://github.com/user-attachments/assets/5a1887d7-20c4-480c-b4c6-fdae6f15743d" />


<img width="788" height="485" alt="Screenshot 2025-09-14 174417" src="https://github.com/user-attachments/assets/afe83421-2f2b-4600-a7fc-13fb95b06514" />



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
|  1200:12 24:1204                       |                          |

      1201:34               68:1205
      1202:12               00:1206
      1203:34               c4:1207                               

#### Manual Calculations


![WhatsApp Image 2025-09-14 at 18 17 56_75c7d1cf](https://github.com/user-attachments/assets/598d8dbe-974a-45ec-8aaf-5f2a1501ef1d)



## OUTPUT SCREEN FROM MASM SOFTWARE

<img width="292" height="299" alt="Screenshot 2025-09-14 174853" src="https://github.com/user-attachments/assets/ee20cc79-bbf7-4136-8935-4742dbc394ee" />




<img width="781" height="485" alt="Screenshot 2025-09-14 175008" src="https://github.com/user-attachments/assets/181da87e-693f-4662-9af4-c4e9f997f2c8" />



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
|  1200:12 24:1204                       |                          |


      1201:34               68:1205
      1202:12               00:1206
      1203:34               c4:1207                                

#### Manual Calculations

![WhatsApp Image 2025-09-14 at 18 18 00_d7a9d8e0](https://github.com/user-attachments/assets/471dfa27-0b4a-44a1-9960-d9affb00ab44)




## OUTPUT FROM MASM SOFTWARE

<img width="284" height="300" alt="Screenshot 2025-09-14 175205" src="https://github.com/user-attachments/assets/1b289f62-8169-4743-b3f1-e7ce87de1a74" />


<img width="790" height="479" alt="Screenshot 2025-09-14 175257" src="https://github.com/user-attachments/assets/090f5bf7-c25a-4512-a7a7-f9bbf88a4b95" />





## RESULT

Thus, the Assembly Language Programs for 8086 to perform arithmetic operations (Addition, Subtraction, Multiplication, and Division) using both direct and indirect methods were successfully written and executed using MASM.

