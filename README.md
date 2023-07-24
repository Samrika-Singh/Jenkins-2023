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
*Password* :: find at /var/lib/jenkins/secrets/initialAdminPassword
*Username*  :: admin


# Git + MVN + Jenkins Integration

## Git
---------------------------------
Git on jenkins server(our pc) need to be installed and even the *Plugin* need to installed and configured on Jenkins UI.
On Local pc the github source code is pull from github to local jenkins server under /var/lib/jenkins/workspace/{Repository_name}.
On Jenkins UI wher we define repo link during configration of repository need Plugin.

## Maven and JDK
-------------------------------------
Maven is building tool therefore need to install on Jenkins server(local pc where jenkins installed)
For installation:
cd /opt
wget https://dlcdn.apache.org/maven/maven-3/3.9.3/binaries/apache-maven-3.9.3-bin.tar.gz
mv apache-maven-3.9.3 maven

cd ~
vi .bash_profile
M2_HOME=/opt/maven
M2=/opt/maven/bin
JAVA_HOME=/usr/lib/jvm/java-11-openjdk-11.0.19.0.7-1.amzn2.0.1.x86_64

NOTE: This *JAVA_HOME* and *M2_HOME* need to pass in Jenkins UI also 

## Pictorial View GITHUB + JENKINS + MVN INTEGRATION
<img width="576" alt="Jenkins_mvn_integration" src="https://github.com/Samrika-Singh/Jenkins-2023/assets/67017620/2942c83f-855d-47bd-92aa-2590a54ab4d1">






