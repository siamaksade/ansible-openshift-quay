Ansible Role: Red Hat Quay on OpenShift [![Build Status](https://travis-ci.org/siamaksade/ansible-openshift-quay.svg?branch=master)](https://travis-ci.org/siamaksade/ansible-openshift-quay)
=========

Ansible Role for deploying Red Hat Quay enterprise image registry on OpenShift. 

Role Variables
------------

| Variable                    | Default Value     | Required |  Description   |
|-----------------------------|--------------------|----------|----------------|
|`quayio_pull_username`       | -                  | Required | Quay image repository pull username quay.io/coreos/quay |
|`quayio_pull_password`       | -                  | Required | Quay image repository pull password quay.io/coreos/quay |
|`quay_version`               | `v2.9.2`           | Optional | Quay image version |
|`quay_service_name`          | `quay`             | Optional | Quay service name |
|`project_name`               | `che`              | Optional | OpenShift project name for the Quay container  |
|`project_display_name`       | `Eclipse Che IDE`  | Optional | OpenShift project display name for the Quay container  
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
    quayio_pull_username: user
    quayio_pull_password: password
```
