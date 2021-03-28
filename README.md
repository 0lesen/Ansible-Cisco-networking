# Ansible Automate Cisco networking project
This was a small project that was created when trying to automate networking for Cisco devices.

The project is based on ansible software for automation.


# Project description

This project primary goal was to learn Ansible networking for Cisco devices.

The project contains:
* 2 Core Routers for redundancy
* Switch Stack for redundancy to VMware Cluster
* VMware Cluster with 3 nodes
* Shared Storage to VMware Cluster
* Firewall for protection

Network equipment used:
* Switch Stack = Cisco Crystal 3750-x
* Core Routes = Cisco Crystal 3750


Network devices must have enabled SSH for this to work.

look <b>cisco_manual_config.txt</b> for manual SSH configuration

The Ansible playbooks make it possible to configure Core Routers and Switch Stack.

This makes it easy to add vlans to the Switch Stack - to validate that the configuration is up to date and to update OSPF routing.


Simple high level network topology:

![GitHub Logo](/topology/Network_devices.png)

Low level project topology:

![GitHub Logo](/topology/Low-level.png)


<br>

# How to use this

This Ansible project contains roles that configure Cisco devices, based on information defined in host files.


Playbooks can contain different roles based on what to configure.


Predefined playbooks that can be used to seperate device configurations.
* cisco_all_roles.yml
* cisco_add_vlans.yml
* cisco_base_msw.yml
* cisco_base_interfaces.yml
* cisco_base_routing.yml

The playbook <b>cisco_backup_configs.yml</b> is made to gather device configurations and push it to GitHub if it changed.

This can be created as a role and implemented in both start and ending of a playbook, to track changed configuration.
<br>

# What is next?

* Implementing SSoT software to generate host files
* Try Ansible community modules
* Scale this to a large setup
* Implement this as a ZTP solution in some way
