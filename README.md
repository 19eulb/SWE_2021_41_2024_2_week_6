# SWE_2021_41_2024_2_week_6
---
### Week 4 Assignment
* https://github.com/19eulb/SWE_2021_41_2024_2_week_4

```python
def isHappy(n):
  num = set()

  while n != 1 and n not in num:
    num.add(n)
    n = sum(int(digit)**2 for digit in str(n))
  return n==1

n = int(input())
output = print(isHappy(n))
```

* First define function isHappy and delcare an empty set. while loop runs in 2 conditions. n != 1 because it is happy if n is 1, and not in set to avoid repeating. Then add number n to num and convert to string and sum after squaring each digits.

  ---

  ### Week 5 Assignment
  > <pre><code> docker exec ossp-container cat /etc/os-release </pre></code>
  >> + show the operating system information of the running Docker container

  > <pre><code> docker exec ossp-container git --version </pre></code>
  >> + check the version of Git installed in the running Docker container

  > <pre><code> docker exec ossp-container python3 --version </pre></code>
  >> + check the version of Python 3 installed in the running Docker container
  
  > <pre><code> docker inspect --format="{{ .HostConfig.Binds }}" <ossp-container> </pre></code>
  >> + gprint the path of mounted directory of the Docker container
