# LMS Output 2.5 Create a Server
## Description
Starting out by actually creating a server will give you insights into how servers work and help you be successful any time you’re working with a server in the future… which will be often!

This repo sets up and configires a virtual machine on the local machine, then installs an operating system on to the virtual machine. To set up this repo locally, a number of things are needed.

## Pre-requisite
  1. A laptop or computer with at least 4gb of RAM
  2. VirtualBox: Download and install virtual box from [here](https://www.virtualbox.org/wiki/Downloads).                    This is a virtual machine provider, just like VMWare and HyperV.
  3. Vagrant: Download and install Vagrant from [here](https://www.vagrantup.com/downloads.html). Vagrant                 allows us to configure our virtual machine and save those configurations in a file.

## Steps To Set up.
If all the above pre-requisites are completed, then we can get on to setting up.

1. We need to clone this repo. Run this command on your terminal:
   ``` 
   git clone https://github.com/bryan-munene/LMS-2-5-Create-a-Server.git 
   ```

2. Move inside the newly created folder by running this command on your terminal:
   ``` 
   cd LMS-2-5-Create-a-Server 
   ```

3. Now, lets start up our virtual machine. This virtual machine is configured to run on `ubuntu/bionic64` OS.
   To start our virtual machine, run this command on the terminal:
   ``` 
   vagrant up 
   ```
   This installs all the dependencies and sets up the virtual machine as per the specifications in the `Vagrantfile` in the folder.
   Once the command runs to completion, a log file of your virtual machine will be created in the same folder.

4. Your virtual machine is now configured, and it's up and running. Time to login to the newly created           virtual machine. To log in, run this command on your terminal:
   ``` 
   vagrant ssh 
   ```
   This logs you in to the virtual machine running on `ubuntu/bionic64` OS. The default root user is `vagrant`
   From here you can run any command on the ubuntu vitual machine terminal.
   
5. To access the info about this virtual machine, you need to log out. Type this on the terminal to logout:
   ``` 
   exit 
   ```
   To access the info mentioned above, type the following command in the terminal:
   ``` 
   vagrant ssh-config 
   ```
   This command should give you an output that resembles this one below:
    ``` 
    Host default
        HostName 127.0.0.1
        User vagrant
        Port 2200
        UserKnownHostsFile /dev/null
        StrictHostKeyChecking no
        PasswordAuthentication no
        IdentityFile /~relative-path-to-your-file/LMS-2-5-Create-a-Server/.vagrant/machines/default/virtualbox/private_key
        IdentitiesOnly yes
        LogLevel FATAL 
    ```

