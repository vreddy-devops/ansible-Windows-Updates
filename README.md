# Ansible-Windows-Updates

## Dependencies
* Assumes Ansible is installed on the linux machine

## Configure Anbile for Windows 
[Manage Ansible with windows](https://github.com/vinod-reddy/ansible-Windows-Updates/wiki/Manage-Windows-with-Ansble---Configuration)

Ansible-playbook to update windows servers

```
ansible-playbook -i inventory/envieonmentname/hosts.yml update_windows_servers.yml -vv
```
