
## What is

This is [Ansible](https://blog.codecentric.de/en/2014/06/ansible-simple-yet-powerful-automation/) playbook to install Jenkins Master machine

## Compatible operating systems

- Debian like (APT)

## You need

- Python 2.7
- [Ansible](http://docs.ansible.com/intro_installation.html#latest-releases-via-apt-ubuntu)
- Debian package `sshpass` (for ask password)

You need this packages to **Python 2.7**, because modules using:

- python-apt
- python-urllib3

## How to use

- Fill `master` file with IP(s) of the machine(s)

```
[master]
<IP> ansible-ssh-user=<user-client-machine>
```

> One per line

- Enter `vars` directory and edit variables what you need
- Execute command:

```
$ ansible-playbook -i master playbook.yml --ask-pass --ask-sudo-pass
```
    - `--ask-pass`: password to ssh connection
    - `--ask-sudo-pass`: password to remote_user
