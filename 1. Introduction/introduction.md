# 📘 Introduction to Ansible

Welcome to the **Introduction** section of this repository.  
This guide will help you understand the basics of Ansible and its core concepts.

---

## 🔍 What is Ansible?

Ansible is an open-source automation tool used for:

- Configuration Management
- Application Deployment
- Task Automation
- Infrastructure as Code (IaC)

It allows IT administrators and developers to automate repetitive tasks like installing software, configuring servers, and managing systems across multiple machines.

---

## ⚙️ Key Features

- **Agentless Architecture**  
  No need to install software on managed nodes.

- **Simple Syntax**  
  Uses YAML, which is easy to read and write.

- **Powerful Automation**  
  Supports simple to complex IT workflows.

---

## ❓ Why Use Ansible?

- **Simplifies Complex Tasks**  
  Automates manual processes like deployments and configurations.

- **Consistency**  
  Ensures all systems are configured uniformly.

- **Scalability**  
  Can manage one or thousands of systems.

- **Agentless**
  Ansible is agentless in nature, which means you don't need install any software on the manage nodes.
  Uses SSH (Linux/Unix) and WinRM (Windows).

---

## 🧩 Core Components

### 🔹 Control Node
The machine where Ansible is installed and executed.

### 🔹 Managed Nodes
The systems that Ansible manages.

### 🔹 Inventory
A file that contains the list of hosts (servers).

### 🔹 Modules
Pre-built tools used to perform tasks (e.g., install packages, manage services).

### 🔹 Playbooks
YAML files that define automation tasks.

Example:

```yaml
- name: Install nginx
  hosts: webservers
  tasks:
    - name: Install nginx package
      yum:
        name: nginx
        state: present