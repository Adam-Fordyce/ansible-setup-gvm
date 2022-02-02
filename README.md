# Ansible Setup GVM Environment

Ansible code to setup a local GVM environment on Linux for developing Go

> Targeted Ubuntu 20.04 LTS 

## Introduction

## Setup

### Enable sudo access

Before Ansible can run with become set to true sudoer access must be enabled.

```
su - root
# Enter Password

visudo

# Add the following line to the end of the sudoers file, replacing {{ username }} with your username
{{ username }}	ALL(ALL)	NOPASSWD: ALL
```

### Install Ansible

Use the default package repository to install Ansible

```
sudo apt install ansible
```

## Examples

Setup the GVM environment

```
ansible-playbook -i inventory setup.yml
```

## Author

Adam Fordyce
