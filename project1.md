# Project1 - Web stack implementation
-*Installing windows terminal*
-*Creating EC2 instance along with the security group in the AWS cloud*
-*Generate SSH keys in AWS for the EC2 instance , ssh into EC2 from the windows terminal*

*Install Apache2*
`sudo apt update`
`sudo apt install apache2`

![Installation of apache](./images/P1-1.jpg)
![Running](./images/P1-2.jpg)
*Verify running of apache2*
`curl http://localhost:80`
`curl -s http://169.254.169.254/latest/meta-data/public-ipv4`

![Verify in web](./images/P1-S3.jpg)
![Verify in web1](./images/P1-S4.jpg)

*My sql installation and verify*
`sudo apt install mysql-server`
`sudo mysql`

![mysql](./images/P1-S5.jpg)
![mysql](./images/P1-S6.jpg)

*Install php*
`sudo apt install php libapache2-mod-php php-mysql`
`php -v`

![php](./images/P1-S7.jpg)

*VIRTUAL HOST FOR YOUR WEBSITE*

`sudo mkdir /var/www/projectlamp`
`sudo chown -R $USER:$USER /var/www/projectlamp`
`sudo vi /etc/apache2/sites-available/projectlamp.conf`
`sudo a2ensite projectlamp`

![website](./images/P1-S8.jpg)

`sudo echo 'Hello LAMP from hostname' $(curl -s http://169.254.169.254/latest/meta-data/public-hostname) 'with public IP' $(curl -s http://169.254.169.254/latest/meta-data/public-ipv4) > /var/www/projectlamp/index.html`

![virtualhost](./images/P1-S9.jpg)

*enable php*

`vim /var/www/projectlamp/index.php`

![php](./images/P1-S10.jpg)
![php](./images/P1-S11.jpg)
