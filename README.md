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

| Name             | Purpose                                              |
|------------------|------------------------------------------------------|
| `common`         | Install common components, programmes and files      |
| `gpu`            | Install GPU-specific drivers and utilities           |
| `shell`          | Install and configure shell, including dotfiles etc. |
| `window-manager` | Install and configure WM for system                  |

## Variables

| Name                    | Role             | Description                                                   | Valid/Expected Values        |
|-------------------------|------------------|---------------------------------------------------------------|------------------------------|
| `user_name`             |                  | Local Unix user name to configure                             |                              |
| `gpu`                   | `gpu`            | Type of GPU present in workstation                            | `nvidia`, `amd`, `intel`     |
| `dotfiles_repo`         | `shell`          | URL of Git repository containing (`chezmoi` managed) dotfiles | HTTPS link to Git repository |
| `dwm_custom_repo`       | `window-manager` | URL of Git repository containing custom spin of dwm           | HTTPS link to Git repository |
| `dmenu_custom_repo`     | `window-manager` | URL of Git repository containing custom spin of dmenu         | HTTPS link to Git repository |
| `st_custom_repo`        | `window-manager` | URL of Git repository containing custom spin of st            | HTTPS link to Git repository |
| `dwmblocks_custom_repo` | `window-manager` | URL of Git repository containing custom spin of dwmblock      | HTTPS link to Git repository |
