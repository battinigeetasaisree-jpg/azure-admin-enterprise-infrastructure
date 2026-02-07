# Azure Admin Enterprise Infrastructure

This project demonstrates the design, deployment, and management of a secure, production-like Microsoft Azure environment.

It showcases core Azure administration skills aligned with AZ-104 including networking, security, monitoring, and alert validation.

---

## Architecture Overview

- Hub-Spoke Networking Architecture
- Virtual Network Peering
- Network Security Groups (NSGs)
- Bastion Secure SSH Access
- Ubuntu 24.04 LTS Virtual Machine Deployment
- NGINX Web Server Installation
- Azure Monitor Metric Alerts
- Action Groups & Email Notifications
- CPU Stress Testing for Alert Validation
- Infrastructure Monitoring & Governance

---

## Project Implementation

In this project, I performed the following tasks:

- Created structured Resource Groups
- Designed Hub and Spoke VNets with subnets
- Configured NSG inbound and outbound rules
- Deployed Ubuntu 24.04 LTS Virtual Machine
- Secured VM access using Azure Bastion (no public IP exposure)
- Installed and configured NGINX web server
- Created Azure Monitor CPU metric alert (>70%)
- Configured Action Group for email notification
- Simulated high CPU usage using stress tool
- Successfully triggered and validated alert notifications

---

## Monitoring Validation

CPU usage was artificially increased using:

stress --cpu 2 --timeout 300


This triggered:
- CPU spike in Azure Metrics
- Alert rule fired (Severity 2 – Warning)
- Email notification received

---

## Skills Demonstrated

- Azure Networking
- Infrastructure Security
- Linux VM Administration
- Monitoring & Observability
- Incident Alerting & Validation
- Production-like Environment Simulation

---

## Screenshots

All implementation proof is available in the `/screenshots` directory.

---

## Security Design Considerations

- No Public IP assigned to Virtual Machine
- Secure access provided through Azure Bastion
- NSG rules restricted to required ports only
- Principle of least privilege applied

---

## Cost & Governance Considerations

- Used minimal VM size for testing
- Alert evaluation frequency optimized (1 min check, 5 min lookback)
- Resources organized using structured naming conventions
- Monitoring cost estimated before deployment
