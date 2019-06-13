# ansible-ibm-domino

Ansible playbooks for IBM Domino, Traveler, ...

# Playbooks

| Playbook name                 | Status         |           Description                                        |
|-------------------------------|----------------|--------------------------------------------------------------|
| ibm-domino-complete.yml       | Complete       | Install IBM Domino 9.0.1 Server  |

# Roles

| Role name                       |            Description of Role                                          |
|---------------------------------|-------------------------------------------------------------------------|
| domino-install.yml              | Install IBM Domino Server   |
| domino-fp-install.yml           | Install IBM Domino Server Fix Pack  |
| domino-hf-install.yml           | Install IBM Domino Server Hot Fix  |

## Prerequisites

1) Download installation files:

* IBM Domino 10.0.1
* IBM Domino 10.0.1 FP2
* IBM Domino 10.0.1 FP2 HF XX

2) Copy files to Web Server

Example of my repository
```

-- domino
    |-- 10.0.1
    |   |-- DOM_SVR_V10.0.1_64_BIT_Lnx.tar
    |   |-- FP1
    |   |   |-- domino10001FP1_linux64.tar
    |   |   `-- 10.0.1FP1HF12.tar
    |   |-- FP2
    |   |   `-- domino10001FP2_linux64.tar
    |-- 9.0.1
    |   |-- DOMINO_9.0.1_64_BIT_LIN_XS_EN.tar
    |   |-- FP9
    |   |   |-- domino901FP9_linux64_x86.tar
    |   |   `-- 901FP9HF321.tar
    |   |-- FP10
    |   |   |-- domino901FP10_linux64_x86.tar
    |   |   |-- 9.0.1FP10HF48.tar
    |   |   `-- 9.0.1FP10HF541.tar

```


## Install ansible on your ansible manager machine.

* You can do: 
```
pip install ansible
```

* Setup ssh access from master to workers.
```ssh-copy-id -i ~/.ssh/id_rsa.pub <user@host>```


## Cloning ansible-ibm-websphere from git

```
cd /etc/ansible

git clone https://github.com/ebasso/ansible-ibm-domino.git

cd ansible-ibm-domino
```

## Configure Ansible hosts file

Change you ansible host file like **hosts_domino**


## Running playbooks

```
cd /etc/ansible

ansible-playbooks -i environments/hosts.development -u <username> -k playbooks/ibm-domino-complete.yml
```

## Community Support
Special Thanks go to the following people for having provided valuable input to this project

* Daniel Nashed for his [startscript](https://www.nashcom.de/nshweb/pages/startscript.htm) under the [Apache License 2.0](https://www.apache.org/licenses/LICENSE-2.0.html). 

## License

This project is licensed under the [Apache License 2.0](https://www.apache.org/licenses/LICENSE-2.0.html). 

