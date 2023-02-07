# ansible-workstation-bootstrap
Ansible playbooks for bootstrapping a Linux workstation

## Pre-requisites

1. Minimal install of chosen Linux distribution (warning: currently only tested with Artix)
2. Ansible and Git installed on the system

## Usage

Clone the repo to an appropriate location in your home directory and run locally:

```shell
ansible-playbook main.yaml -K --extra-vars ...
```

or use `ansible-pull` to fetch and run it:

```shell
ansible-pull https://github.com/cjrowe/ansible-workstation-bootstrap main.yaml -K --extra-vars ...
```

## Roles

| Name     | Purpose                                         |
|----------|-------------------------------------------------|
| `common` | Install common components, programmes and files |
| `gpu`    | Install GPU-specific drivers and utilities      |

## Variables

| Name  | Role  | Description                        | Valid/Expected Values    |
|-------|-------|------------------------------------|--------------------------|
| `gpu` | `gpu` | Type of GPU present in workstation | `nvidia`, `amd`, `intel` |

