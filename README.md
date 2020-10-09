# Ansible playbook for Kubernetes deployment

This ansible-playbook contains a deployment of the Kubernetes cluster. It supports multiple control plane nodes (high availability).

## Supported Linux Versions

* CentOS 7
* Red Hat Enterprise Linux 7

_needs to be tested on other versions_

## Instruction

1. Copy [`inventories/example`](inventories/example) dir to something like `inventories/staging`.\
   This will be your ansible inventory.
2. Modify the `hosts` file, put your actual servers there.
3. Modify the [`group_vars/cluster.yaml`](group_vars/cluster.yaml) by following description there.
4. Run the playbook:
   ```
   # replace staging with your inventory name
   ansible-playbook -i inventories/staging playbook.yaml
   ```
