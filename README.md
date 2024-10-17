# Multipass-Documentation
**This documentation explains the various commands use to run virtual machines in multipass:**

**multipass launch docker --name docker-vm:**
 This command launches a new VM instance with Docker pre-installed. The VM is created with a default name called docker-vm

**multipass list:**
 This command lists all the running and suspended virtual machines, along with their status, IP address, number of CPUs, memory usage, and disk allocation.

**multipass shell docker-vm:**
 Connects to the VM’s shell, allowing you to execute commands within the VM.

**multipass start docker-vm:**
 If a VM is stopped and you want to restart it

**multipass stop docker-vm:**
 This will suspend the VM until it is restarted.

**multipass delete docker-vm:**
 If you no longer need the VM, you can delete it using the ABOVE command

**multipass purge:**
 To free the disk space used by the deleted VM

**multipass exec docker-vm -- docker run:**
 The above command helps to execute commands without having to enter its shell

**multipass alias docker = "multipass exec docker-vm --docker":**
 This command sets up an alias so you can run Docker commands directly on your host without having to SSH into the VM or prefix your commands with multipass exec. The alias maps docker = "multipass exec docker-vm --docker"to the local docker command.

**docker ps:**
 This will work as if Docker is installed on your local machine, but it will actually be running inside the docker-vm.
