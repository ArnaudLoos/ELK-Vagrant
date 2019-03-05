This repository contains a Vagrantfile and Ansible Playbook to deploy Elasticsearch, Logstash, and Kibana on a single Virtual machine using Virtualbox as the provider


To generate a password has to use for the local user:
```
pip install passlib
python -c "from passlib.hash import sha512_crypt; print sha512_crypt.encrypt('plaintextpassword')"
```
