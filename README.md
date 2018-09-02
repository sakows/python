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
6. If use append for merge: l3=l1.append(l2) = [l1,[l2]]
7. Add item before any offset in list, use insert(): l1.insert(3,'Gummo')
8. To delete item by index: del l1[-1], del l1[2]. In this case list length decrease by 1. Del is Python statement, not list method.
9. To delete item by value, use remove() method: l1.remove('Gummo')
10. Get item from list and delete same time use pop() or pop(-1) method. Pop(0) returns start of list.
11. To find index of value in list: l1.index('Sako')
12.Test for value with 'in': ~ 'Grucho' in list: True/False ~
13. Use 'set' if dont care about order of items
14. Count occurences of value by using count(): l1.count('Sako') -> 4
15. Convert to str with join(): l1=[e1,e2,e3] ', '.join(l1) -> 'e1, e2, e3'
PS: Join is a string method not a list!!! Join is opposite of split!!! join <> split
16. Sort() list item by value, sorted() method creates copy of list sorted. l1.sort(reverse=True): do it in reverse order.
17. Number of items in list: len(l1)
18. Copy values of list to independent, fresh list by using: copy(),list(),slice[:]
19. Tuples are immutable, constant list. Cant add, change,delete items after tuple defined. Empty tuple: tup=()
20. Tuple unpacking: tup=(a1,a2,a3) a,b,c=tup
21. To convert from others to tuple, use tuple() func: tuple(l1)
22. Tuples advantages over list: -less space -cant clobber by mistake -can use as dict keys -named tuple is alternate to objects, -func args passed as tuple. NOO!! append(), insert()
23. Dict are mutable, unique key w value. In other lang it is assoc. array,hash, hashmap called.
24. Use dict() func to convert. l1=[[a,b],[c,d]] dict(l1)= {a:b, c:d}
25. Convertable to dict:
-list of 2 item tuple: [(a,b),(c,d)]
-tuple of 2-item list: ([a,b],[c,d])
-list of 2-char str: ['ab','cd']
-tuple of 2-char str: ('ab','cd')
PS: zip() func make it easy to create 2-item sequences
26. When add item to dict, if key exist, it updates the value. Dict keys must be unique!!!
27. Update() method to combine dicts: d1.update(d2)
28. To delete k1: del dict['k1'], to delete all keys: dict.clear(), or dict={}
29. To see if key exist in dict: 'Sako' in dict: T/F
30. Get item by key: dict[k] -> value. If key not exist, you will get exception. To avoid it 2 ways: test using 'in', use get() method:: dict.get('Sako', 'Not in dict'). Otherwise, you get 'None'
31. Get all keys using keys(): dict.keys() -> dict_keys([a,b,c]). To make it iterable: list(dict.keys()) -> [a,b,c]
32. To obtain all values in dict use values():list(dict.values())
33. Get all k-v pairs using items(): list(dict.items()) -> [('green','go'),('red','blue')]
PS: As with list if you make change to dict, it will be reflected in all names refer to it.
34. To copy k/v from dict to another, use copy(): d2=d1.copy()
35. Set is like dict with its values thrown away, leaving only keys. As dict, each key must be unique, use only when want to know if smt. exists. As dict, keys are unordered. Empty_set=set()
36. Convert from list,str,tuple,dict to set by discarding duplicates: set('letters') -> {l,e,t,r,s}
37.Both enclosed w curly braces({}), set is just seq of values, dic is 1 or more k/v pairs.
38. Intersection: &, a & b -> {2} OR a.intersection(b) -> {2}
39. Union: |, a |b -> {1,2,3} OR a.union(b) -> {1,2,3}
40. Difference: a-b -> {1}, a.difference(b) -> {1}
41. Symmetric Difference: a^b ->{1,3} OR a.symmetric_difference(b)
42. To find if subset of another set: a<=b OR a.issubset(b) --> T/F
PS: Dict keys must be immutable, so tuple can, dict,list,set cannot be. List and tuple use index, dict use key. 
43. Proper subset: a<b -> T/F. B should have all elts of a and more.
44. Superset, opposite of subset: a>=b OR a.issuperset(b) A should have all elts. of B. Cannot be superset of itself: a>a


CH4:
1. False:  -boolean:False, -null:None, -zero integer/float:0/0.0, empty str/list/tuple/dict/set:''/[]/()/{}/set() 
2. Infinite loop with while: 
while True:
  stuff=input("Str to capitalize[type q to quit]:")
  if stuff=='q':
    break
  print(stuff.capitalize())
  





