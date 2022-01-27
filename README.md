# Setup & Deployment

## Install Required Packages or Run System Updates
**should be run on first deployment or to update all packages and system**

`ansible-playbook -i inventory server.yml`

## Deployment

`ansible-playbook -i inventory app-dev.yml`

### Recreate Letsencrypt certificates
a lock file is created to ensure not creating certificates unnecessary again

`rm /var/container/{{ container_name }}/data/certbot/letsencrypt-exists.lock`