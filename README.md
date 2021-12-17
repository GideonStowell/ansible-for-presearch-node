# ansible-for-presearch-node
Ansible playbook to setup presearch node

# Testing
Currently, I can test the playbook with the use of Vagrant. Simply run:
`vagrant up`
and the playbook will execute once the vm has been provisioned
After modifying the playbook further, run:
`vagrant provoision` 
to rerun the playbook.

# Features
This playbook will install a presearch node onto the target host matching the configuration found on the official [presearch website](https://docs.presearch.org/nodes/setup). Note that you will need to acquire a registration code from presearch.org and stake PRE tokens to earn rewards as a node runner.

# Deployment
Run this command to deploy your node:
`ansible-playbook -i hosts playbook.yml`
