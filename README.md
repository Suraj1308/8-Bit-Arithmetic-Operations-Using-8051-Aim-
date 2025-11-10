# 8-Bit-Arithmetic-Operations-Using-8051

## Aim:
To perform 8-bit arithmetic operations such as addition, subtraction, multiplication, and division using the 8051 microcontroller.

## Apparatus Required:

•	Laptop with Keil uVision software

## Algorithm:

## For Addition:
1.	Load the first number from memory location 30H into register A.
2.	Load the second number from memory location 31H into register B.
3.	Add the contents of registers A and B.
4.	Store the result in memory location 40H.
5.	Store the carry (if any) in 41H.

## Program:
      MOV A , 30H
      ADD A, 31H
      MOV 40H, A
      JNC NEXT
      MOV 41H, #01H
      SJMP END_PROGRAM
      NEXT: MOV 41H, #00H
      END_PROGRAM: NOP
      END


## Output:
<img width="1919" height="1138" alt="image" src="https://github.com/user-attachments/assets/537c53e5-4134-4c40-a6e0-a89fb6d90ff6" />

   
## For Subtraction:
1.	Load the first number from memory location 30H into register A.
2.	Load the second number from memory location 31H into register B.
3.	Subtract B from A.
4.	Store the result in memory location 40H.

## Program:
      MOV A, 30H
      SUBB A, 31H
      MOV 40H, A
      JNC NEXT
      MOV 41H, #01H
      SJMP END_PROGRAM
      NEXT: MOV 41H, #00H
      END_PROGRAM: NOP
      END


## Output:
<img width="1919" height="1138" alt="image" src="https://github.com/user-attachments/assets/5451cb19-85d7-4d53-8101-5cceb215de1b" />

## For Multiplication:
1.	Load the first number from memory location 30H into register A.
2.	Load the second number from memory location 31H into register B.
3.	Multiply A and B.
4.	Store the lower byte of the result in memory location 40H.
5.	Store the higher byte of the result in memory location 41H.

## Program:
      ORG 0000H
      MOV A, 30H
      MOV B, 31H
      MUL AB
      MOV 40H, A
      MOV 41H, B
      END


## Output:
<img width="1919" height="1140" alt="image" src="https://github.com/user-attachments/assets/a4c46725-a4b2-43ee-80f1-0497c9cbbed8" />


## For Division:
1.	Load the dividend from memory location 30H into register A.
2.	Load the divisor from memory location 31H into register B.
3.	Divide A by B.
4.	Store the quotient in memory location 40H.
5.	Store the remainder in memory location 41H.


## Program:
      ORG 0000H
      MOV A, 30H
      MOV B, 31H
      DIV AB
      MOV 40H, A
      MOV 41H, B
      END


## Output:
<img width="1919" height="1141" alt="image" src="https://github.com/user-attachments/assets/7debb895-dd61-4a13-96ca-82e6df9bd597" />



## Result:
The 8-bit arithmetic operations using the 8051 microcontroller have been successfully executed and verified using Keil software.
