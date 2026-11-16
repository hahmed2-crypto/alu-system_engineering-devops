# Web stack debugging #1

This directory contains the solution for the second web stack debugging project, focused on diagnosing why Nginx is not listening on port 80 inside an Ubuntu 20.04 container and writing a Bash script to automate the fix.

## Tasks

* **0. Nginx likes port 80** (`0-nginx_likes_port_80`): Ensures the default site is enabled, configures Nginx to listen on port `80` for all active IPv4 addresses, clears any port conflict, and restarts the `nginx` service.
