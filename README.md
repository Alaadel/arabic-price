# NumberToArabic
The function converts a floating point number (with 2 decimal digits) to a price desctiption in Arabic. I made it for a billing system I worked on. Currently it works only on the format "X.Y", where X is 6 digits at maximum and Y is 2 digits maximum.

Examples:
5069.46
is converted to:
"فقط خمسة آلاف و تسعة و ستون جنيه و ستة و أربعون قرش لا غير"

2539034.50
is converted to:
"فقط مليونان و خمسمائة و تسعة و ثلاثون ألفاً و أربعة و ثلاثون جنيه و خمسة قرش لا غير"

Due to Arabic grammer and the fact that Arabic numbers are read in a different order than how they are written, I could not find a systematic approach to solve this problem (during the limited time of the project). The function may seem complex, but it basically replace each digit with the appropriate word and suffix. Here is what it does:

1- Define constant words, units and suffixes.

2- Define the words that represnet numbers in Arabic.

3- Loop over the given number from left to right.

4- Analyze the relation of the current digit with its surroundings. Arabic represnetation of a digit is affected by what is before and after it.

5- Represent the digit using a constant word + the right suffix, according to Arabic grammers and data from previous steps.

6- Set the units (Millions, Thousands ..).

7- Calculate the positions of the "و" (means "and"). This also differes based on the number structure.

8- Concatenate the words in one string.

9- Remove extra spaces. (removing them at the end is a way easier than trying to predict the right positions from the start, trust me!)

I have tested it on tens of cases, but if you found any bugs please drop me a comment. 
Thanks.
