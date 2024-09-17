### This project is to deploy Vprofile application in docker containers on a Virtual Machine hosted on VMware fusion over Macbook M3 pro using vagrant.

Following are the steps to deploy the application:

Step 1:
Clone the repository on your local machine and change to the respective drirectory.

$  git clone https://github.com/lone-sajid/VprofileApp_docker.git

$  cd VprofileApp_docker/MacOSM1Chip/

Step 2: 
Now run the below command to build the VM on VMware fusion for which the docker which also get installed using the bootstrap provided in Vagrantfile.

$ vagrant up

Step 3:
Once the VM is up and ready login to the VM using below ssh command from the directory .../VprofileApp_docker/MacOSM1Chip/ and switch to root user;

$ vagrant up

$ sudo -i

Step 4:
Now move to /vagrant/ directory inside VM which will have "compose" directory in it. Also cd into this compose directory which will have "docker-compose.yml" file;

cd /vagrant/compose

Step 5:
Run the below command will be depoy the necessary containers on this VM.

docker compose up -d

Step 6:
Once everything is up and completed you can use "ip addr show" command to get the IP address of your VM (you can get the IP address information from Vagrantfile directly as well). 
Put the IP in the web browser to see your application being accessible.


