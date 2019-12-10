# ansible-aci-ng

The `ansible-aci` project provides an Ansible collection for managing and automating your Cisco ACI environment.
It consists of a set of modules and roles for performing tasks related to ACI.

> Note: This collection is not compatible with versions of Ansible before v2.8.


## Requirements

- Ansible v2.9 or newer
- APIC v4.2 or newer


## Use

Once the collection is installed, you can use it in a playbook by specifying the full namespace path to the module, plugin and/or role.

```yaml
- hosts: aci
  gather_facts: no

  tasks:
  - name: Add a new EPG
    cisco.aci.aci_epg:
      hostname: apic
      username: admin
      password: SomeSecretPassword
      tenant: production
      ap: intranet
      epg: web_epg
      description: Web Intranet EPG
      bd: prod_bd
    delegate_to: localhost
```
