# Confluent Kafka in KRaft & Ansible

## Starts 
- Confluent latest
- alpine/ansible

## Commands

 1. > docker-compose up -d
 1. > docker-compose exec -w /etc/data bastion bash
 1. > ansible-galaxy collection install confluent.platform
 1. > ansible -i hosts.yml all -m ping
 1. > ansible-playbook -i hosts.yml confluent.platform.validate_hosts
 1. > ansible-playbook -i hosts.yml confluent.platform.all
 
 After playbooks've been installed in e.g. con<1 | 2> container:
 
 > kafka-topics --bootstrap-server localhost:9092 --command-config /tmp/clientconfig/client.properties --list
 
 
 ## Control Center reachable on http://localhost:9021 (controlcenterAdmin: controlcenterAdmin)

