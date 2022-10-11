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

### for AWS environment
#### How to retrieve `.ansible_vault` file

Run following command.
```bash
$ aws ssm get-parameters --names /Ansible/Vault --with-decryption --query Parameters[].Value --region ap-northeast-1 --output text
```

#### How to run

Run following command. (You have to prepare `.ansible_vault` file.)
```bash
ansible-playbook -i localhost, -c local --vault-password-file .ansible_vault PLAYBOOKFILE
```