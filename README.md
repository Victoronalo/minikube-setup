# minikube-setup
Project: Minikube Installation



Objective: To install Minikube on our local machine.



-I started by creating an instance named kubernete-instance.



-I used an available keypair.



-I connected to the instance using EC2 instant connect.



-I ran the command,  sudo apt-get update to refresh package list.



-Also ran sudo apt-get install ca-certificates curl gnupg to install essential packages.


-I ran the command sudo install -m 0755 -d /etc/apt/keyrings to create directory and store ring files.




-I ran this command to download docker GPG key using curl
      * curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /etc/apt/keyrings/docker.gpg.





-I ran the below code to set read permission for all users on the Docker GPG file.
      * sudo chmod a+r /etc/apt/keyrings/docker.gpg




-The below command creates a Docker apt repository configuration entry
      * echo \
  "deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/docker.gpg] https://download.docker.com/linux/ubuntu \
  $(. /etc/os-release && echo "$VERSION_CODENAME") stable" | \
  sudo tee /etc/apt/sources.list.d/docker.list > /dev/null




-To install latest update, I ran sudo apt-get update



-To verify docker has successfully been installed, I ran the command
              *sudo apt-get install docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin




-To install minikube, I ran the below command
        * curl -LO https://storage.googleapis.com/minikube/releases/latest/minikube_latest_amd64.deb



-The command was successful.



-To download minikube binary, I ran the command below.
     * sudo dpkg -i minikube_latest_amd64.deb



-I ran the command “minikube start --driver=docker”



-To download kubernete command I ran the below command.
       * sudo snap install kubectl –classic




The process was successful and the installation was done.

-

