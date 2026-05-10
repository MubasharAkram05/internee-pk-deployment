# 🚀 Internee.pk Cloud Deployment

## 📌 Project Overview
Static clone of Internee.pk deployed on AWS EC2 cloud infrastructure
as part of Internee.pk internship task.

> **Source:** Cloned from https://www.internee.pk  
> **Saved via:** SingleFile Browser Extension  
> **Deployed on:** AWS EC2 (Ubuntu 22.04 + Nginx)

---

## 🛠️ Tech Stack

| Technology | Purpose |
|---|---|
| AWS EC2 (t2.micro) | Virtual Machine / Cloud Server |
| Ubuntu 22.04 LTS | Operating System |
| Nginx | Web Server |
| Git | Version Control |
| SingleFile | Website Cloning Tool |

---

## ⚙️ Auto Deployment Script

Used this script in EC2 User Data for automatic setup:

```bash
#!/bin/bash
apt update && apt upgrade -y
apt install nginx git -y
systemctl start nginx
systemctl enable nginx
mkdir -p /var/www/html/internee
git clone https://github.com/MubasharAkram05/internee-pk-deployment.git /var/www/html/internee
chown -R www-data:www-data /var/www/html/internee
chmod -R 755 /var/www/html/internee
echo "Setup Complete! $(date)" >> /var/log/internee-setup.log
```

---

## 🚀 Deployment Steps

1. ✅ Launched AWS EC2 instance (Ubuntu 22.04, t2.micro Free Tier)
2. ✅ Configured Security Group (Port 22, 80 open)
3. ✅ Auto installed Nginx + Git via User Data script
4. ✅ Pulled website files automatically from GitHub
5. ✅ Website live on `http://EC2_PUBLIC_IP`
6.  ✅ Free domain configured (internee-mubashar.ddns.net)
7. ✅ HTTPS enabled using Let's Encrypt SSL
8. ✅ HTTP to HTTPS auto redirect enabled

## 🔗 Live URL
https://internee-mubashar.ddns.net

---

## 📸 Screenshots

- EC2 Instance Running
- <img width="1880" height="461" alt="dshb inst" src="https://github.com/user-attachments/assets/275f5197-ca35-4c9c-8d8c-bdfcec3b7793" />
<img width="1920" height="934" alt="instance running dashboard" src="https://github.com/user-attachments/assets/ba1ef3f9-b080-473a-8b7a-8ba127eef4b9" />
- <img width="1886" height="900" alt="1st intance" src="https://github.com/user-attachments/assets/f13cd703-8b81-4cfa-9731-8d95749fa397" />

- Nginx Active Status
<img width="797" height="663" alt="bash-setup3" src="https://github.com/user-attachments/assets/4b1f1d9b-c8d7-478f-83a3-97db9e91baf7" />
<img width="988" height="1037" alt="bash-setup2" src="https://github.com/user-attachments/assets/bf878d9c-33c5-4526-9fac-814cd06b2682" />
<img width="1226" height="1027" alt="bashsetub1" src="https://github.com/user-attachments/assets/31db5f77-780e-44d8-bedf-e04b828ba958" />

- 
- Website Live on Browser

---<img width="1920" height="1080" alt="ssllive" src="https://github.com/user-attachments/assets/88a2d0da-76dc-498a-a8ed-894ce122f148" />
<img width="1920" height="1080" alt="live" src="https://github.com/user-attachments/assets/d824a0a2-aa06-4eed-bcda-8c2f6e87b8a6" />

Domain 
<img width="1557" height="651" alt="domain" src="https://github.com/user-attachments/assets/ea381424-b071-488a-af95-c3b449085f6c" />

Security Group
<img width="1267" height="610" alt="security" src="https://github.com/user-attachments/assets/33d52aee-645e-4b15-af3c-5e004fd21577" />

Instance connect
<img width="1887" height="895" alt="ubunto-interface2" src="https://github.com/user-attachments/assets/49602cab-4659-4c7e-aba8-f6de8c1a00a9" />
<img width="1920" height="955" alt="ubunto interface" src="https://github.com/user-attachments/assets/b3fea3d1-bb8d-4bfa-9cf2-8db6ba8a0da5" />

Instance Acess using putty 
<img width="1112" height="692" alt="access using putty" src="https://github.com/user-attachments/assets/3902c9b6-6ff7-4f01-9af7-996982b83b40" />




## 👨‍💻 Author

**Mubashar Akram**  
Internee @ Internee.pk  
GitHub: [@MubasharAkram05](https://github.com/MubasharAkram05)
