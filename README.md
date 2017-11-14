Ansible playbook
=================

# Clone this repo
This repo has submodules in folder role
```
git clone https://repu-url --recursive
```

# Role used:
The role are included as submodule in the roles folder, to avoid to manage it with ansible-galaxy
* [epel](https://galaxy.ansible.com/sfromm/epel/)
* [nginx](https://github.com/datadog-galaxy/nginx.git)
* [repo-remi](https://github.com/hostclick/remi_repo.git)
* [solr](https://github.com/geerlingguy/ansible-role-solr.git)
* [java-oracle](https://github.com/William-Yeh/ansible-oracle-java.git)

# How to run playbook
1. Change hosts file
2. Install role dependency
3. Check ansible
```
ansible-playbook -i dynamic_inventory/ec2.py --list-hosts --extra-vars "env=produzione" --private-key  ~/keys/opencontent/key.pem site.yml
```
4. If ec2.ini is locatend in another folder than the ec2.py script export the path:
```
export EC2_INI_PATH=/path/to/custom/ini/ec2.ini
```

Run ansible staging:
```
ansible-playbook -i dynamic_inventory/ec2.py --extra-vars "env=staging" --private-key ~/keys/opencontent/EU-XPeppers-collaudo.pem site.yml
```# xp-opencontent-ansible-migrazione
