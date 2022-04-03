## About
Ansible playbook to read secret name/path from a kubernetes Secret manifest file, then fetch the real secret value from HashiCorp Vault, and then finally automatically encrypt the secret's value using the kubeseal command to produce a SealedSecret manifest file.

## Installation
```
ansible-galaxy collection install community.hashi_vault

Kubeseal (helm and kubeseal command):
https://github.com/bitnami-labs/sealed-secrets
```

## Run
```
ansible-playbook -i inventory --vault-password-file=ansible-vault.secret  playbooks/k8s-encrypt-secrets/main.yml
```