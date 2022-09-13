Install Jenkins

https://www.jenkins.io/doc/tutorials/tutorial-for-installing-jenkins-on-AWS/


1- Create Instance AWS and install Jenkins

[ec2-user ~]$ sudo yum update –y
[ec2-user ~]$ sudo wget -O /etc/yum.repos.d/jenkins.repo \
    https://pkg.jenkins.io/redhat-stable/jenkins.repo
[ec2-user ~]$ sudo rpm --import https://pkg.jenkins.io/redhat-stable/jenkins.io.key
[ec2-user ~]$ sudo yum upgrade
[ec2-user ~]$ sudo amazon-linux-extras install java-openjdk11 -y
[ec2-user ~]$ sudo yum install jenkins -y
[ec2-user ~]$ sudo systemctl enable jenkins
[ec2-user ~]$ sudo systemctl start jenkins
[ec2-user ~]$ sudo systemctl status jenkins
sudo amazon-linux-extras install epel -y
sudo yum update -y
sudo yum install jenkins java-1.8.0-openjdk-devel

Errors:https://stackoverflow.com/questions/68806741/how-to-fix-yum-update-of-jenkins

2- Connect to Jenkins
http://<IP>/8080

Get password:
[ec2-user ~]$ sudo cat /var/lib/jenkins/secrets/initialAdminPassword

3-Under Global credentials configure credentials for 
DockerHub and GitHub (Token)