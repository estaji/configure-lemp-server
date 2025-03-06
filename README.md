# About
This Ansible role installs and maintains a Linux server that contains Nginx webserver, Mariadb database, PHP and other useful packages.

Not only can this role install a LEMP (Linux+Nginx+Mariadb+PHP) server (on first execution), but also the role provides management features using flag variables (on next executions).

# How
## Requirements
Do these steps before using this role:
- Update authorized_keys for root user
- Change ssh port and disable PasswordAuthentication in ssh configurations (recommended)
- Copy ssl certificates and dhparams.pem to /etc/nginx/ssl/
- Ensure website files directory is copied to /usr/share/nginx/ & (for Wordpress website) Modify wp-config.php file
- Configure the Mariadb and import the database after running this playbook

## Usage
To use the role, you can create your own playbook.yaml and inventory files.

Then modify vars section in your playbook.yaml file to overwrite variables.

Run the playbook.

## Caution
Running this playbook will overwrite and change some configuration files.

Add the SSH port in templates/iptables.j2 file.

# Contribution
Feel free and don't hesitate to contribute to this repository.
