# Ansible Home Lab

This repository contains Ansible playbooks and roles for managing a home lab environment.

## Structure

- `inventories/` - Environment-specific inventory files
- `playbooks/` - Ansible playbooks for various tasks
- `roles/` - Reusable Ansible roles
- `ansible.cfg` - Ansible configuration file
- `requirements.yml` - External role dependencies

## Usage

### Running Playbooks

```bash
# Run the main site playbook
ansible-playbook -i inventories/dev/hosts.yml playbooks/site.yml

# Run updates
ansible-playbook -i inventories/dev/hosts.yml playbooks/update.yml

# Run health checks
ansible-playbook -i inventories/dev/hosts.yml playbooks/healthcheck.yml
```

### Environment Management

- `inventories/dev/` - Development environment
- `inventories/prod/` - Production environment

## Roles

- `common` - Basic system configuration
- `nginx` - Web server setup
- `docker` - Container runtime setup
