# Chuck Norris jokes operator 

### `chuck-operator` deploying the following stack 
![alt text](./config/samples/chuck-operator.png)

### Quick start
1. Install [make](https://man7.org/linux/man-pages/man1/make.1.html)
2. Build operator image `IMG="<SET-YOUR-IMAGE-NAME>" make docker-build && IMG="<SET-YOUR-IMAGE-NAME>" make docker-push`
3. Deploy new operator image `IMG="<SET-YOUR-IMAGE-NAME>" make deploy` 
4. Create chuck CR instance `kubectl create -f ./config/samples/chuck.yaml` (set `clusterDomain: <DOMAIN_WAS_SENT_BY_EMAIL>` to the valid domain)
5. Remove deployment `IMG="<SET-YOUR-IMAGE-NAME>" make undeploy`

### Development
1. Install [Pipenv](https://pipenv.pypa.io/en/latest/) 
2. `git clone https://github.com/Dimss/chuck-operator.git && cd chuck-operator/`
3. Install dependencies `pipenv install`
4. Run ansible locally `pipenv run ansible-playbook playbooks/chuck.yml --extra-vars='{"debug":"true","dry_run":"true","cluster_domain":"chuck.example.com","ansible_operator_meta":{"namespace":"chuck"}}'` 
5. Run operator locally `pipenv run ansible-operator run` 


### Accomplish the following tasks 
1. Currently the application is failing to deploy. Find the issue and apply the fix to `chuck-operator` (fork the repo,apply changes, build and deploy a new image, etc.)
2. Improve the `chuck-operator` to follow best cloud/k8s native patterns. Apply the fixes to `chuck-operator` at your current fork. 
 
 ### Outcomes
 1. Git repo with all the applied fixes 
 2. `chuck-operator` Docker image ready for deployment with all the fixes applied.    