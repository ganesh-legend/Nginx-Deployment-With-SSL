# Nginx-Deployment-With-SSL

### Requirements:
#### - Linux machine (Ubuntu 22.04 LTS)
#### - Domain name (required to map your machine ip in domain name provider with A record)

### Stage 1: Install nginx service on your linux machine.

```bash
sudo apt install nginx
```

###

### Stage 2: Install Certbot and nginx plugin 

```bash
sudo apt install certbot
sudo apt install python3-certbot-nginx
```

### Stage 3: Edit default file of nginx

```bash
sudo vim /etc/nginx/sites-available/default
```
- In this file, you have to set **server_name** which is your domain name. e.g. example.com , if subdomain you have then you can write e.g. demo.example.com
- 
