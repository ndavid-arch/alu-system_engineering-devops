# Web-01 Firewall Configuration

This file contains the UFW (Uncomplicated Firewall) commands to block all incoming traffic on the `web-01` server except essential ports: SSH (22), HTTP (80), and HTTPS (443).

## Commands Used

```bash
# Set default policy to deny all incoming connections
sudo ufw default deny incoming

# Allow SSH connections
sudo ufw allow 22/tcp

# Allow HTTP connections
sudo ufw allow 80/tcp

# Allow HTTPS connections
sudo ufw allow 443/tcp

# Enable the firewall
sudo ufw enable

# Verify rules
sudo ufw status verbose