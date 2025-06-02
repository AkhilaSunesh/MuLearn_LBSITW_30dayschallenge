# CamelCase

## 📝 Problem  
There is a sequence of words written in CamelCase as a single string. The rules are:

- The string is a concatenation of one or more words.
- The first word consists only of lowercase English letters.
- Each subsequent word starts with an uppercase letter followed by lowercase letters.

**Task**: Given such a string, determine the number of words in it.

### Example  
**Input:**  
```
saveChangesInTheEditor
```

**Output:**  
```
5
```

---

## 💡 Approach  

1. Get each and every letter.
2. Check if it is uppercase using a comparison.
3. If so, increment a counter by 1.
4. Finally, add 1 to the result to count the first lowercase word.

---

## 🧾 Code (Python 3)

```python
#!/bin/python3

import math
import os
import random
import re
import sys

def camelcase(s):
    c=0
    d=len(s)
    for i in range(d):
        if s[i] in "ABCDEFGHIJKLMNOPIQRSTUVWXYZ":
            c=c+1
    c=c+1
    return c

if __name__ == '__main__':
    fptr = open(os.environ['OUTPUT_PATH'], 'w')

    s = input()

    result = camelcase(s)

    fptr.write(str(result) + '\n')

    fptr.close()
```

---

## Submissions:
![image](https://github.com/user-attachments/assets/8ab08a24-805a-4456-a31b-90d246703e7a)


## Leaderboard:
![image](https://github.com/user-attachments/assets/2cb3a0ab-bf5e-4fe9-a741-525084683808)

