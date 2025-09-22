Arithmetic-operation-using-8086
8086 Assembly Language Programs for Arithmetic Operations
AIM
To write and execute Assembly Language Programs to perform arithmetic operations for the 8086 microprocessor.

APPARATUS REQUIRED
Personal Computer with MASM Software
1. ADDITION
Algorithm
Initialize memory location in HL register.
Store 1st data.
Increment HL to enter 2nd data.
Move 2nd number to accumulator.
Decrement HL.
Add value in memory with accumulator.
Store result.
Stop.
FLOW CHART
image
Program
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
Output Table
MEMORY LOCATION (INPUT)	MEMORY LOCATION (OUTPUT)
2000	79
2001	88
2002	23
2003	02
MEMORY LOCATION (INPUT)	MEMORY LOCATION (OUTPUT)
2004	9C
2005	8A
2006	00
Manual Calculations
Manual Calculation Direct Addition

OUTPUT IMAGE FROM MASM SOFTWARE
Indirect Addition
2. SUBTRACTION
Algorithm
Initialize memory and store 1st data.
Increment to get 2nd data.
Move 2nd data to accumulator.
Subtract memory content.
Store result.
FLOWCHART
image
Program
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
Output Table
MEMORY LOCATION (INPUT)	MEMORY LOCATION (OUTPUT)
2000	79
2001	88
2002	23
2003	02
MEMORY LOCATION (INPUT)	MEMORY LOCATION (OUTPUT)
2004	56
2005	86
2006	00
Manual Calculations
Indirect Substraction

OUTPUT SCREEN FROM MASM SOFTWARE
Indirect substraction
3. MULTIPLICATION
Algorithm
Initialize memory and store operands.
Move operands to registers.
Multiply.
Store result.
##FLOWCHART

image
Program
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
Output Table
MEMORY LOCATION (INPUT)	MEMORY LOCATION (OUTPUT)
2000	02
2001	00
2002	03
2003	00
MEMORY LOCATION (INPUT)	MEMORY LOCATION (OUTPUT)
2004	06
2005	00
2006	00
Manual Calculations
Manual Calculation Indirect Multiplication

OUTPUT SCREEN FROM MASM SOFTWARE
Indirect Multiplication
4. DIVISION
Algorithm
Load memory location of operands.

Perform division.

Store result.

FLOWCHART
image
Program
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
Output Table
MEMORY LOCATION (INPUT)	MEMORY LOCATION (OUTPUT)
2000	69
2001	24
2002	34
2003	12
MEMORY LOCATION (INPUT)	MEMORY LOCATION (OUTPUT)
2004	02
2005	00
2006	01
Manual Calculations
Manual Calculation Indirect Division

OUTPUT FROM MASM SOFTWARE
Indirect division
RESULT
Thus, the Assembly Language Programs for 8086 to perform arithmetic operations (Addition, Subtraction, Multiplication, and Division) using both direct and indirect methods were successfully written and executed using MASM.
