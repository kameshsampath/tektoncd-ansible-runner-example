# Tektoncd Ansible Runner Examples

A repo to hold Ansible runner examples for the Tektoncd Task `ansible-runner`

## Examples


### Listing pods

```shell
 tkn task start ansible-runner \
   --serviceaccount ansible-deployer-account \
   --param=args='-p list-pods.yml' \
   --workspace=name=project-directory,config=ansible-playbooks \
   --showlog
```

### Create Deployment

```shell
 tkn task start ansible-kubernetes \
   --serviceaccount ansible-deployer-account \
   --param=args=create-deployment.yml \
   --workspace=name=playbook-directory,config=ansible-playbooks \
   --showlog
```

### Create Service

```shell
 tkn task start ansible-kubernetes \
   --serviceaccount ansible-deployer-account \
   --param=args=create-service.yml \
   --workspace=name=playbook-directory,config=ansible-playbooks \
   --showlog
```
