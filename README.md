# Project-Euler-59---Python
Solution for Project Euler problem 59 in Python 
___  
## Description  
Each character on a computer is assigned a unique code and the preferred standard is ASCII (American Standard Code for Information Interchange). For example, uppercase A = 65, asterisk (*) = 42, and lowercase k = 107.  

A modern encryption method is to take a text file, convert the bytes to ASCII, then XOR each byte with a given value, taken from a secret key. The advantage with the XOR function is that using the same encryption key on the cipher text, restores the plain text; for example, 65 XOR 42 = 107, then 107 XOR 42 = 65.  

For unbreakable encryption, the key is the same length as the plain text message, and the key is made up of random bytes. The user would keep the encrypted message and the encryption key in different locations, and without both "halves", it is impossible to decrypt the message.  

Unfortunately, this method is impractical for most users, so the modified method is to use a password as a key. If the password is shorter than the message, which is likely, the key is repeated cyclically throughout the message. The balance for this method is using a sufficiently long password key for security, but short enough to be memorable.  

Your task has been made easy, as the encryption key consists of three lower case characters. Using 0059_cipher.txt, a file containing the encrypted ASCII codes, and the knowledge that the plain text must contain common English words, decrypt the message and find the sum of the ASCII values in the original text.  
___
## Solution
As every original word must contains A-Z or a-z characters, our original code must contains ascii codes between 65-90 or between 97-122.
Our password must contains ascii codes between 97-122.
Starting with key aaa (97, 97, 97), then aab (97, 97, 98)..., and finishing with zzz (122, 122, 122), we must Xor every 3 encrypted codes with the key.
If the resulting Xor code is not allowed, we try the next key.  
We print the words and sum of codes of every allowed result, and if we have more than one,  
the solution will be the result in which every word is an english word
I asume at the beginning that there will be a few solutions or only one solution.
