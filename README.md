This repository here automates the installation and configuration of **auditd**, the Linux Auditing System, using **Ansible** and a **GitHub-hosted ansible-pull workflow**. That was the goal of this repository here

Auditd is important because it:
- Logs critical system activity  
- Records authentication changes  
- Tracks file modifications  
- Provides security teams with required audit trails  
- Supports compliance frameworks such as PCI-DSS, HIPAA, and CJIS  

This repository contains an Ansible playbook designed to deploy a hardened auditd configuration on an Ubuntu 24.x system.


| Component | Requirement |
|----------|-------------|
| Operating System | Ubuntu 24.x LTS |
| Ansible Version | ansible-core 2.15+ |
| Required Packages | git, ansible, auditd, python3 |
| Access | SSH key-based access to GitHub |

Visual Setup
     +-----------------------------+
     |         GitHub Repo         |
     |     (auditd playbook)       |
     +-------------+---------------+
                   |
                   | ansible-pull
                   v
     +-----------------------------+
     |   Ubuntu 24.x Target VM     |
     |  - Pulls playbook           |
     |  - Installs auditd          |
     |  - Applies rules            |
     +-------------+---------------+
                   |
                   | audit logs
                   v
     +-----------------------------+
     |  /var/log/audit/audit.log   |
     +-----------------------------+
