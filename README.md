<img width="858" alt="image" src="https://github.com/user-attachments/assets/d6a3b91a-d820-42d9-9839-d5bd836722c3">

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

