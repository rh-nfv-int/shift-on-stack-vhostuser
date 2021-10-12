Ansible Role: Create MachineConfig for Shift-on-Stack Vhostuser Interface
=========================================================================

NOTE: Changed from sriov-device-plugin approach to host-device CNI approach via MachinseSet

Commands to create virtual env in undercloud
```
virtualevn /tmp/ansible_venv
source /tmp/ansible_venv/bin/activate
pip install kubernetes==11.0.0 openshift==0.11.0  ansible==2.9.12
```

Commands to create MachineConfig for driver binding
```
ansible-playbook play.yaml -e network_ids="d6441a96-b050-4119-85df-7cbca5d18314,6363fdc6-8754-4075-9040-4a44e481ef18"
```
