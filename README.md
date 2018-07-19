Ansible Role: Red Hat Quay on OpenShift
=========

Ansible Role for deploying Red Hat Quay enterprise image registry on OpenShift. 

Role Variables
------------

| Variable                    | Default Value     | Required |  Description   |
|-----------------------------|--------------------|----------|----------------|
|`quay_version`               | `v2.9.2`           | Optional | Quay image version |
|`project_name`               | `che`              | Optional | OpenShift project name for the Quay container  |
|`project_display_name`       | `Eclipse Che IDE`  | Optional | OpenShift project display name for the Quay container  |
|`project_desc`               | `Eclipse Che IDE`  | Optional | OpenShift project description for the Quay container |
|`project_annotations`        | -                  | Optional | OpenShift project annotations for the Quay container |
|`project_admin`              | -                  | Optional | If set, the user to be assigned as project admin |
|`openshift_cli`              | `oc`               | Optional | OpenShift CLI command and arguments (e.g. auth) | 


Example Playbook
------------

```
name: Example Playbook
hosts: localhost
tasks:
- import_role:
    name: siamaksade.openshift_quay
  vars:
    project_name: "registry"
```
