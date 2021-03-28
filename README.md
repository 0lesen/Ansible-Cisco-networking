# Ansible Automate Cisco networking
This was a small project that was created when trying to automate networking for Cisco devices.

The project is based on ansible software for automation.


<br>

This Ansible project contains roles that configure Cisco devices, based on information defined in host files.


Playbooks can contain different roles based on what to configure.


I have predefined some playbooks that can be used to seperate device configurations.
* cisco_all_roles.yml
* cisco_add_vlans.yml
* cisco_base_msw.yml
* cisco_base_interfaces.yml
* cisco_base_routing.yml


Network topology:
![GitHub Logo](/topology/Network_devices.png)

Low level project topology:
![GitHub Logo](/topology/Low-level.png)

How to scale this project?

Try to implement some SSot software to generate host files.






