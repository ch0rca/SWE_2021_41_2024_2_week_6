# SWE_2021_41_2024_2_week_6

## Week 4 Assignment
- [**Week 4 Repository**](https://github.com/ch0rca/SWE_2021_41_2024_2_week_4)
```python
def isHappy(n):
  visited = set()
  while n != 1:
    n = sum(int(i) ** 2 for i in str(n))
    if n in visited:
      return False
    visited.add(n)
  return True

n = int(input("Input: "))
print("Output: ",isHappy(n))
```

- **Description of code**
  
The function `isHappy(n)` determines whether a given number `n` is a **"happy number"**  .
A happy number is a number that eventually reaches `1` when replaced by the sum of the squares of its digits, without entering an endless cycle.
#### Function Explanation:

#### 1. Initialization:
- A set `visited` is initialized to store numbers that have been previously encountered during the process. This helps detect cycles and prevents infinite loops.

#### 2. Main Logic:
- The function enters a `while` loop that continues until `n` becomes `1`.
- Inside the loop, the sum of the squares of the digits of `n` is calculated using the following generator expression and is assigned back to `n`:
  ```python
  n = sum(int(i) ** 2 for i in str(n))
- If this new value of `n` is already in the visited set, it means the number is stuck in a cycle and will never reach 1. In this case, the function returns False, indicating that the number is not a happy number.
- If `n` is not in the set, it gets added to visited to track the values that have been checked.

#### 3. Termination:
- If `n` reaches 1, the function returns True, meaning that the number is a happy number.

#### 4. Input/Output:
- The user is prompted to input an integer `n`.
- The function isHappy(n) is called, and the result (True or False) is printed as the output.

#### 5. Example:
- If the input is 19, the process goes as follows:
```
19 → 1² + 9² = 82 
82 → 8² + 2² = 68 
68 → 6² + 8² = 100
100 → 1² + 0² + 0² = 1 (Happy number)
```
- If the input is 2, the sum of the squares of its digits will eventually enter a cycle, and the function will return False.
  
---

## Week 5 Assignment

>```bash
>docker exec <your container> cat /etc/os-release</code>
>```
> - Explanation of commandline and your output

>```bash
>python docker exec <your container> git --version
>```
> - Explanation of commandline and your output

>```bash
>docker exec <your container> python3 --version
>```
> - Explanation of commandline and your output

>```bash
>docker inspect --format="{{ .HostConfig.Binds }}" <container_name>
>```
> - Explanation of commandline and your output
