# DOCKER

## Question 1: What is Docker?
Docker is a containerization platform that provides an easy way to containerize your applications. Using Docker, you can build container images, run the images to create containers, and push these containers to container registries such as DockerHub.

## Question 2: What are Containers?
A container is a bundle of an application, the application libraries required to run your application, and the minimum system dependencies.

## Question 3: What is host Operating System and Guest Operating System?
The host operating system (OS) is software installed on a computer that communicates with the computer's hardware. The guest OS is software installed in a virtual machine (VM) that runs on the host OS. The host OS executes directly on the hardware, while the guest OS executes on the VM. It's important to note that while a container uses resources from the host operating system, it is still isolated from the host and other containers, so changes to the container do not affect the host or other containers.

## Question 4: Difference between Containers and Virtual Machines
Containers and virtual machines are both technologies used to isolate applications and their dependencies, but they have some key differences:

1. **Resource Utilization**: Containers share the host operating system kernel, making them lighter and faster than VMs. VMs have a full-fledged OS and hypervisor, making them more resource-intensive.
2. **Portability**: Containers are designed to be portable and can run on any system with a compatible host operating system. VMs are less portable as they need a compatible hypervisor to run.
3. **Security**: VMs provide a higher level of security as each VM has its own operating system and can be isolated from the host and other VMs. Containers provide less isolation, as they share the host operating system.
4. **Management**: Managing containers is typically easier than managing VMs, as containers are designed to be lightweight and fast-moving.

## Question 5: What files and folders are present in a container's base image?
Files and folders present in a container's base image include:
- `/bin`: contains binary executable files, such as the `ls`, `cp`, and `ps` commands.
- `/sbin`: contains system binary executable files, such as the `init` and `shutdown` commands.
- `/etc`: contains configuration files for various system services.
- `/lib`: contains library files that are used by the binary executables.
- `/usr`: contains user-related files and utilities, such as applications, libraries, and documentation.
- `/var`: contains variable data, such as log files, spool files, and temporary files.
- `/root`: is the home directory of the root user.

## Question 6: How to install Docker in Ubuntu?

1. Add Docker's official GPG key:
#Update your machine
```
sudo apt-get update
```
#to install a root CA certificate in the trust store
```
sudo apt-get install ca-certificates curl
 ```
#Creating directory with appropriate permissions, using super-user privileges.
```
sudo install -m 0755 -d /etc/apt/keyrings
```
#Download the file from docker.com to docker.asc file in keyrings folder
```
sudo curl -fsSL https://download.docker.com/linux/ubuntu/gpg -o /etc/apt/keyrings/docker.asc
```
#Add Read Permission for all user to docker.asc
```
sudo chmod a+r /etc/apt/keyrings/docker.asc
```
2. Add the repository to Apt sources:
```
echo \
  "deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/docker.asc] https://download.docker.com/linux/ubuntu \
  $(. /etc/os-release && echo "$VERSION_CODENAME") stable" | \
  sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
```
#Update your machine
```
sudo apt-get update
```
