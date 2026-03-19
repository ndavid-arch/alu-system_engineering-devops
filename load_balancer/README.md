# Load Balancer Project - ALU System Engineering & DevOps

## Overview

This project sets up a web infrastructure with redundancy and load balancing. It automates configuration for web servers and a load balancer using Bash scripts on Ubuntu.

---

## Directory Structure


load_balancer/
├── 0-custom_http_response_header # Adds X-Served-By header to Nginx
├── 1-install_load_balancer # Installs and configures HAProxy
├── README.md # This file


---

## Scripts

### 0-custom_http_response_header
- Configures Nginx on a brand new Ubuntu web server.
- Adds a custom HTTP response header:

X-Served-By: <server hostname>

- This helps track which server handled each HTTP request.
- Usage: run the script on **web-01** and **web-02**.

### 1-install_load_balancer
- Installs and configures HAProxy on a new Ubuntu load balancer server.
- Balances HTTP traffic between web-01 and web-02 using **roundrobin**.
- Ensures HAProxy can be managed via init/systemctl.
- Usage: run the script on **lb-01**.
