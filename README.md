Ansible Playbooks for
- Setup VM environment on openstack (i.e image, flavor, key-pair, and netwrk setup ). (vm_env_setup.yml)
- Create VM on openstack (vms_creation.yml)
- Fio deployment. (fio_deployment.yml)
- Setup node exporter on nodes (setup_nodexporter.yml)
- Setup prometheus (prometheus_env_setup.yml)
- Setup grafana on admin node for graphical view (grafana_setup.yml)


Ansible host file configuration
[fio]
#list down all loadgen nodes ip or hostnames
[controller_nodes]
#stamp controller node
[node_exporter]
[prometheus]
[grafana]

Linux Jump host:
git clone /etc/ansible/https://github.com/MuhammadAsif1/Ansible-playbooks.git

Run this command 
ansible-playbook -i /etc/ansible/Ansible-playbooks/hosts /etc/ansible/Ansible-playbooks/master-playbook.yml --key-file "/etc/ansible/ssh-key.pem"
