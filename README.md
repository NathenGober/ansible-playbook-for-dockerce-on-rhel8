# Ansible Playbook for DockerCE on RHEL 8 OS
Here is an ansible playbook automating the process on removing podman and other dependecies to install Docker Community Edition on Red Hat Enterprise Linux version 8 operating system. This is to ensure support for Juniper containerized Routing Protocol Process (cRPD) on a Linux-based OS with Docker. 

Before running the playbook, we must install Ansible on the HPE ProLiant DL20 server running RHEL 8 OS, here are the steps:

# Set Up the Local Environment 
## 1. Clone the repository:

```
git clone https://github.com/NathenGober/ansible-playbook-for-dockerce-on-rhel8
cd ansible-playbook-for-dockerce-on-rhel8
```

## 2. Install Ansible:
```
sudo dnf install epel-release
sudo dnf install ansible
```

## 3. Uninstall Podman:
```
sudo dnf remove podman
```

## 4. Run the Playbook:
```
ansible-playbook install_docker.yml
```

# Explanation of Ansible Playbook
- Install yum-utils: Ensures yum-utils is installed.
- Add Docker repository: Adds the Docker repository to your system.
- Remove conflicting packages: Removes podman and buildah to avoid conflicts with Docker.
- Install Docker packages: Installs Docker CE and its dependencies.
- Enable and start Docker service: Ensures Docker starts on boot and is running.
- Check Docker version and info: Verifies the Docker installation.
- Add non-root user to Docker group: Adds the current user to the Docker group.
- Reboot the system: Reboots the system to apply group changes.
- Test Docker with hello-world image: Runs a test Docker container to verify everything is working.
