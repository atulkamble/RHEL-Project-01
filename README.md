# RHEL-Project-01
Basic RHEL Project

This project focusing on setting up a simple web server using Apache on Red Hat Enterprise Linux (RHEL). This project will guide you through installing Apache, configuring a basic website, and testing its functionality.

### Clone Project to Your Machine 
```
```

### Project: Setting up a Basic Web Server with Apache on RHEL

#### Step 1: Create EC2 Instance | RHEL | SSH 

#### Step 2: Install Apache

First, you need to install the Apache HTTP server on your RHEL system.

```bash
sudo -i passwd
sudo yum update -y
sudo yum install httpd -y
```

#### Step 2: Start Apache and Enable it on Boot

Once Apache is installed, start the service and enable it to start automatically on system boot.

```bash
sudo systemctl start httpd
sudo systemctl enable httpd
sudo usermod -a -G apache ec2-user
```

#### Step 3: Configure Security Group of Instance

Add Inbound Traffic Rule HTTP (80), HTTPS(443), SSH(22)

#### Step 4: Create a Sample HTML Page

Create a simple HTML page to serve as your website's content. For example, create a file named `index.html` in the Apache document root directory (`/var/www/html/`).

```bash
cd /var/www/html
sudo touch index.html
sudo nano /var/www/html/index.html
```

Add the following content to `index.html`:

```html
<!DOCTYPE html>
<html>
<head>
    <title>Welcome to My Website</title>
</head>
<body>
    <h1>Welcome to My Website</h1>
    <p>This is a basic webpage served by Apache on Red Hat Enterprise Linux.</p>
</body>
</html>
```

#### Step 5: Test Apache Server

Open a web browser and navigate to  `http://instance_public_ip`. You should see the content of `index.html` displayed.


### Summary

This project provides a foundational understanding of setting up a basic web server using Apache on Red Hat Enterprise Linux. It covers installation, configuration, and testing steps necessary to serve a simple webpage. Depending on your familiarity with Linux and Apache, you can expand this project with more advanced configurations and features.
