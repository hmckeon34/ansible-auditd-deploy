This project automates the installation and configuration of **auditd**, the Linux Auditing System, using **Ansible** and a **GitHub-hosted ansible-pull workflow**.

Auditd is important because it:
- Logs critical system activity 
- Records authentication changes 
- Tracks file modifications 
- Provides security teams with required audit trails 
- Supports compliance frameworks such as PCI-DSS, HIPAA, and CJIS 

 System Requirements
| Component | Requirement |
|----------|-------------|
| Operating System | Ubuntu 24.x LTS |
| Ansible Version | ansible-core 2.15+ |
| Required Packages | git, ansible, auditd, python3 |

     +----------------------+
     |      GitHub Repo     |
     |  (auditd playbook)   |
     +----------+-----------+
                |
                | ansible-pull
                v
     +---------------------------+
     | Ubuntu 24.x Target System |
     |  - Pulls playbook         |
     |  - Installs auditd        |
     |  - Applies rules          |
     +-----------+---------------+
                 |
                 | audit logs
                 v
     +---------------------------+
     |  /var/log/audit/audit.log |
     +---------------------------+
