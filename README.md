# Ansible Playbook to update Dynamic DNS Entries using AWS Route 53

## Overview
Ansible Playbook to update dynamic DNS entries using AWS Route 53.

Can be used as an alternative to dynamic DNS services such as afraid.org, noip.com, etc.

## Configuration

### AWS Authentication and Authorization

Create the following environment variables by adding to your local shell configuration file such as the $HOME/.bashrc

```
AWS_ACCESS_KEY=<key goes here>
AWS_SECRET_KEY=<secret goes here>
```

### Inventory file

Create an Ansible inventory file:

```
[local]
localhost   ansible_python_interpreter=/usr/local/bin/python3
```

### Executing

Run the playbook:

```
ansible-playbook -i hosts dynamic-aws.yaml
```
