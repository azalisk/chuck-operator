# Chuck Norris jokes operator 

### `chuck-operator` deploy the following stack 


Run locally 

```bash
pipenv run ansible-playbook playbooks/chuck.yml --extra-vars='{"debug":"true","dry_run":"true","cluster_domain":"asd.asd","ansible_operator_meta":{"namespace":"cnvrg"}}'
```
