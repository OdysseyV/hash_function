*  Name      : Odyssey Villagomez & Megha Sapra
*  Class     :  CSCI 5743
*  Date  :  13th Oct 2022
*  Assignment 2 : Hash Function

*******************************************************
Assignment: 

Part 1 - Using any programming language (Preferably Java or Python), develop your own hash function. Given an input string x of any length, your hash function must generate a random output bit vector y of length 32 bits. You should only use logical operators (&, |, >>, <<) and also (Rotate right/left) to generate the output (digest). You can take ideas from how existing Hash functions like SHA-2 are designed.

Part 2 - Then, write a method that finds collisions in your hash function using brute-force attack. This method will generate many random input strings and stops when two strings have the same hash. Analyze your hash function in terms of robustness using the concept of birthday attack.

*******************************************************
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

The brute force function is then executed 5 times and the 
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

Analysis

The hash function is modeled after SHA-256 where the input string s is divided into blocks (size 8 bits) and then those blocks are further divided into sub blocks (size 2 bits). The sub block performs binary operations on the word, combining it with initialization values. The result of the sub blocks are concatenated and only the first 32 bits of the value are kept, to output a digest of size 32 bits.

For the hash function to be secure it needs to be resistant to (2^16) brute force attacks, defined by the birthday bound of 2^(n/32) where n is the size of the hash, 32.

The hash funciton was evaluated by attempting a brute force attack 5 times. The amount of steps to break the attack are averaged and result in average steps of ~15,000, ~7000, and 22000. This hash function is not secure, based on the birthday attack because it takes less than 2^16 steps to find a collision

*******************************************************
Status of program
- The program is complete. 

- Known bugs or omissions: 
- Bugs: None
*******************************************************
 

	
