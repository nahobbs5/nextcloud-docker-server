# nextcloud-docker-server
Server Setup with WireGuard, Ubuntu LTS, and Docker for NextCloud
This guide walks through setting up a WireGuard VPN to access iDRAC, installing Ubuntu Server LTS, and configuring Docker for a future NextCloud deployment.

## Prerequisites
- Wireguard
- Dell server with iDRAC enabled
- Ubuntu Server LTS ISO
- basic knowledge of Linux command line

## Steps
### 1. Configure WireGuard VPN for iDRAC Access


### 2. Install Ubuntu Server LTS
Set first boot device to virtual CD/DVD/ISO in iDRAC.  
Navigate to Server > Setup > First Boot Device.  
Select Virtual CD/DVD/ISO and apply.  
Boot server with Ubuntu Server LTS ISO via iDRAC virtual media.  
Follow installer prompts
Set up username and password.  
Complete installation and reboot.

### 3. Install Docker
Run the following commands to install Docker on Ubuntu:  
sudo apt update && sudo apt upgrade -y  
sudo apt install docker-compose  

### 3b. Verify Docker Installation
Test Docker with:  
docker --version  
sudo docker run hello-world  

### 4. Create Docker Compose YAML for Nextcloud
Create a docker-compose.yml file for Nextcloud:  
mkdir ~/nextcloud  
cd nextcloud  
touch docker-compose.yml  

### Next Steps

Run sudo docker-compose up -d to start NextCloud.  
Access NextCloud at `http://<server-ip>:8080.`  
Configure NextCloud via the web interface.  

