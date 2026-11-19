# Sorting-of-numbers-
sorting-of-numbers
## Aim
To write and execute an Assembly Language Program for sorting data in Ascending and descending order using 8051 microcontroller on Keil software.
## Apparatus Required
Personal Computer
Keil µVision software
## Algorithm(ASCENDING ORDER)
Initialize the register R7 with count (number of elements).
Get the first two elements into two registers.
Compare the two elements:
If the value in register R0 is lower, exchange A and R0 data.
Otherwise, increment pointer and decrement register R7.
Check if R7 = 0 → if yes, move the register R0 & A.
Increment pointer and decrement R7.
If R7 ≠ 0, repeat from Step 2.
Otherwise, stop the program.  
## Program (Ascending order)
ORG 0000H

MOV R0,#40H
MOV R2,#05H

LOOP1:
    MOV R1,#04H
    MOV R0,#40H

LOOP2:
    MOV A,@R0
    INC R0
    MOV B,@R0
    CJNE A,B,CHECK
    SJMP NEXT

CHECK:
    JC NEXT
    MOV @R0,A
    DEC R0
    MOV @R0,B
    INC R0

NEXT:
    DJNZ R1,LOOP2
    DJNZ R2,LOOP1

HERE: SJMP HERE

END
## OUTPUT(Ascending order)
<img width="1919" height="1199" alt="image" src="https://github.com/user-attachments/assets/8fb6a67d-a02b-428e-a6dd-7079a36b454b" />

## Algorithm(Descending order)
Initialize the register R7 with count.
Get first two elements in two registers.
Compare the two elements of data:
If the value of R0 register is high, then exchange A and R0 data.
Else, increment pointer and decrement register R7.
Check if R7 = 0, then move the contents of R0 and A.
Again increment pointer and decrement R7.
Check if R7 = 0:
If No, repeat the process from Step 2.
If Yes, stop the program.

## Program (Descending order)
ORG 0000H

MOV R0,#40H
MOV R2,#05H

LOOP1:
    MOV R1,#04H
    MOV R0,#40H

LOOP2:
    MOV A,@R0
    INC R0
    MOV B,@R0
    CJNE A,B,CHECK
    SJMP NEXT

CHECK:
    JNC NEXT
    MOV @R0,A
    DEC R0
    MOV @R0,B

NEXT:
    DJNZ R1,LOOP2
    DJNZ R2,LOOP1

HERE: SJMP HERE

END
## OUTPUT (DESCENDING ORDER)
<img width="1919" height="1199" alt="image" src="https://github.com/user-attachments/assets/4ff65037-0ad6-4d76-ba80-256bb89f7b00" />




## RESULT:
Thus the sorting of given data was done using 8051 keil software.
