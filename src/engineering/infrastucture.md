# Infrastructure

We use Digital Ocean and Linode for hosting our services.

Digital Ocean is used for long lived VMs and Linode is used for VMs created for the duration of the trainings.

## Domains

We use the following domains at work.

* pipal.in - the primary domain of Pipal Academy
* k8x.in - domain created for docker & k8s training

We use Digital Ocean DNS for managing the DNS records.

## Provisioning a new node

We prefer to have the identical configuration on all the nodes as much as possible to make it easier to deal to produciton issues.

We use the latest Ubuntu LTS as the operating system.

The key elements of the setup are:

- disable root login
- disable login with password (login is posisble onl with ssh-keys)
- every person working at pipal academy will have an account
- account with username `pipal` with all people have access
- standard dependencies

The configuration of the nodes is done using ansible scripts in the [cloud-setup](https://github.com/pipalacademy/cloud-setup) repository.

