
# SORTING---8051

**AIM:**

To write and execute Assembly language Program for sorting of data using 8051 keil.

**APPARATUS REQUIRED: Personal computer with Keil software**

**(i) Descending order ALGORITHM:**

1.	Initialize the register r7 with count.
2.	Get first two elements in two registers.
3.	Compare the two elements of data. If value of R0 register is low, then exchange A & R0 data else increment pointer and decrement register R7.
4.	Check R7 is zero, and then move the register R0 & A.
5.	Again increment pointer and decrement R7,
6.	Check R7 is zero. If no repeat the process from step 2.
7.	Otherwise stop the program.

**PROGRAM:**

ORG 0000H 

MOV R7,#4

LOOP1:MOV R0,#40H 

MOV R6,#04

LOOP: MOV A,@R0 

INC R0

MOV 50H,@R0 

CJNE A,50H,NEXT 

SJMP DOWN 

NEXT:JNC DOWN 

MOV @R0,A

DEC R0

MOV @R0,50H 

DOWN:DJNZ R6,LOOP 

DJNZ R7,LOOP1

END


**OUTPUT:**
![WhatsApp Image 2025-11-11 at 21 59 18_d8c884f5](https://github.com/user-attachments/assets/c039646f-d8b2-4d9c-9282-c70fe215b911)

**MEMORY WINDOW:**

Before execution: D:0x40H:
<BR>
<BR>
<BR>
![WhatsApp Image 2025-10-30 at 19 24 26_d64be2a0](https://github.com/user-attachments/assets/11477241-cb12-4560-b1f6-a7115297e55a)


After execution: D:0x40H:
<BR>
<BR>
<BR>
![WhatsApp Image 2025-10-30 at 19 23 21_4bcacf34](https://github.com/user-attachments/assets/8f56e509-1ce6-4a99-b7b7-7fa99f26e011)

**(ii)	Ascending order**
 
**ALGORITHM:**

1.	Initialize the register r7 with count.
2.	Get first two elements in two registers.
3.	Compare the two elements of data. If value of R0 register is high then exchange A & R0 data else increment pointer and decrement register R7.
4.	Check R7 is zero, and then move the register R0 & A.
5.	Again increment pointer and decrement R7,
6.	Check R7 is zero. If no repeat the process from step 2.
7.	Otherwise stop the program.

**PROGRAM:**

ORG 0000H 

MOV R7,#4

LOOP1:MOV R0,#40H

MOV R6,#04

LOOP: MOV A,@R0

INC R0

MOV 50H,@R0 

CJNE A,50H,NEXT

SJMP DOWN 

NEXT:JC DOWN

MOV @R0,A

DEC R0

MOV @R0,50H 

DOWN:DJNZ R6,LOOP 

DJNZ R7,LOOP1

END

**OUTPUT:**
![WhatsApp Image 2025-11-11 at 21 59 41_bf9af3da](https://github.com/user-attachments/assets/75360a60-a27e-4744-8bff-058df1bd1a14)

**MEMORY WINDOW:** 

**Before execution:**
D:0x40H:
<BR>
<BR>
<BR>
<BR>
![WhatsApp Image 2025-10-30 at 19 31 14_62f25439](https://github.com/user-attachments/assets/9fe7dfda-5e8c-4755-9243-23f49763a0f0)

After execution:
D:0x40H:
<BR>
<BR>
<BR>
![WhatsApp Image 2025-10-30 at 19 30 15_9d2e99fd](https://github.com/user-attachments/assets/8386b046-194c-43c9-8ec8-249d1256c3e7)

**Result:**

Thus the sorting of given data was done using 8051 keil and shown the output.

