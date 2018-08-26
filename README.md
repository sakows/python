#  Python Notes
Ch:1,2
Variables only can contain:
lowercase,uppercase,digits, underscore(_)
Check python variable type: type()
Names cannot start with digits.
7 // 2 =3 Integer division
7 / 2 =3.12321 Floating-point division
7 % 3 =1 Modulus(remainder)
To get quotient and remainder at once:
divmod(9,5)=(1,4)
0b or 0B binary(base 2)
0o or 0O octal(base 8)
0x or 0X for hex(base 16)

## Type conversions
int(),float(),str(),list()
True treated as 1, False as 0.
Googol = 10*'*'100
Strings are immutable
stat='na'*4
stat.replace('n','l')
Slicing:
[:] entire string
[start:]
[:end]
[start:end]
[start:end:step]
3 last characters: letters[-3:]
From start to end in in steps 7 chars: letters[::7]
To reverse string: letters[-1::-1] or letters[::-1]
String to list convert: split() If separator not defined used:newline,space,tab
Join() is opposite to Split: ','.join(list)

==
Questionary:
1. Get 1st 13 chars:
poem[::13]
2. How many chars?
len(poem)
3. Does it start with letters All?
poem.startwith('All')
4. Does it end with folks?
poem.endwith('folks')
5. Find offset of 1st occurrence in word:
poem.find('thes')
6. Find offset of last occurrence in word:
poem.rfind('thes')
7. How many times repeated word?
poem.count('thes')
8. Are all chars are letter and number?
poem.isalnum()
9. Remove '.' from both ends:
setup.strip('.')
10. Capitalize 1st word:
setup.capitalize()
11. Capitalize all words:
setup.title()
12. Convert all chars to uppercase:
setup.upper()
13. Convert all chars to lowercase:
setup.lower()
14. Swap upper and lower case:
setup.swapcase()
15. center string within 30 spaces:
setup.center(30)
16. Left justify:
setup.ljust(30)
17. Right justify:
setup.rjust(30)
18. Replace word with another up to 100 of them:
setup.replace('sako','maka',100)


Ch3:
Tuples are immutable. List are mutable.
If you have more than 1 separator string in row, will get an empty string as list item.
Can extract single value from list as string using offset: my_list[2], my_list[-1]
Can extract subsequence of list by using slice:
listo[0:2]=[1,2]
1. Slice of list is also list
2. a=[G,C,H] a[::-2]=[H,G] a[::2]=[G,H] 
3. Reverse list: a[::-1]
4. Add item to the end of list: a.append('sako')
5.Merge 2 lists: l3=l1.extend(l2) OR l1+=l2








