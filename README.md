# Azure Admin Enterprise Infrastructure

This project demonstrates the deployment and monitoring of a production-like Azure infrastructure environment.

## Project Overview

In this project, I performed the following tasks:

- Deployed an Ubuntu 24.04 LTS Virtual Machine in Azure
- Configured secure SSH access using Azure Bastion
- Installed and configured NGINX web server
- Created Azure Monitor CPU metric alerts
- Configured an Action Group for email notifications
- Simulated high CPU usage using stress tool
- Successfully triggered and validated alert notifications

---

## Resource Details

Resource Group: rg-prod-infra  
Virtual Machine: vm-web-02  
Operating System: Ubuntu 24.04 LTS  
Web Server: NGINX  
Monitoring: Azure Monitor Metric Alert  
Action Group: Email Notification  

---

## NGINX Installation Commands

sudo apt update  
sudo apt install nginx -y  
sudo systemctl enable nginx  
sudo systemctl start nginx  
sudo systemctl status nginx  

---

## CPU Stress Testing

sudo apt install stress -y  
stress --cpu 2 --timeout 300  

This command generated high CPU usage and triggered the Azure Monitor alert.

---

## Alert Configuration

Signal: Percentage CPU  
Condition: Greater than 70%  
Evaluation Frequency: 1 minute  
Lookback Period: 5 minutes  
Action: Email notification  

---

## Skills Demonstrated

- Azure Virtual Machines
- Linux Administration
- NGINX Configuration
- Azure Monitor
- Metric Alerts
- Action Groups
- Performance Monitoring
- Cloud Infrastructure Management

---

## Outcome

Successfully designed, deployed, monitored, and tested a secure Azure infrastructure environment with automated alerting and performance validation.
