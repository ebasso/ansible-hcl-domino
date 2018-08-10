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

* IBM Domino 9.0.1
* IBM Domino 9.0.1 FP10
* IBM Domino 9.0.1 FP10 HF XX

2) Copy files to Web Server

## Configure Ansible hosts file

3) Change you ansible host file like **hosts.example**


## Cloning ansible-ibm-websphere from git

```
cd /etc/ansible

git clone https://github.com/ebasso/ansible-ibm-domino.git
```

## Running playbooks

```
cd /etc/ansible

ansible-playbooks -i environments/hosts.development -u <username> -k playbooks/ibm-domino-complete.yml
