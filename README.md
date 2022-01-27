# Setup & Deployment

## Install Required Packages or Run System Updates
**should be run on first deployment or to update all packages and system**

`ansible-playbook -i inventory server.yml`

## Deployment

`ansible-playbook -i inventory app-dev.yml`

### Recreate Letsencrypt certificates
a lock file is created to ensure not creating certificates unnecessary again

`rm /var/container/{{ container_name }}/data/certbot/letsencrypt-exists.lock`

### Troubleshooting
the containers may not start properly, if they run for first time

just create a lock file, once the containers started you can delete the file

`touch /var/container/{{ container_name }}/data/certbot/letsencrypt-exists.lock`