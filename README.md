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

- **Description of your code**
  - _Write a brief description here..._

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
