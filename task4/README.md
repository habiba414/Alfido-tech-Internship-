# Alfido Tech Internship – Task Report
## Deploying a Docker Container on a Cloud Virtual Machine (AWS EC2)

**Intern:** Habiba Shafait
**Internship:** Alfido Technologies
**Cloud Platform:** Amazon Web Services (AWS) – EC2
**Operating System:** Ubuntu (EC2 instance)
**Tool Used:** Docker

---

## Objective

The objective of this task was to gain hands-on experience with cloud computing and containerization by launching a virtual machine (VM) on AWS, installing Docker on it, and deploying a live web server inside a Docker container. The task demonstrates the complete workflow of provisioning cloud infrastructure, configuring a Linux environment, and running a containerized application accessible over the public internet.

## Tools & Technologies Used

- Amazon Web Services (AWS) – EC2 (Elastic Compute Cloud)
- Ubuntu Server (Linux operating system running on the cloud VM)
- EC2 Instance Connect (browser-based SSH terminal)
- Docker Engine (`docker.io` package)
- Nginx (official Docker image used as the sample web server)
- Linux shell commands (`apt`, `systemctl`, `docker` CLI)

---

## Step-by-Step Procedure

### Step 1 — Launch an EC2 Virtual Machine on AWS

An Ubuntu-based EC2 instance named **"MyWebServer"** was launched from the AWS Management Console using a `t3.micro` instance type. The AWS EC2 dashboard confirms the instance is in the **"Running"** state with its status checks initializing.

---

### Step 2 — Connect to the VM and Update the System

The instance was accessed through **EC2 Instance Connect**, a secure browser-based SSH terminal (logged in as the default `ubuntu` user). The package index was refreshed first:

```bash
sudo apt update -y
```

---

### Step 3 — Install Docker on the VM

Docker was installed using the official Ubuntu package:

```bash
sudo apt install docker.io -y
```

---

### Step 4 — Start, Enable, and Verify Docker

The Docker service was started and enabled to run automatically on every boot, then verified:

```bash
sudo systemctl start docker
sudo systemctl enable docker
docker --version
```

---

### Step 5 — Run a Docker Container (Nginx Web Server)

A container running the official `nginx` image was launched, mapping port 80 of the container to port 80 of the host VM:

```bash
sudo docker rm my-web-server
sudo docker run -d -p 80:80 --name my-web-server nginx
sudo docker ps
```
---

### Step 6 — Access the Web Server Using the Public IP

The EC2 instance's public IP address (`54.167.115.79`) was entered into a browser to test connectivity to the containerized application over the internet.

---

### Step 7 — Verify Successful Deployment

The browser successfully loaded the default **"Welcome to nginx!"** page, confirming the Docker container was deployed correctly and is accessible from outside the cloud VM over the public internet.

---

## Result

The task was completed successfully. A cloud-based virtual machine was provisioned on AWS EC2, Docker was installed and configured on it, and a containerized Nginx web server was deployed and made publicly accessible through the instance's public IP address.

## Conclusion

This task provided practical experience in combining cloud computing with containerization — two core skills in modern IT and DevOps workflows. Key learnings included:

- Provisioning and managing a virtual machine on a public cloud platform (AWS EC2)
- Connecting to a remote Linux server securely via SSH / EC2 Instance Connect
- Installing and configuring the Docker Engine on a Linux system
- Building and running containers, and mapping container ports to host ports
- Verifying a deployment end-to-end by accessing the application over the public internet
