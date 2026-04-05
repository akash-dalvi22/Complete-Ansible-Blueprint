# 📘 Inventory of an Ansible

Welcome to the **Inventory** section of this repository.  
This guide will help you understand how we can create an inventory file.

When we install ansible one file is created ```hosts``` and when we run any ansible command then Ansible get the manage node details from that file ```/etc/ansible/hosts```



We can create our custom inventory file and use it with Ansible
#### Types of Inventory files
**1. Static Inventory -**  It is a Simple text file written in INI or YAML format and does not change dynamically at runtime. Static inventories are best suited for small or stable environments where infrastructure does not frequently change.

## Examples :-

### INI Format

inventory.ini

```
[webservers]
web1.example.com
web2.example.com

[dbservers]
db1.example.com

[all:vars]
ansible_user=ubuntu
ansible_ssh_private_key_file= (<location of the ssh private key file>)

```

### YAML Format

```
all:
  vars:
    ansible_user: ubuntu
    ansible_ssh_private_key_file: (<location of the ssh private key file>)

  children:
    webservers:
      hosts:
        web1.example.com:
        web2.example.com:

    dbservers:
      hosts:
        db1.example.com:
```

**2. Dynamic Inventory -** A dynamic inventory file is a script or plugin used by an Ansible to automatically generate and update the list of managed hosts at runtime. Instead of relying on a fixed, manually maintained list, a dynamic inventory fetches infrastructure details from external sources such as cloud providers, APIs, or databases.