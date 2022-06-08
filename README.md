# Ansible-adhoc

web01 ansible_host=172.31.19.132 ansible_user=centos ansible_ssh_private_key_file=profile-key.pem
web02 ansible_host=172.31.23.62 ansible_user=centos ansible_ssh_private_key_file=profile-key.pem
db01 ansible_host=172.31.31.253 ansible_user=centos ansible_ssh_private_key_file=profile-key.pem



[websrvgrp]
web01
web02

[dbsrvgrp]
db01

[dcohio:children]
websrvgrp
dbsrvgrp

[dcohio:vars]
ansible_user=centos
ansible_ssh_private_key_file=profile-key.pem
