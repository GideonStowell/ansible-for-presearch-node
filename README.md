# ansible-for-presearch-node
Ansible playbook to setup presearch node on Ubuntu


# Features
This playbook will install a presearch node onto the target host(s) in **one simple command** matching the configuration found on the official [presearch website](https://docs.presearch.org/nodes/setup). Ansible allows for repeatable deployments and documentation of your deployments.

![Screenshot](assets/screenshot.png)

**Note** that you will need to acquire a registration code from presearch.org and stake PRE tokens to earn rewards as a node runner.

# Deployment
1. [Install ansible](https://docs.ansible.com/ansible/latest/installation_guide/intro_installation.html#installing-ansible-on-specific-operating-systems) on your laptop or workstation
2. Clone this repo: `git clone https://github.com/GideonStowell/ansible-for-presearch-node.git`
3. Change directories to the newly clone repo: `cd ansible-for-preasearch-node`
4. Rename `example-hosts.ini` to `hosts.ini` and edit to match your deployment (`mv example-hosts.ini hosts.ini` then `nano host.ini`)
5. Add your REGISTRATION_CODE into `vars.yml`
6. Run this command to deploy your node(s): `ansible-playbook -i hosts.ini playbook.yml`
7. Check your work by logging into the host and running `docker logs -f presearch-node`

# Support
Did you find this playbook helpful?? Consider donating to allow for continued development efforts on this project:

* PRE address: [0xFd91fd23594eb434Be83e8480AA1cF6AD27dD1cF](https://metamask.app.link/send/0xFd91fd23594eb434Be83e8480AA1cF6AD27dD1cF)
* XRP address: rJHaS2aoKFngQayJP8qqtibRMMV8819oFL
* NANO/XNO address: nano_3mskjdt66bi96m3wdu1ynnqgx5inhjeoe3bhg3um3mwwxtfbiehzp5tcqww5


### Testing
Currently, the playbook was tested with the use of Vagrant. Simply run:
`vagrant up`
and the playbook will execute once the vm has been provisioned.

After modifying the playbook further, run:
`vagrant provision` 
to rerun the playbook.




