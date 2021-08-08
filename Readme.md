
To deploy ELK STACK
  ansible-playbook -i inventory elk.yml

To deploy logstash role only
ansible-playbook -i inventory elk.yml --tag logstash

To deploy Nginx role to localhost
ansible-playbook -i inventory elk.yml --tags nginx --extra-vars "ehosts=local"


To deploy the nginx role to localhost with a specified user
ansible-playbook -i inventory elk.yml --tags nginx --extra-vars "ehosts=local" -u username


To clean ELK STACK
ansible-playbook -i inventory elk.clean.yml

To clean logstash role only
ansible-playbook -i inventory elk-clean.yml --tags logstash



Installing Ansible on local machine
using pip 
pip install ansible
pip install docker
pip install requests



ansible-playbook -i inventory elk.yml --connection=local