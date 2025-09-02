# Jenkins-Zero-to-Hero
This Repo is all about CI/CD using Jenkins and Argo CD


'''
# 🚀 Jenkins Installation Guide (on Debian/Ubuntu)

This guide provides step-by-step instructions to install **Jenkins** on a **Debian-based system** (e.g., Ubuntu) using the official Jenkins repository and Java 17 (required by recent Jenkins versions).

## 📦 Prerequisites

- A Debian/Ubuntu-based Linux system
- `sudo` privileges


##  Steps to Install Jenkins

### 1. ✅ Update Package Index

    sudo apt update

### 2. ☕ Install Java 17 (OpenJDK)

Jenkins requires Java to run. Install OpenJDK 17:

    sudo apt install openjdk-17-jre
    
Verify jenkins version

    java -version

### 3. Jenkins installation


curl -fsSL https://pkg.jenkins.io/debian/jenkins.io-2023.key | sudo tee \
  /usr/share/keyrings/jenkins-keyring.asc > /dev/null

echo deb [signed-by=/usr/share/keyrings/jenkins-keyring.asc] \
  https://pkg.jenkins.io/debian binary/ | sudo tee \
  /etc/apt/sources.list.d/jenkins.list > /dev/null

sudo apt-get update
sudo apt-get install jenkins


### Note: If you are using any cloud platform please enable traffic for your instance

##  Start and Enable Jenkins Service

To ensure Jenkins starts automatically on boot and is running now:

    sudo systemctl enable jenkins
    sudo systemctl start jenkins

##  Access Jenkins Web Interface

After installation, Jenkins runs on **port `8080`** by default.

Open your browser and navigate to:

    http://localhost:8080

Or, if accessing remotely:

    http://<your-server-ip>:8080

## 🔐 Initial Admin Password

To unlock Jenkins for the first time, retrieve the admin password:

    sudo cat /var/lib/jenkins/secrets/initialAdminPassword

Copy this password and paste it into the Jenkins setup wizard.



## 📚 Resources

- [Official Jenkins Installation Guide](https://www.jenkins.io/doc/book/installing/)
- [OpenJDK Downloads](https://openjdk.org/)
'''
