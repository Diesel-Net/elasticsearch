[![Build Status](https://drone.kiwi-labs.net.net/api/badges/Diesel-Net/elasticsearch/status.svg)](https://drone.kiwi-labs.net.net/Diesel-Net/elasticsearch)

# elasticsearch
Elastic Search cluster automation for our EFK stack.

## Notes
- [Traefik configuration](https://marcofranssen.nl/building-a-elasticsearch-cluster-using-docker-compose-and-traefik)

## Installing External Dependencies
Ansible core version `2.10.3` was used at the time of this writing.
```bash
ansible-galaxy install -r .ansible/roles/requirements.yaml -p .ansible/roles --force
```

## Deploy
```bash
ansible-playbook .ansible/deploy.yaml -i .ansible/inventories/production/hosts --vault-id ~/.tokens/vault.txt
```
