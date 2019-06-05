# [FSND](https://www.udacity.com/course/full-stack-web-developer-nanodegree--nd004) project3 - Linux Server Configuration

This is my submission as the third project of the [Full Stack Nano Degree from Udacity](https://www.udacity.com/course/full-stack-web-developer-nanodegree--nd004).

This project is about how to take a baseline installation of a Linux server and prepare it to host web applications. how to secure the server from a number of attack vectors, install and configure a database server, and deploy an existing [web application](https://github.com/Amr-Fekry/FSND-project2-item-catalog) onto it.

### Server Information:
- IP Address: 52.57.126.228
- SSH Port: 2200
- Domain Name: http://52-57-126-228.nip.io

### Server Access:
- download the `grader_key` file (preferably into `~/.ssh/` directory)
- `ssh grader@52.57.126.228 -p 2200 -i ~/.ssh/grader_key`

### Server Configuration and Software:
1. Start a new Ubuntu Linux server instance on [Amazon Lightsail](https://lightsail.aws.amazon.com).
2. Login into instance using a provided SSH key for a default user `ubuntu`.   
**------- _User Management_**  
3. Remote login as `root` user is disabled by default on instance.
4. Create a new user `grader` and give him `sudo` access.
5. Create an SSH key pair for `grader` using the `ssh-keygen` tool.   
**------- _Security_**  
6. Update Package-Source-List and all currently installed packages.
7. Change SSH hosting port from the default 22 into 2200.
8. Configure firewall to only allow connections for (SSH, HTTP, NTP) on ports (2200, 80, 123) respectively.
9. Force Key-based SSH authentication.   
**------- _Prepare for deployment_**
10. Configure the local timezone to UTC.
11. Install `Apache` web server.
12. Install `mod_wsgi` python application handler. 
13. Install `PostgreSQL` database server.
14. Install `Git` version control system.

### Deployment:
- Clone [Item Catalog](https://github.com/Amr-Fekry/FSND-project2-item-catalog) project.
- Construct the file structure for the app to work with Apache.
- Configure Python version and install application requirements.
- Configure WSGI files.
- Configure, setup and connect database.
- Update OAuth settings to use the domain name.
- Restart Apache service and use Apache logs for debugging.

### Resources:
- This project is mainly based on the [Configuring Linux Web Servers](https://www.udacity.com/course/configuring-linux-web-servers--ud299) course.
- For the deployment part, some external links were used: see [this](http://leonwang.me/post/deploy-flask) and [this](https://www.digitalocean.com/community/tutorials/how-to-deploy-a-flask-application-on-an-ubuntu-vps) and [this](https://www.digitalocean.com/community/tutorials/how-to-install-and-use-postgresql-on-ubuntu-16-04) and [this](https://wixelhq.com/blog/how-to-install-postgresql-on-ubuntu-remote-access). 
