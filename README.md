# ansible_docker

Add Secrets to ansible vault in a prod instance
      ansible-vault encrypt /etc/ansible/secrets.yml

refrence the path in the docker_play yaml files:

    vars_files:
        - /etc/ansible/secrets.yml

run playbook:
