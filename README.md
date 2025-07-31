# Ansible-ACI-simple

This is a sample script to demonstrate the basics of what Ansible can do with ACI. It will create a tenant, AP, VRF and a few EPGs and BDs. This example reads the variable.yaml for some variables, and also parses a comma seperated value file whcih some may find easier for entering repetitive data.

To run the code and create the objects in ACI, be sure to set the state_cli to present as shown as follows: `ansible-playbook -i inventory-file epg-playbook.yaml -e @variables.yaml -e state_cli=present`

Then set the state to absent to remove the objects: `ansible-playbook -i inventory-file epg-playbook.yaml -e @variables.yaml -e state_cli=absent`
