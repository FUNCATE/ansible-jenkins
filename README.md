
## What is

This is Ansible playbook to install Jenkins Master machine

## Compatible operating systems

- Debian like (APT)

## You need

- Python 2.7
- Ansible
- Debian `sshpass` for ask password

You need this packages to **Python 2.7**, because modules using:

- python-apt
- python-urllib3

## How to use

- Fill `master` file with IP(s) of the machine(s)

```
[master]
<IP>
```

> One per line

- Enter `vars` directory and edit variables what you need
- `remote_user` in `playbook.yml` with user in future master machine(s)
- Execute command:

```
$ ansible-playbook -i master playbook.yml --ask-pass --ask-sudo-pass
```
    - `--ask-pass`: password to ssh connection
    - `--ask-sudo-pass`: password to remote_user

## TODO

- Create plugins array in file `vars/master.yml`
