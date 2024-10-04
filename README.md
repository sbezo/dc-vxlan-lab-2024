<img width="852" alt="image" src="https://github.com/user-attachments/assets/87cc90f9-e2e6-467d-9967-8e2ca45f0ad7">


# Manual configuration
EVPN BGP VXLAN fabric was manually configured on Nexus 9300V virtual switches via:
1. Underlay_scipts
2. Overlay_scripts

After connectivity tests, configuration was saved and Overlay fabric was completly unconfigured from all switches:

destroy_overlay.txt

There is a possibility to transit between fully deployed fabric and underlay network configuration only for testing purposes:

lab_transitions.txt


# Ansible configuration
see /Ansible/notes.txt for details

full stack site playbook:
ansible-playbook -i inventories/staging/hosts.yml --ask-vault-password site.yml

