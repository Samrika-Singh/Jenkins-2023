# Jenkins-2023
For Full understanding of CI and CD

# Jenkins installation on AMI 2
1. sudo wget -O /etc/yum.repos.d/jenkins.repo https://pkg.jenkins.io/redhat-stable/jenkins.repo
2. sudo rpm --import https://pkg.jenkins.io/redhat-stable/jenkins.io-2023.key
3. sudo amazon-linux-extras install epel
4. sudo amazon-linux-extras install java-openjdk11
5. check java install
  java --version
6. sudo yum install jenkins

# Finally for UI 

just on browser 
Public_IPADDRESS_EC2:8080 (check at sg(security_group) level in aws for instance 8080 enabled)
password :: find at /var/lib/jenkins/secrets/initialAdminPassword
Username:: admin
