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
- Nginx Active Status
- Website Live on Browser

---

## 👨‍💻 Author

**Mubashar Akram**  
Internee @ Internee.pk  
GitHub: [@MubasharAkram05](https://github.com/MubasharAkram05)
