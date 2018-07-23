Ansible Role: Red Hat Quay on OpenShift [![Build Status](https://travis-ci.org/siamaksade/ansible-openshift-quay.svg?branch=master)](https://travis-ci.org/siamaksade/ansible-openshift-quay)
=========

Ansible Role for deploying Red Hat Quay enterprise image registry on OpenShift. 

Role Variables
------------

| Variable                    | Default Value      | Required |  Description   |
|-----------------------------|--------------------|----------|----------------|
|`quayio_username`            | -                  | Required | Quay.io username for pulling Quay image from quay.io/coreos/quay |
|`quayio_password`            | -                  | Required | Quay.io password for pulling Quay image from quay.io/coreos/quay |
|`quayio_docker_json_path`    | -                  | Optional | Docker authentication json (instead of `quayio_username` and `quayio_password` ) for pulling Quay image from quay.io/coreos/quay |
|`quay_version`               | `v2.9.2`           | Optional | Quay image version |
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
