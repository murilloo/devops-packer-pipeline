# devops-vagrant-pipeline
Example pipeline using Vagrant for provisioning a VM and to install Docker and Packer on the host. After, it uses Packer to create a Docker image based on a Packer template (no Dockerfiles) and Ansible to customize the image.

## Requirements
- Vangrant >= 2.2.5
- Libvirt >= 5.1.0

## Goals
- Create a Docker image using Packer *without* Dockerfile
- Run customization on the image using Ansible

## Running
```
$ vagrant up --provider=libvirt
$ vagrant ssh centos (to connect to the VM provisioned)
$ sudo su - packer
$ packer build container.json
```
