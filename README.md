# jenkinsinstallation

BUILDING jenkins server = https://www.youtube.com/watch?v=at6r2SqNYR8  ;; 
========================= https://pkg.jenkins.io/redhat-stable/


instance - t2.micro
ami: ami-025b4b7b37b743227  || amazon linux 2 ami (hvm) - kernel 5.10 ssd volume type



1) yum install java*c

2) yum install java* -y


sudo wget -O /etc/yum.repos.d/jenkins.repo https://pkg.jenkins.io/redhat-stable/jenkins.repo
  
sudo rpm --import https://pkg.jenkins.io/redhat-stable/jenkins.io-2023.key

yum install jenkins

systemctl enable jenkins

systemctl start jenkins

---------------------------


Docker 
=====================


sudo yum update

sudo yum search docker


sudo yum install docker

sudo usermod -a -G docker ec2-user

id ec2-user

sudo systemctl enable docker.service

sudo systemctl start docker.service

sudo systemctl status docker.service



Docker-compose 
=================

sudo pip3 install docker-compose

or manually


wget https://github.com/docker/compose/releases/latest/download/docker-compose-$(uname -s)-$(uname -m) 


sudo mv docker-compose-$(uname -s)-$(uname -m) /usr/local/bin/docker-compose

sudo chmod -v +x /usr/local/bin/docker-compose

 sudo cp  /usr/local/bin/docker-compose /usr/bin


docker-compose version




