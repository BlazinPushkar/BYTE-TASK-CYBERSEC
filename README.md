TASK-1
I tried base64 decoding first cause it had upper,lower case characters with numbers
then i got something NYBX{ and it looked similar to BYTE{ so i tried ROT13 , but that didn't give any thing useful
so i tried caeser shift on that, still got nothing
then i had to try XOR or vigenere shift but i didn't know how keys are calculated for them , i used chatgpt for that
i did vigenere shift and got the CTF 
TASK -2 
This one was really difficult, i did pngcheck and got crc error
i found 2 IEND , i extracted everything from that
I got 5 PKs and tried to unzip them all but didn't find anything
I did binwalk then , got a zlib , default compressed file
tried to decompress it with zlib-deflate, but it gave error
tried xor decoding then , didn't get anything useful
then tried fixing the png image , i replaced crc with expected crc i got from pngcheck and then binwalk / zlib after that didn't get anything useful
