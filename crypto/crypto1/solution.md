Answer: i_love_cats_meow

Explaination:
Caesar Cipher but each shift is exponential, meaning each letter is shifted by n^n, but the number gets too big so mod 26 to be in range:

Steps:  
1) The shifts for each position are:

    1^1=1
    2^2=4
    3^3=27        mod  26 = 1
    4^4=256       mod  26 = 22
    5^5=3125      mod  26 = 25
    6^6=46656     mod  26 = 4
    7^7=823543    mod  26 = 7
    8^8=16777216  mod  26 = 16
    9^9=387420489 mod  26 = 17
    10^10         mod  26 = 22
    11^11         mod  26 = 15
    12^12         mod  26 = 4
    13^13         mod  26 = 15

2) Now, decode each letter by subtracting the respective shift value (mod 26) from each position.

    'j' (position 10) → Shift back by 1 → 'i' (position 9)
    'p' (position 16) → Shift back by 4 → 'l' (position 12)
    'p' (position 16) → Shift back by 1 → 'o' (position 15)
    'r' (position 18) → Shift back by 22 → 'v' (position 22)
    'd' (position 4) → Shift back by 25 → 'e' (position 5)
    'g' (position 7) → Shift back by 4 → 'c' (position 3)
    'h' (position 8) → Shift back by 7 → 'a' (position 1)
    'j' (position 10) → Shift back by 16 → 't' (position 20)
    'j' (position 10) → Shift back by 17 → 's' (position 19)
    'i' (position 9) → Shift back by 22 → 'm' (position 13)
    't' (position 20) → Shift back by 15 → 'e' (position 5)
    's' (position 19) → Shift back by 4 → 'o' (position 15)
    'l' (position 12) → Shift back by 15 → 'w' (position 23)
