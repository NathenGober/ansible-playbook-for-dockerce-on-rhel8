# Ansible Playbook for DockerCE on RHEL 8 OS
Here is an ansible playbook automating the process on removing podman and other dependecies to install Docker Community Edition on Red Hat Enterprise Linux version 8 operating system. This is to ensure support for Juniper containerized Routing Protocol Process (cRPD) on a Linux-based OS with Docker. 

HOWEVER, before running the playbook, we must install Ansible on the HPE ProLiant DL20 server running RHEL 8 OS, here are the steps:

## 1. Update the System:
```
$ sudo dnf update
$ sudo dnf install -y yum-utils
```
# Running the Docker Playbook to install Docker on RHEL 8 OS

## 1. Clone the repository:

```
git clone https://github.com/NathenGober/Ansible-Playbook-for-DockerCE-on-RHEL8
```

## 2. Run the playbook:
```
ansible-playbook -i your_inventory_file docker_playbook.yml
```
