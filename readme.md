# Create a Web Server on EC2

1. Launch an EC2 instance on AWS.
2. Connect to the instance using SSH or EC2 Instance Connect.
3. Create an `index.html` file.
4. Install and start the Apache web server:

```bash
sudo yum update -y
sudo yum install httpd -y
sudo systemctl enable --now httpd
sudo mv index.html /var/www/html/index.html
sudo systemctl restart httpd
```

5. Ensure the EC2 security group allows inbound HTTP (port 80).
6. Open the EC2 instance's Public DNS or Public IP in your browser to view the webpage.