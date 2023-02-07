# ansible-workstation-bootstrap
Ansible playbooks for bootstrapping a Linux workstation

## Roles

| Name     | Purpose                                         |
|----------|-------------------------------------------------|
| `common` | Install common components, programmes and files |
| `gpu`    | Install GPU-specific drivers and utilities      |

## Variables

| Name  | Role  | Description                        | Valid/Expected Values    |
|-------|-------|------------------------------------|--------------------------|
| `gpu` | `gpu` | Type of GPU present in workstation | `nvidia`, `amd`, `intel` |

