Ansible playbooks to provision the naps-emergency-response-project to OpenShift.

Prerequisites:
* You need to be logged in into the Openshift cluster with access to the project namespace
* `oc` client on the PATH

#### Global variables:
* namespace: defaults to `naps-emergency-response`

#### Postgresql

To provision: 
```
$ ansible-playbook playbooks/postgresql
```

To unprovision:
```
$ ansible-playbook playbooks/postgresql -e ACTION=uninstall"
```

Variables:
* postgresql user: defaults to `naps`
* postgresql password: defaults to `naps`
* postgresql database: defaults to `naps_emergency_response`

#### PgAdmin4

PgAdmin4 is a web-based administration and development tool for Postgresql.

PgAdmin4 is deployed in the `Tools` namespace.

To provision: 
```
$ ansible-playbook playbooks/pgadmin4
```

To unprovision:
```
$ ansible-playbook playbooks/pgadmin4 -e ACTION=uninstall"
```