Update package lists and system:

sudo apt update && sudo apt upgrade -y   # For Ubuntu/Debian
sudo dnf update -y                      # For CentOS/Rockysudo apt install curl wget unzip vim ufw net-tools -y


Set hostname and timezone:

hostnamectl set-hostname lamp-server
timedatectl set-timezone Asia/Kolkata


Install basic tools:

sudo apt install curl wget unzip vim ufw net-tools -y

Install and Configure Apache:

sudo apt install apache2 -y   # Or: sudo dnf install httpd -y
sudo systemctl enable apache2
sudo systemctl start apache2

Verify local host:
curl http://localhost

Install and Secure MySQL:

sudo apt install mysql-server -y
sudo mysql_secure_installation

Set Up User & Database:

CREATE DATABASE app_db;
CREATE USER 'app_user'@'localhost' IDENTIFIED BY 'StrongPass@123';
GRANT ALL PRIVILEGES ON app_db.* TO 'app_user'@'localhost';
FLUSH PRIVILEGES;


Install PHP:

sudo apt install php libapache2-mod-php php-mysql php-cli php-curl php-gd php-mbstring php-xml php-zip -y

Test PHP:
Create a file at /var/www/html/info.php:
#And inside that script write it
<?php phpinfo(); ?>




























