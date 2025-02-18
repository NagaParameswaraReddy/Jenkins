# 🚀 Installing Jenkins on AWS EC2 Instance: A Step-by-Step Guide  

## 📌 Prerequisites  
Before starting, ensure you have:  
✔️ An **AWS EC2 instance** (Amazon Linux 2023)  
✔️ An **SSH key pair** to connect to your instance  
✔️ Security group configured to allow **port 8080** (for Jenkins UI access)  

---

## ⚡ 1. Launch an EC2 Instance & Set Up Security Group  
- Launch an EC2 instance with **Amazon Linux 2023**.  
- Configure the **security group** to allow inbound traffic on **port 8080** (Jenkins UI).  

```sh
# Allow HTTP access on port 8080 (for Jenkins)
Inbound Rule: TCP | Port 8080 | Source: 0.0.0.0/0 (or restrict as needed)
```

---

## 🖥️ 2. Connect to Your EC2 Instance  
After launching your EC2 instance, **connect via SSH** using:  

```sh
ssh -i your-key-pair.pem ec2-user@your-ec2-public-ip
```

---

## ⚙️ 3. Install Jenkins  

### **Step 1: Update Software Packages**  
```sh
sudo yum update -y
```

### **Step 2: Add the Jenkins Repository**  
```sh
sudo wget -O /etc/yum.repos.d/jenkins.repo https://pkg.jenkins.io/redhat-stable/jenkins.repo
```

### **Step 3: Import the Jenkins Key**  
```sh
sudo rpm --import https://pkg.jenkins.io/redhat-stable/jenkins.io-2023.key
```

### **Step 4: Upgrade Packages (Optional)**  
```sh
sudo yum upgrade -y
```

### **Step 5: Install Java (Required for Jenkins)**  
Amazon Linux 2023 supports Amazon Corretto 17 (LTS):  
```sh
sudo dnf install java-17-amazon-corretto -y
```

### **Step 6: Install Jenkins**  
```sh
sudo yum install jenkins -y
```

---

## 🔧 4. Configure Jenkins  

### **Step 1: Enable Jenkins to Start on Boot**  
```sh
sudo systemctl enable jenkins
```

### **Step 2: Start Jenkins Service**  
```sh
sudo systemctl start jenkins
```

### **Step 3: Check Jenkins Status**  
```sh
sudo systemctl status jenkins
```

If Jenkins is running correctly, you should see **"Active (running)"**.

---

## 🌐 5. Access Jenkins Web Interface  

After starting Jenkins, open your browser and navigate to:  
```sh
http://<your-ec2-public-ip>:8080
```
🔹 **Replace `<your-ec2-public-ip>`** with your actual EC2 instance's public IP.

---

## 🔑 6. Unlock Jenkins  
Jenkins will prompt for an **initial admin password**. Retrieve it using:  
```sh
sudo cat /var/lib/jenkins/secrets/initialAdminPassword
```
Copy & paste this password into the Jenkins UI to **unlock** it.

---

## 🚀 7. Complete Jenkins Setup  
Once unlocked, follow the **Jenkins setup wizard**:  
✔️ Install **suggested plugins** (recommended).  
✔️ Create an **admin user** (or use the default `admin`).  

---

## 🎯 8. Final Notes & Conclusion  
🎉 **Congratulations!** Jenkins is now successfully installed. You can start:  
✅ **Creating Jenkins jobs & pipelines**  
✅ **Automating deployments using CI/CD**  
✅ **Exploring advanced Jenkins plugins & configurations**  

---

### 🔗 **Additional Resources**  
📚 **Official Jenkins Documentation:** [Jenkins.io](https://www.jenkins.io/)  
📌 **AWS EC2 Guide:** [AWS Docs](https://docs.aws.amazon.com/)  

---

### 💡 **"The best way to predict the future is to automate it!"**
