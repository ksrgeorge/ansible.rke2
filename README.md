# ansible.rke2
This is a work in progress RKE2 installation over ansible with vagrant

STEPS
1. Please generate an ssh keypair and add the public key under ansible_provisioning/roles/create_users/files/.
2. Then add the name of the user in the file ansible_provisioning/group_vars/all.yml
3. Switch in the vagrant directory and execute vagrant up

This will spin up 3 VMs (1 load balancer and 3 cluster nodes)
Then ssh to the 10.50.10.11 node and:
1. cd /usr/local/bin
2. ./rke2 server --config /etc/rancher/rke2/config.yaml --selinux
