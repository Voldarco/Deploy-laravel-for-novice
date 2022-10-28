## **ALTSCHOOL AFRICA**

### **Mini Project (Exercise 11)**

### Prerequisites
- basic knowledge of the linux file system | ownership | permissions 🐧

- basic knowledge of git 🚦

- stable internet connection (very important)☁️

-  How to use linux editor `vim` or at least `nano` 📝

### Overview

- Setup Debain 11 on a virtual machine instance with a cloud provider or as instructed

- Setup Apache2 with every dependency the application needs to run

- Don't use Laravel Sail or Docker as suggested in the project README.md file, simply clone the project with Git and deploy with apache2

- Setup MySQL with credentials and a database for your application to use

- Configure a subdomain if you have a domain name to point to the Vm instance or speak to an instructor for futher guide

- You have complete the project if you are able to view the application according to the specifications in the project from your Host browser

![laravel](https://user-images.githubusercontent.com/69207791/198589053-388f85f0-9ab4-4201-b561-7923f97d2f09.png)

## **Getting Started**

## **Step One:**

We will be using Debain 11 on a virtual machine instance with Amazon Web Services (AWS) as our VPC provider.

**NOTE:**   this should take 6min. 

- Create a new key pair if you don't have one or select an existing one. Just note where the new key pair 
is downloaded.

![Screenshot (9)](https://user-images.githubusercontent.com/69207791/198605842-1b047bfd-087e-4f8e-9aa7-2a59c98f4791.png)

Next set your security to allow port **22** for SSH and 0 - 65535 for All TCP

![Screenshot (10)](https://user-images.githubusercontent.com/69207791/198609826-abbb3ddf-9109-41db-ab9c-909d6afcc717.png)

Once you have this set you can launch the instance. click on connect instance and copy the "Example ssh"

Open your terminal and **cd into** where you have the downloaded key pair. Paste the **"ssh"** (for me it is download)and Enter. You will be logged in.

![Screenshot (11)](https://user-images.githubusercontent.com/69207791/198623362-b2d38f3a-5f78-44d3-a813-f96dc563fbc5.png)

## **Step Two:** 

Update the Package Installer

I switch to `root user` because most installation will require root access; You can run all command below as normal user using ``**sudo**``.
<br> We will be updating the apt repository before installing any package

```php
sudo su
```

```php
 apt update && apt upgrade -y
```

**When prompted, select keep the local version currently installed and Hit the Enter Key**

Now that our installer is up to date, we can now install our web server Apache and the following packages on the server

## **Step Three:**

Installing Dependencies

I install the following packages at once (Apache2, Wget, Git, Curl)

```php
apt install -y wget git apache2 curl
```
**Note:* You might like to take each at a step so here is a great link for that: <br>
https://github.com/michaelagbiaowei/altschool-cloud-exercises/tree/main/Semester-Project

## **Step Four:**

 Install PHP

 Add the SURY PPA for PHP 8.1

```php
apt -y install lsb-release apt-transport-https ca-certificates
```
```php
wget -O /etc/apt/trusted.gpg.d/php.gpg https://packages.sury.org/php/apt.gpg
```

Add the PPA to the server packages using the following command

```php
echo "deb https://packages.sury.org/php/ $(lsb_release -sc) main" | sudo tee /etc/apt/sources.list.d/php.list
```

Update the packages and install PHP 8.1

```php
apt update
```
```php
apt install php libapache2-mod-php php8.1-mysql php8.1-common php8.1-mysql php8.1-xml php8.1-xmlrpc php8.1-curl php8.1-gd php8.1-imagick php8.1-cli php8.1-dev php8.1-imap php8.1-mbstring php8.1-opcache php8.1-soap php8.1-zip php8.1-intl -y
```

Once PHP is installed you can check the version using the following command.

```php
php -v
```






