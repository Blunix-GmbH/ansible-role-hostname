# Hostname Ansible Role (ansible-role-hostname) from Blunix GmbH

This Ansible role configures the system hostname and related `/etc/hosts` entries on Debian servers. Baseline playbooks run it across all hosts with defaults.

The Ansible Role is written and actively maintained by <a href="https://www.blunix.com" target="_blank">Blunix GmbH</a>.
It is used in the Blunix <a href="https://www.blunix.com/linux-managed-hosting.html" target="_blank">Linux Managed Hosting</a> Stack.
Its usage is documented at our <a href="https://www.blunix.com/manual" target="_blank">Linux Managed Hosting Documentation</a>.


## Features

- Sets the system hostname using the `hostname` module.
- Writes the hostname to `/etc/hostname`.
- Manages the `127.0.1.1` entry in `/etc/hosts` with fully qualified domain names and aliases.
- Exposes variables for hostname, domains, and aliases.


## Requirements

- Ansible: **>= 2.20.0**
- Managed operating systems:
  - Debian **trixie**



## Role variables and example playbook

Defaults are sufficient for most hosts. Override domains/aliases only when you need extra FQDNs in `/etc/hosts`. The example is split under `example/`:

- <a href="https://github.com/Blunix-GmbH/ansible-role-hostname/blob/main/example/play.yml" target="_blank">`example/play.yml`</a> — baseline play.
- <a href="https://github.com/Blunix-GmbH/ansible-role-hostname/blob/main/example/inventory/group_vars/example_web.yml" target="_blank">`example/inventory/group_vars/example_web.yml`</a> — optional domains/aliases.


## Author Information

Blunix GmbH Berlin  

`root@Linux:~# Support | Consulting | Hosting | Training`

Blunix GmbH provides 24/7/365 Linux emergency support and consulting, Service Level Agreements for Debian Linux managed hosting using Ansible Configuration Management as well as Linux trainings and workshops.

Learn more at <a href="https://www.blunix.com" target="_blank">https://www.blunix.com</a>.

## Contact Information

Click here to see our <a href="https://www.blunix.com/#contact" target="_blank">Contact Information</a>.

For bug reports and feature requests, please open an issue in this repository’s GitHub issue tracker.


## License

Apache-2.0

Please refer to the `LICENSE` file in the root of this repository.

### Tests

The directory `test/` contains an example `play.yml` as well as `inventory/group_vars/`, if applicable to the role. the script `example/run-tests.sh` creates a IONOS cloud instance with terraform, uses the example inventory and playbook to run the role and then run pytest tests located in `example/tests/`. Destroy the terraform using `./run-tests.sh -d`.
