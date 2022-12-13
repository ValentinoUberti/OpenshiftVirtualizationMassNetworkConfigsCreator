# Simple ansible generator for creating NodeNetworkConfigurationPolicy (vlan and bridges) and NetworkAttachmentDefinition

These operations are a prerequisites for import VMs in Openshift Virtualization

Based on guidelines written by Fulvio Carrus (Red Hat)(Thanks!) 

## Steps:
- populate the .vars/vars.yaml with the vlans/bridges configuration to be created
- run ansible-playbook no_vlan_bridge_filtering.yaml or no_vlan_bridge_filtering.yaml
  - https://access.redhat.com/articles/6972285
- oc apply -f output.yaml