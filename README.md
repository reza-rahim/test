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
yum install -y git
sed -i 's/PermitRootLogin no/PermitRootLogin yes/' /etc/ssh/sshd_config
systemctl restart sshd
ssh-keygen -f ~/.ssh/id_rsa -t rsa -N ''
cat ~/.ssh/id_rsa.pub >> ~/.ssh/authorized_keys
```

3. Now ssh to public ip address of the machine to make sure we have passwordless access. 

4. Clone the repo

```bash
git clone https://github.com/gshipley/installcentos.git

```

5. Set the env varaible. Replace the public ip. Accepts all the defaults from install-openshift.sh.

```bash
cd installcentos/

export DOMAIN= {public Ip}.nip.io
export USERNAME=admin
export PASSWORD=admin

./install-openshift.sh
```



