# Diagonal Difference

## 📝 Problem  
Given a square matrix, calculate the **absolute difference** between the sums of its diagonals.

### Example  
For the square matrix `arr` shown below:
<table>
  <tr><td>1</td><td>2</td><td>3</td></tr>
  <tr><td>4</td><td>5</td><td>6</td></tr>
  <tr><td>7</td><td>8</td><td>9</td></tr>
</table>

- **Primary diagonal**: 1 + 5 + 9 = 15  
- **Secondary diagonal**: 3 + 5 + 7 = 15  
- **Absolute difference** = |15 - 15| = 0

---

## 💡 Approach  

1. Initialize `pd` for primary diagonal and `sd` for secondary diagonal.
2. Traverse the matrix:
   - Add `arr[i][j]` to `pd` (primary diagonal)
   - Add `arr[i][n-j-1]` to `sd` (secondary diagonal)
3. Return `abs(pd - sd)`

---

## 🧾 Code (Python 3)

```python
#!/bin/python3

import math
import os
import random
import re
import sys

def diagonalDifference(arr):
    pd = 0  
    sd = 0 
    c = len(arr)
    
    for i in range(c):
        pd += arr[i][j]
        sd += arr[i][c - j - 1]
    
    return abs(pd - sd)

if __name__ == '__main__':
    fptr = open(os.environ['OUTPUT_PATH'], 'w')

    n = int(input().strip())
    arr = []

    for _ in range(n):
        arr.append(list(map(int, input().rstrip().split())))

    result = diagonalDifference(arr)
    fptr.write(str(result) + '\n')
    fptr.close()
```

## Submissions:
![image](https://github.com/user-attachments/assets/166c6905-e3b8-422a-890a-a25ddcfbd2d6)
## Leaderboard:
![image](https://github.com/user-attachments/assets/eb76616c-69ac-4057-a9e2-eb50148d776b)


