# Ansible-Windows-Updates

## Dependencies
* Assumes Ansible is installed on the linux machine
* Assumes Ansible can reach Windows host machines on the configured winrm port 
* Assumes windows machines have network access to get updates downloaded

## Configure Anbile for Windows 
[Manage Ansible with windows](https://github.com/vreddy-devops/ansible-Windows-Updates/wiki/Manage-Windows-with-Ansble---Configuration)

## Variables
[win_updates](https://github.com/vreddy-devops/ansible-Windows-Updates/tree/master/roles/win_updates) role installs the updates provided by the [win_updates](http://docs.ansible.com/ansible/latest/win_updates_module.html) module. 

## Playbook
```
---
- name: windows updates
  hosts: windows
  roles:
    - role: win_updates
      win_updates_category_names:
         - "CriticalUpdates"
         - "SecurityUpdates"
```
**win-updates_category_names**  can be updated in the playbook with list of categories to install updates from. 
* Application
* Connectors
* CriticalUpdates
* DefinitionUpdates
* DeveloperKits
* FeaturePacks
* Guidance
* SecurityUpdates
* ServicePacks
* Tools
* UpdateRollups
* Updates

## Ansible-playbook to update windows servers

```
ansible-playbook -i inventory/envieonmentname/hosts.yml update_windows_servers.yml -vv
```
