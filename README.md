# Greatest-and-Smallest-of-the-given-numbers-Using-8085

## Aim:

To write 8085 microprocessor programs to find the greatest and smallest number from the given 8-bit numbers.

## Apparatus Required:

•	Laptop with an internet connection

## Finding the Greatest Number

## Algorithm:

1.	Load the count of numbers from memory location 4200H into register C.
2.	Load the first number from 4201H into register A (Assume it as the greatest).
3.	Load the next number and compare it with A.
4.	If the new number is greater, update A.
5.	Repeat the process for all numbers.
6.	Store the greatest number in 4300H.

## Program:
LDA 4200H ;<BR>
MOV C,A ;<BR>
LXI H,4201H ;<BR>
MOV A,M ;<BR>
INX H ;<BR>
DCR C ;<BR>
LOOP:CMP M ;<BR>
JNC NEXT ;<BR>
MOV A,M ;<BR>
NEXT:INX H ;<BR>
DCR C ;<BR>
JNZ LOOP ;<BR>
STA 4300H ;<BR>
HLT ;<BR>


## Output:
<img width="1829" height="899" alt="Screenshot 2025-09-12 152241" src="https://github.com/user-attachments/assets/9fc70f3c-996b-4571-adc0-48e483718da6" />
<img width="301" height="523" alt="Screenshot 2025-09-12 152259" src="https://github.com/user-attachments/assets/2fd25863-f18d-481f-81b4-9c0f18b318cc" />




## Finding the Smallest Number

## Algorithm:

1.	Load the count of numbers from memory location 4200H into register C.
2.	Load the first number from 4201H into register A (Assume it as the smallest).
3.	Load the next number and compare it with A.
4.	If the new number is smaller, update A.
5.	Repeat the process for all numbers.
6.	Store the smallest number in 4301H.

## Program:
LDA 4200H ;<BR>
MOV C,A ;<BR>
LXI H,4201H ;<BR>
MOV A,M ;<BR>
INX H ;<BR>
DCR C ;<BR>
LOOP:CMP M ;<BR>
JC NEXT ;<BR>
MOV A,M ;<BR>
NEXT:INX H ;<BR>
DCR C ;<BR>
JNZ LOOP ;<BR>
STA 4301H ;<BR>
HLT ;<BR>

## Output:

<img width="1827" height="904" alt="image" src="https://github.com/user-attachments/assets/6bbfa8ec-b8bf-4b93-bd00-0407e786ff11" />

<img width="300" height="536" alt="image" src="https://github.com/user-attachments/assets/cafb174e-8c6b-4971-ae49-1caff7f96893" />



## Result:

The 8085 microprocessor successfully finds the greatest and smallest numbers from multiple inputs and stores them in memory.
