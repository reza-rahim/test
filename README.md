# Test

1. Create a VM instance on GCP with following
  
Requirement  | Specification  
------------ | -------------
CPU | 4
Memory | 15 GB
OS | Cent OS 7
Disk | 30 GB

2. ssh to the machine

```bash 
sudo su
sed -i 's/PermitRootLogin no/PermitRootLogin yes/' /etc/ssh/sshd_config
systemctl restart sshd
ssh-keygen -f ~/.ssh/id_rsa -t rsa -N ''
cat ~/.ssh/id_rsa.pub >> ~/.ssh/authorized_keys
```

3. Now ssh to public ip address to make sure we have passwordless access. 

