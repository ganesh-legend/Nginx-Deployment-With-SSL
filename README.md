# Nginx-Deployment-With-SSL

### Requirements:
- *Linux machine (Ubuntu 22.04 LTS)*
- *Domain name (required to map your machine ip in domain name provider with A record)*

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

###

### Stage 3: Create A type record in your domain name provider.(e.g. Godaddy,Route53)
e.g. you have example.com domain. Now click on **add record** and fill the values.
- record type: A
- name: demo
- value: your_ipv4_address of machine

*It will map IP address with demo.example.com domain.*

###

### Stage 4: Edit default file of nginx and Check Configuration

```bash
sudo vim /etc/nginx/sites-available/default
```
- In this file, you have to set **server_name** which is your domain name. e.g. **example.com** , if subdomain you have then you can write e.g. **demo.example.com**
- Save the file and run next command to check configuration are correct or not.

```bash
sudo nginx -t
```

###

### Stage 5: Obtain SSL certificate

```bash
sudo certbot --nginx -d your_domain_name
```
Say Yes when it will interrupt while running command.

###

## Yeah...! You have deployed nginx with SSL.
## You are done by here. Stage 6 is optional if you want to renew certificate.

###

### Stage 6: Renew Certificate

- If you want to check certificate is about to expire then run below command.
```bash
sudo certbot renew --dry-run
```
- To renew cerficate
```bash
sudo certbot renew
```

###

### Thanks.... You are done.
### Happy Learning...😊
