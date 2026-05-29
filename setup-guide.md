# Lab Setup Guide

## Prerequisites
- Windows PC with 8GB+ RAM
- VirtualBox installed
- Ubuntu 24.04 LTS ISO
- Free Splunk Enterprise account

## Steps

### 1. Create the Virtual Machine
- Install VirtualBox on Windows
- Create a new VM with 4GB RAM, 2 CPUs, 25GB disk
- Mount the Ubuntu 24.04 ISO and install Ubuntu

### 2. Install Splunk
- Download Splunk Enterprise .deb package from splunk.com
- Install using: `sudo dpkg -i splunk*.deb`
- Start Splunk: `sudo /opt/splunk/bin/splunk start --accept-license --run-as-root`
- Access Splunk at: `http://127.0.0.1:8000`

### 3. Configure Log Monitoring
- In Splunk go to Add Data → Monitor → Files & Directories
- Add path: `/var/log/auth.log`
- Set permissions: `sudo chmod 644 /var/log/auth.log`

### 4. Simulate Brute Force Attack
- Install SSH: `sudo apt install openssh-server -y`
- Run failed logins: `ssh fakeuser@localhost`
- Enter wrong password multiple times

### 5. Detect the Attack in Splunk
- Search: `source="/var/log/auth.log" "Failed password"`
- Build dashboard and set up alerts
