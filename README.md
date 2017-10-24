# install_ansible_on_ubuntu

# Update

```
sudo apt-get update
sudo apt-get install software-properties-common
```


```
sudo apt-add-repository ppa:ansible/ansible
```

Accept the PPA addition.

# Refresh our system's package index.

```
sudo apt-get update
```

# Install Ansible.

```
sudo apt-get install ansible
```

# Setup ssh using Hosts

Setup Hosts


```
sudo vim ~/.ssh/config
```

save the config with the following contents:

```
Host __name__of__my__remote__system
    HostName __my__remote__system__ip
    User __my__remote__system_username
```


Generate key.

```
ssh-keygen
```

Leave it balnk and hit enter/return. Enter passphrase, or leave it empty and hit enter/return key twice.

# Copy key to remote system

```
ssh-copy-id __my__remote__system_username@__my__remote__system__ip
```

Say yes and enter remote system password.


login to remote system

```
ssh __name__of__my__remote__system
```

# Setup ssh using key

Generate key.

```
ssh-keygen
```

Enter filename in which to save the key and hit enter/return. Enter passphrase, or leave it empty and hit enter/return key twice.

# Copy key to remote system

```
ssh-copy-id -i name_of_keygenerated __my__remote__system_username@__my__remote__system__ip
```

Say yes and enter remote system password.


login to remote system

```
ssh -i ~/name_of_keygenerated __name__of__my__remote__system
```




