*  Name      : Odyssey Villagomez & Megha Sapra
*  Class     :  CSCI 5743
*  Date  :  13th Oct 2022
*  Assignment 2 : Hash Function

*******************************************************
Assignment: 

Part 1 - Using any programming language (Preferably Java or Python), develop your own hash function. Given an input string x of any length, your hash function must generate a random output bit vector y of length 32 bits. You should only use logical operators (&, |, >>, <<) and also (Rotate right/left) to generate the output (digest). You can take ideas from how existing Hash functions like SHA-2 are designed.

Description of the program

Part 1 includes the hash function. The hash function 
takes in a string x. X is encoded into bytes and 
those bytes are divided into blocks, which are further
divided into sublocks. Logical operations are performed
on the sublocks and then concatenated. The resulting
32 bit hash value is returned. 

Part 2 includes a brute force attack function that 
generates two random strings, of any specified k, length. 
The two random strings are hashed using the previous 
mentioned hash function and checked for equality. 
A counter keeps track of how many attempts have been made. 
The counter stops at collision or if birthday bound of 
(2^16) attempts is reached. Function outputs the counter.

The brute force function is then ran 5 times and the 
resultant attempts are averaged. 

Part 3 includes the analysis of the brute force 
attack on the hash function. 
*******************************************************

!******************************************************
Collaboration Disclosures
!******************************************************

The left rotate functions used in the hash function are from  
https://www.geeksforgeeks.org/python-logical-operators-with-examples-improvement-needed/

*******************************************************
Source files
- Secure Hash Function.ipynb
  - Jupyter notebook file with the hash function code
  and analysis 
*******************************************************

Status of program
- The program is complete. 

- Known bugs or omissions: 
- Bugs: None
*******************************************************
 

	
