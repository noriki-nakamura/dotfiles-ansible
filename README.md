dotfiles-ansible
================

This repository provides dotfiles and playbooks for ansible.

# How to Run
## Preparation
### Install ansible

In Ubuntu environment, run following commands.
```bash
$ sudo apt update && sudo apt install ansible
```

## Run playbook
### for localenvironment

Run following command.
```bash
$ ansible-playbook -i localhost, -c local deploy.yaml
```