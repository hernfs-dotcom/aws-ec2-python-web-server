# aws-ec2-python-web-server
## EC2 Instance Running

I launched an EC2 instance using Amazon Linux and verified that it is in a running state.

![EC2 Running](ec2-server-running.png)
## Initial Security Configuration

Initially, the security group only allowed SSH (port 22) access, which is used to connect to the EC2 instance.

![Initial Security Group](inbound-rules.png)

## Identifying Missing HTTP Access

I noticed that HTTP (port 80) was not enabled, which would prevent external users from accessing the web server through a browser.

To resolve this, I added an inbound rule to allow HTTP traffic on port 80.
## Updated Security Configuration

After adding the HTTP rule on port 80, the EC2 instance was able to receive web traffic from the internet.

![Updated Security Group](inbound-rules-http.png)
