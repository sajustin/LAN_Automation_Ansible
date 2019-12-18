# Ansible playbook examples for LAN Automation Catalyst 9000 serie

This repository contains some basic Ansible playbooks to start your automation journey on Catalyst 9000. It will guide you through the setup of your Ansible environment and give some examples of inventory and configuration playbooks.

## Getting Started


### Prerequisites
A workstation running Linux or OSX. Although it can be used to manage Windows, Ansible does not run on Windows as the control station.

### Components
* Modules are typically written in Python. They are typically copied to remote hosts and run by the Ansible tool. Ansible modules are referenced as tasks in Ansible playbooks or using CLI arguments in the Ansible ad-hoc CLI tool. - native IOS modules that are included in Ansible 2.5 and later to interact with IOS XE:  https://docs.ansible.com/ansible/latest/modules/list_of_network_modules.html#ios
* Inventory files file that contain an inventory of the hosts to manage. When executing Ansible, it will look at the config file and command line to determine which inventory file to use for that run. Subsequent runs can leverage different inventory files, allowing users to break large infrastructure environments into smaller batches easily.
* Playbooks are written in YAML and contain Ansible domain-specific language (DSL). To enable reuse, playbooks can be modularized much like software. Variables containing data for playbooks can be separated into YAML files residing on the Ansible control machine.
* Configuration files control how the tool runs. For example, the configuration file can change the default directories of the modules.

### Using Ansible

The following list describes more useful CLI tools that Ansible provides.
* The ansible CLI tool runs modules against targeted hosts. This is commonly referred to as the ad-hoc CLI. Engineers can run tasks against targeted hosts without creating playbooks containing Ansible DSL.
* The ansible-playbook CLI tool runs playbooks against targeted hosts. Playbooks contain Ansible domain-specific language in YAML.
* The ansible-vault CLI tool enables engineers to encrypt sensitive data. If a playbook requires access to data that engineers do not want to expose in plain text, the ansible-vault tool can be used to create an encrypted YAML file containing the sensitive data. When data needs to be accessed, a password is provided.
* The ansible-pull tool enables clients to "pull" modules from a centralized server. (Normally, Ansible pushes modules out from a control station to the managed hosts.)
* The ansible-docs CLI tool enables engineers to parse the docstrings of Ansible modules to see example syntax and the parameters modules require.
* The ansible-galaxy tool can create or download roles from the Ansible community. Ansible Galaxy is a public repository of Ansible playbooks grouped into roles from the community. Roles provide a method to package Ansible playbooks for re-use.
