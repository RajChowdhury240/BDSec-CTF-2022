```py
def y_(c):

    a = list(c)

    for i in range(len(c)-1):
        b = chr(c[i]^c[i+1])
        a[i] = b
    return "".join(a[:-1])


a = bytes.fromhex('397b3f6c296a117f4f3b6451613e5b6f5a237c14412916497d4e7d')
print(y_(a)+"}")
```
![](dominos.png)
