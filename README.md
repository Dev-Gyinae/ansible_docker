# ansible_docker

Add Secrets to ansible vault in a prod instance
      ansible-vault encrypt /etc/ansible/secrets.yml

refrence the path in the docker_play yaml files:

    vars_files:
        - /etc/ansible/secrets.yml

run playbook:
ansible-playbook docker_play.yml --ask-vault-pass


Edit vault later by:
ansible-vault edit /etc/ansible/secrets.yml

Remove encryption by:
ansible-vault decrypt /etc/ansible/secrets.yml
