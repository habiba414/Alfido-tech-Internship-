# Task 2 – Deployment of a Web Server on AWS EC2

## Overview
This task demonstrates the deployment of an Apache2 web server on an AWS EC2 instance running Ubuntu Server 24.04 LTS. It covers provisioning a virtual machine in the cloud, connecting to it remotely via SSH, installing and configuring a web server, and verifying public access over HTTP.

## Objective
To launch a virtual server (EC2 instance) on Amazon Web Services (AWS), install and configure the Apache2 web server on it, and verify successful deployment by accessing the server's default web page through a public IP address.

## Tools & Environment
- **Cloud Provider:** Amazon Web Services (AWS) – EC2 Service
- **AMI:** Ubuntu Server 24.04 LTS
- **Instance Type:** t3.micro (Free Tier eligible)
- **Region:** US East (N. Virginia)
- **Web Server:** Apache2
- **Access Method:** SSH terminal (EC2 Instance Connect) and Web Browser

## Steps Performed
1. Accessed the AWS EC2 console
2. Reviewed EC2 resources (confirmed clean environment, zero existing resources)
3. Confirmed no existing instances
4. Launched a new instance and selected the Ubuntu Server 24.04 LTS AMI
5. Reviewed t3.micro instance type specifications and pricing
6. Configured the key pair (`MyWebServerKey`) for secure SSH access
7. Verified successful instance launch (status: Running, 3/3 checks passed)
8. Connected to the instance via SSH (public IP: `50.17.125.153`, user: `ubuntu`)
9. Updated package repositories with `sudo apt update`
10. Installed the Apache2 web server with `sudo apt install apache2 -y`
11. Verified the Apache2 service status with `sudo systemctl status apache2` (active/running)
12. Reviewed instance details (public & private IP addresses)
13. Accessed the web server via browser (initial check – tab title confirmed page loaded)
14. Verified the Apache2 default welcome page at `http://50.17.125.153`

## Result
The Apache2 web server was successfully installed, configured, and confirmed publicly accessible via the EC2 instance's public IP address, displaying the standard Apache2 Ubuntu default page.

## Deliverable
Full step-by-step report with screenshots: `Task2_AWS_EC2_WebServer_Report.docx`

## Links
- **GitHub Repository:** _add your repo link here_
- **Live Demo / Deployed Server:** `http://50.17.125.153` (Note: this was a temporary EC2 instance for the task demo — the IP may no longer be active)
- **Portfolio:** _add your Netlify portfolio link here_
- **LinkedIn:** _add your LinkedIn profile link here_

## Author
Habiba Shafait – Alfido Tech
