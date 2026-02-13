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
LDA 4200H 
MOV C, A  
LXI H, 4201H  
MOV A, M 
INX H  
DCR C  
LOOP: CMP M  
JNC NEXT 
MOV A,M  
NEXT: INX H  
DCR C 
JNZ LOOP  
STA 4300H 
HLT




## Output:
<img width="1871" height="1024" alt="Screenshot 2026-02-13 160946" src="https://github.com/user-attachments/assets/fffb401e-c907-4456-bdb4-11092a49f715" />
<img width="1878" height="1018" alt="Screenshot 2026-02-13 161010" src="https://github.com/user-attachments/assets/fcfedfce-5582-4774-acef-d0ff656cc4dc" />


## Finding the Smallest Number

## Algorithm:

1.	Load the count of numbers from memory location 4200H into register C.
2.	Load the first number from 4201H into register A (Assume it as the smallest).
3.	Load the next number and compare it with A.
4.	If the new number is smaller, update A.
5.	Repeat the process for all numbers.
6.	Store the smallest number in 4301H.

## Program:

LDA 4200H 
MOV C, A 
LXI H, 4201H 
MOV A, M 
INX H 
DCR C  
LOOP: CMP M 
JC NEXT 
MOV A,M 
NEXT: INX H 
DCR C 
JNZ LOOP 
STA 4300H 
HLT

## Output:
<img width="1882" height="1023" alt="Screenshot 2026-02-13 161058" src="https://github.com/user-attachments/assets/79d5c673-a6ca-4f0b-bc8d-01a94d538f7b" />
<img width="1873" height="1013" alt="Screenshot 2026-02-13 161211" src="https://github.com/user-attachments/assets/3225c293-0168-4cbd-b707-97dc7907f7d7" />



## Result:

The 8085 microprocessor successfully finds the greatest and smallest numbers from multiple inputs and stores them in memory.
