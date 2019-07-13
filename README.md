# Allow only one IP host to access SSH


1. Make sure SSHD was built with TCP wrappers: 
```
ldd /usr/sbin/sshd | grep libwrap
```

2. Execute: 
```
nano /etc/hosts.allow
```

3. Add: 
```
sshd: YOUR_IP: ALLOW
sshd: ALL: DENY
```
