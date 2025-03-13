# Ansible Playbooks

This project contains a collection of Ansible playbooks and roles designed for automating tasks across multiple hosts.

## Directory Structure

- **group_vars/**: Contains global variables applicable to all hosts.
  - `all.yml`: Global variables for the playbooks.

- **host_vars/**: Contains host-specific variables.
  - `example_host.yml`: Variables specific to the host `example_host`.

- **roles/**: Contains reusable roles.
  - **example_role/**: A sample role demonstrating the structure.
    - **tasks/**: Contains task definitions.
      - `main.yml`: Main tasks for the role.
    - **handlers/**: Contains handlers triggered by tasks.
      - `main.yml`: Handlers for the role.
    - **templates/**: Jinja2 templates for dynamic configuration files.
    - **files/**: Static files to be copied to target hosts.
    - **vars/**: Role-specific variables.
      - `main.yml`: Variables for the role.
    - **defaults/**: Default variables for the role.
      - `main.yml`: Default values that can be overridden.

- **inventory**: Lists the hosts and groups of hosts managed by Ansible.

- **playbook.yml**: The main playbook orchestrating tasks across defined hosts.

## Usage

To run the playbooks, use the following command:

```
ansible-playbook playbook.yml -i inventory
```

Make sure to customize the `inventory` file and the variable files as needed for your environment.