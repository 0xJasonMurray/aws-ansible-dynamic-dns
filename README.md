# Simple Dynamic DNS Client with Ansible and AWS Route 53

## Overview
Simple Ansible Playbook to update dynamic DNS entries using AWS Route 53.  Many of the other
systems out there are too complicated for such a simple service.  

Can be used as an alternative to dynamic DNS services such as afraid.org, noip.com, etc.

## Configuration

### Requirements

Install boto python library:

```
pip3 install boto
```

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

### Automatic Updates

Could be added to cron or Ansible Tower (there is a free 10 host license) for automatic updates.


