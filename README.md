# Hello Java Jenkins - Build Demo

This project demonstrates how to build a simple Java application using Maven in a Jenkins Freestyle job.]

## Prerequisites
Docker: Make sure Docker is installed and running on your machine.

## Start Jenkins (use Docker): 
```bash
docker run -p 8080:8080 jenkins/jenkins:lts
```
Access Jenkins UI at: http://localhost:8080

The initial admin password can be found using:
```bash
docker exec -it jenkins cat /var/jenkins_home/secrets/initialAdminPassword
```

## 🛠 Jenkins Build Setup

- Go to Manage Jenkins → Global Tool Configuration → Add Maven 3.8.6 (install automatically)
- Create a new Freestyle project
```bash
Source Code Management: Git
Repository URL: https://github.com/<your-username>/hello-java-jenkins.git
```
- In Build section, select: Invoke top-level Maven targets
- Build Goal: clean package
- Save & Build the job
- Check Console Output → You should see: BUILD SUCCESS

📁 Jenkins Workspace Output

After a successful build, the compiled .jar file will be located in the target/ directory.

![Image](https://github.com/user-attachments/assets/8d87159a-d9e6-447c-be32-895c2da0938e)

## 👤 Author
GitHub: rxm-gupta
