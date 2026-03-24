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
# AWS EC2 Python Web Server
# AWS EC2 Python Web Server

## Project Overview

In this project, I launched an Amazon EC2 instance, connected to it through the terminal, created a simple HTML webpage, and hosted it using Python’s built-in web server.

## Terminal Setup and Commands

After connecting to my EC2 instance through the browser-based terminal, I began setting up my project environment. I first ran the command `mkdir website`, which created a new directory named `website` to keep my files organized. I then used `cd website` to navigate into that directory so that any files I created would be stored in the correct location.

Next, I ran `nano index.html`, which opened the Nano text editor and allowed me to create and edit a file named `index.html`. This file is important because it serves as the main webpage that the server will display.

The screenshot below shows the sequence of commands I executed in the terminal.

![Terminal Commands](command-list-terminal.png)
After navigating into the project directory, I created the main webpage by running the command nano index.html in the terminal. This opened the Nano text editor, where I was able to write and save the HTML code for the website.

I created this file because index.html is the default file that a web server looks for when serving a webpage. This means when the server runs, it will automatically display the contents of this file in the browser.

The screenshot below shows the HTML file being created and edited inside the Nano editor.

Running the Web Server

After creating and saving the HTML file, I returned to the terminal and ran the command sudo python3 -m http.server 80. This started a Python-based web server on port 80, which is the standard port used for HTTP traffic.

Using sudo allowed the server to bind to port 80, enabling the EC2 instance to serve the webpage to external users over the internet.

Live Website Result

Once the server was running, I accessed the EC2 instance using its Public IPv4 address in a browser. This successfully displayed my webpage, confirming that the server was live and functioning correctly.

The screenshot below shows the live web server running.
## Creating the HTML File

